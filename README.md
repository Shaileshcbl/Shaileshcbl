from selenium import webdriver
from selenium.webdriver.chrome.service import Service as ChromeService
from webdriver_manager.chrome import ChromeDriverManager
from selenium.webdriver.common.by import By
import time


driver = webdriver.Chrome(service=ChromeService(ChromeDriverManager().install()))
time.sleep(2)
driver.maximize_window()
time.sleep(2)
driver.get("https://omayo.blogspot.com/")
time.sleep(2)
driver.find_element(By.ID, "ta1").send_keys("Hii I am Automation tester")
time.sleep(2)
driver.find_element(By.NAME, "q").send_keys("ABCD")
time.sleep(2)
driver.find_element(By.CLASS_NAME, "dropbtn").click()
time.sleep(8)
driver.find_element(By.LINK_TEXT, "compendiumdev").click()
time.sleep(5)
driver.find_element(By.XPATH, "//input[@value='Login']").click()
time.sleep(5)
driver.find_element(By.XPATH,"/html/body/div[4]/div[2]/div[2]/div[2]/div[2]/div[2]/div[2]/div/div[4]/div[1]/div/div/div[5]/div[1]/form/input[1]").send_keys("shailesh")
time.sleep(20)
