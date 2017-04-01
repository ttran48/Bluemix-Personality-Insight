# Bluemix-Personality-Insight
## Steps to invoke API:

1. Navigate to Catalog > Watson > Personality Insights

2. Click on Create at the right bottom of the page.

3. Click on Demo under Development Resources.

4. Click on “Fork on GitHub”. (The demo application’s code which uses Bluemix’s personality insights service can be accessed through GitHub using this link.)

5. Click Clone or Download button (Green button). (Download it to your desktop’s and take a note of the location.)

=============== (NOTE: This step is ONE TIME only for all Watson labs) ================

6. Scroll down and Click on Cloud-foundry CLI link under Getting Started using CLI Cloud Foundry. Download ‘Installers’ (NOT Binaries)

7. Select the appropriate Installer as per your operating system.

8. Download and install the program. (install Installers only) Make a note of the install directory: C:\Users\MR\Downloads\cf-cli-installer_6.23.1_winx64

9. To confirm if Cloud foundry is installed correctly open your command prompt/Terminal (Start > cmd) and type cf –version. The current version installed should be shown. (If you get any such message it can be ignored.

======================================================================

10. Go to the location where you downloaded personality insights GitHub code in step 5, and open the file “manifest.yml”. Open it in Notepad or Notepad ++ (preferred).

11. Edit the manifest.yml file and change the to something unique. Include your name in place of livedemo.

12. In the command prompt, change directory and go inside the personality insights download location folder, (for eg. C:\Users\pande\Desktop\personality-insights-nodejs-master) and type the following:


>> cf api https://api.ng.bluemix.net

>> cf login -u

>> Enter Password

>> (Here Bluemix connects to the cloud foundry (cloud platform) with the login details.)

13. Create and retrieve service keys to access the [Personality Insights][service_url] service:

14. cf create-service personality_insights tiered my-pi-service

15. cf create-service-key my-pi-service myKey

16. cf service-key my-pi-service myKey

In this step the service is being created. This can be done in 2 ways:

1. Command prompt

2. BlueMix (students in this exercise use option 1.

The service comes with two pricings – Standard or Tiered. Few applications that are most popular like personality insights comes in Tired. Tiered pricing is typically used for charge metrics that are expected to have very high quantities per month, such as API calls.

17. Create a .env file in the root directory by copying the sample .env.example file using the following command:
""" 
copy .env.example .env
"""
You will update the .env with the information you retrieved in steps 13.

The .env file will look something like the following:

PERSONALITY_INSIGHTS_USERNAME=

PERSONALITY_INSIGHTS_PASSWORD=

For MAC Users:

You might have noticed that you are unable to view the above files in MAC. Basically, these files are all those which start with a 'dot'. Mac OS hides all such files which start with a 'dot'.

To unhide all such files type follow following steps:

Copy the path of the folder where you would like to unhide the files.

Go to command prompt, and change the directory to the path you copied above.

Run following command: - 

defaults write com.apple.finder AppleShowAllFiles -bool YES

killall Finder

Push it Live: Run the below command in the command prompt/Terminal

cf push
