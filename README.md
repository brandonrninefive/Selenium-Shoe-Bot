# Selenium Shoe Bot (DEPRECATED!)

**This program is old and no longer works on the nakedcph site. This repo remains here as a simple example of how to use Selenium to make an automated purchase bot. This code is no longer maintained. Please do not DM me to improve this code, you will be on your own.**

*NOTE: This program is made for Python 2.7.X and will not work with Python 3.X.X!*

This is a simple Python bot which uses Selenium to navigate the website [http://www.nakedcph.com/](http://www.nakedcph.com/)  and quickly checkout shoe orders. Although the script was written with the specific intention of making shoe orders, there is nothing stopping users from checking out other items on the site through the script. Users can configure how many orders they want to make, including the credit card info to use and various items to checkout within each order by editing the included checkout.conf JSON file. The script is configured to use the PhantomJS headless webdriver, which is included as a NodeJS dependency. Chromedriver is also included as a dependency in the case that you don't want to use a headless webdriver.

## Installation Instructions (Linux/Mac)

1. Make sure that you have Python 2.7.X installed, along with Pip.

2. Install Node.js and NPM.

3. Download or clone this repository to a directory on your machine.

4. Add the directory containing this project into your global PYTHONPATH environment variable. *NOTE: If you get an error stating that checkout.conf cannot be found, or that it contains invalid JSON, but the JSON in checkout.conf is correct, you may not have performed this step.*

5. Open the terminal, navigate to the project directory, and type the command `pip install -r requirements.txt`. This should install the Python dependencies Selenium and Chromedriver. *NOTE: On Mac, the dependency chromedriver-installer may not download. If this is the case, you will have to install Chromedriver manually.*

6. From the terminal, type the command `npm install`. This should install PhantomJS.

7. Edit the checkout.conf JSON file to your liking, but make sure that it still contains valid JSON syntax.

8. You may edit autocheckout.py to use Chromedriver instead of PhantomJS if you wish to view the browser navigation performed by the script. 

9. Run the program from the terminal with `python autocheckout.py`. *NOTE: If the checkout process does not complete properly and the program crashes (not including JSON errors, see instruction number 4 for those), then that means that one of two things occurred: Either the site did not have the desired quantity of a particular item in your order, or the website's HTML has been updated since the writing of this script. If the latter is true, then you can try commenting out the alternate code section in the script, and uncommenting the default code section. Please refer to the comments in the script for finding these sections. If neither of the code sections work, then the HTML hardcoded into this script may be outdated. Feel free to modify the HTML in the script to fit your needs. If you wish to debug the script further, you can comment out the PhantomJS driver initialization in the script, and uncomment the Chromedriver initialization to view the browser's progress in real time.*

## Installation Instructions (Windows)

This script has not been tested for Windows, but it should still work if a similar procedure is followed as the one for Linux/Mac.
