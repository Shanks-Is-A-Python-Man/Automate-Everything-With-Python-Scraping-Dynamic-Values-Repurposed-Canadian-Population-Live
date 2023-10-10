from selenium import webdriver
import time

def get_drvier():
    # Set options for browsing ease
    options = webdriver.ChromeOptions()
    options.add_argument("disable-infobars")
    options.add_argument("start-maximized")
    options.add_argument("disable-dev-shm-usage")
    options.add_argument("no-sandbox")
    options.add_experimental_option("excludeSwitches", ["enable-automation"])
    options.add_argument("disable-blink-features=AutomationControlled")

    driver = webdriver.Chrome(options=options)
    driver.get("https://www150.statcan.gc.ca/n1/pub/71-607-x/71-607-x2018005-eng.htm")
    return driver

#You can use this to split a counter's number from text if it's displayed as such.

###def clean_text(text):
###extract temp from text
   ### output = float(text.split(": ")[1])
    ###return output

def main():
    driver = get_drvier()
    time.sleep(2)
    element = driver.find_element(by="xpath", value="/html/body/main/section[1]/div[4]/div[3]/div/div[1]")
    return element.text
