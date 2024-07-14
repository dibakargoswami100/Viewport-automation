# Viewport Automation using Python Selenium

This project demonstrates how to automate viewport testing using Python and Selenium. The script resizes the browser window to various viewports to test the responsiveness of a website.


https://github.com/user-attachments/assets/937ca29c-e678-4b68-aff1-786c1053265d


## Project Overview

The goal of this project is to automate the process of resizing the browser window to different viewport dimensions and observing the behavior of a website. This can be useful for testing the responsiveness of web applications across different device sizes.

## Features

- Automates browser window resizing to multiple viewport dimensions.
- Uses Selenium WebDriver for browser automation.
- Supports multiple viewports including common device sizes.
- Includes error handling to ensure browser closes properly after execution.

## Viewports

The following viewport dimensions are included in the script:

- 1024 x 768
- 768 x 1024
- 375 x 667
- 414 x 896

## Prerequisites

- Python 3.x
- Google Chrome browser
- [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/) (Make sure to have the executable path correctly specified)

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/viewport-automation.git
    cd viewport-automation
    ```

2. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

3. Make sure you have ChromeDriver installed. You can download it from [here](https://sites.google.com/a/chromium.org/chromedriver/) or use `webdriver_manager` to automatically handle it.

## Usage

Run the script using the following command:

```bash
python viewport_automation.py
```

## Code

```python

import time

from selenium import webdriver
viewports = [(1024,768),(768,1024),(375,667),(414,896)]

driver = webdriver.Chrome()
driver.get('https://www.google.com/')

try:
    for width,height in viewports:
        driver.set_window_size(width,height)
        time.sleep(4)

finally:
    driver.close
``

## Contributing

Contributions are welcome! Please fork this repository and submit pull requests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Selenium](https://www.selenium.dev/)
- [webdriver_manager](https://pypi.org/project/webdriver-manager/)
```

### Instructions for the `requirements.txt` file:

Make sure to create a `requirements.txt` file with the following content:

```
selenium
webdriver_manager
```

This `README.md` provides an overview of the project, instructions on how to set it up and run it, and the necessary code to demonstrate its functionality.
