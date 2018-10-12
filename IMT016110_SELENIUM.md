Download and install selenium and a webdriver. The following method is for chrome webdriver. Make sure the driver is in the executable path. Selenium generally starts a browser to run the tests. The goal is to do this in the background without any display. This can be done easily by adding an argument to the chrome options. 
```
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
```
To access the chrome options:
```
options = webdriver.ChromeOptions()
```
Now add an argument 'headless' to these options
```
options = webdriver.ChromeOptions()
options.add_argument('headless')
```
Start the driver and run the tests

```
browser = webdriver.Chrome(options = options)

browser.get("http://www.google.com")
assert 'Google' in browser.title

browser.close()
```
