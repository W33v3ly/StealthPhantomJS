# StealthPhantomJS
I update the official selenium module service.py 

This module allow you to complety hide any output as browser or console from selenium combined with PhantomJS

## Prerequirements<br/>
pip install selenium

## Install
1.Download service.py <br/>
2.Replace your service.py with mine you can find it in: <br />
(C:\Users\XXX\AppData\Local\Programs\Python\Python36-32\Lib\site-packages\selenium\webdriver\common\)<br/>
3.Download PhantomJS from http://phantomjs.org/ <br/>
4.Copy your phantomjs.exe to your optional folder example : C:\PythonProjects\StealthTest\phantomjs.exe<br/>
5.Now create test file ex: webtest.py with code:<br/>

```python
from selenium import webdriver

phantomjs_path = "phantomjs.exe" #Path to our phantomjs.exe
driver = webdriver.PhantomJS(executable_path=phantomjs_path) 
driver.set_window_size(1024, 768)
driver.get('http://facebook.com/')   #open url
driver.save_screenshot('shot.png')   #screenshot.png from site
driver.quit()
print("png file created")
```

6.Now run it and you have working Stealth Selenium+PhatomJS script<br/>
(I tested it on Windows 10 + Python 3.6.1)
