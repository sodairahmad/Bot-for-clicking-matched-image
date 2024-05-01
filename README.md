# Bot-for-clicking-matched-image


#The Main Function
import pyautogui
import time

def click_accept_button():
    while True:
        try:
            accept_button_location = pyautogui.locateOnScreen('image22.png', confidence=0.8)
            if accept_button_location is None:
                print("Button not found. Retrying...")
                time.sleep(0.01)
            else:
                print("Button found.")
                accept_button_center = pyautogui.center(accept_button_location)
                pyautogui.click(accept_button_center)
                print("Your match is accepted. Continuing...")
                time.sleep(1)
        except Exception as e:
            print("Error:", e)
            time.sleep(0.001)

if __name__ == "__main__":
    click_accept_button()
