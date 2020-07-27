# Facebook Auto-comment/reply application
An application that will post comments/replies in an automated fashion

## Installation
This guide has been written for Windows environment

### Download ChromeDriver
ChromeDriver 84.0 is included by default but check this website [ChromeDriver](https://chromedriver.chromium.org/downloads) for your compatible version.


### Config.ini
Modify the path in `config.ini` to match the location of your chromedriver.exe. Fill in with your username and password as well as the URL of the comment you want to reply on.

### Facebook MFA
Turn off your multi-factor authentication for Facebook.

## Running
`python app.py`

## Further configurations
### Timeout Between Comments
Default timeout between comments is 5 seconds. You can set it to a fix amount in line 29:  
```python
timeout = [
    5
]
```
This accepts a list of integers and the application will randomly choose one.
```python
timeout = [
    5, 10, 30, 60, 120
]
```
### Comment Count
The default comment count is 10. You can change it in line 50: `while count < 10:`