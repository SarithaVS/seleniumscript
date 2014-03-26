seleniumscript
==============

selenium_explicit
import selenium
from selenium import webdriver

driver=webdriver.Firefox()
driver.get("http://mail.yahoo.com")
el=driver.find_element_by_link_text("Facebook")
el.click()

for handle in driver.window_handles:
    driver.switch_to_window(handle) 
    if (driver.title == "Facebook"):
        username = driver.find_element_by_id("email")
        username.send_keys("srivarsang@gmail.com")
        inputpass = driver.find_element_by_id("password")
        inputpass.send_keys("savithiri1989")
        e2=driver.find_element_by_id("Log In")
        e2.click()
