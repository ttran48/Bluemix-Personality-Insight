Visual Recognition

About: Visual Recognition allows users to understand the contents of an image or video frame, answering the question: “What is in this image?”

Steps to invoke API:

Navigate to BlueMix > Catalog > Watson > Visual Recognition

Click on View Docs

Click on Try It Out.

Scroll up and click on View Demo under EVALUATE.

Click on “Fork on GitHub”.

Click Clone or Download button (Green button).

Go to the location where you downloaded personality insights GitHub code in step 5, and open the file “manifest.yml”. Open it in Notepad or Notepad ++ (preferred).

Edit the manifest.yml file, and change the - name: visual-recognition-demo line to something unique.

In the command prompt, change directory and go inside the visual recognition download location folder, (for e.g. C:\Users\pande\Desktop\visual-recognition-nodejs-master) and type the following:

For MAC Users:

Mac Users who are not aware how to copy the path of a file, can follow the steps given in below URL:

HYPERLINK "http://osxdaily.com/2013/06/19/copy-file-folder-path-mac-os-x/" http://osxdaily.com/2013/06/19/copy-file-folder-path-mac-os-x/

cf api HYPERLINK "https://api.ng.bluemix.net" https://api.ng.bluemix.net

cf login -u

Enter Password

Create Visual Recognition service in BlueMix:

cf create-service watson_vision_combined free visual-recognition-service

Push it Live:

cf push
