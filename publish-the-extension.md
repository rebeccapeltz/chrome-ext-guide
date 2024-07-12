---
description: >-
  Before we can publish, we need to zip up the folder containing the files to be
  published. We also need to create screenshots that will be displayed on the
  Chrome Web Store page.
---

# Publish the Extension

### Chrome Developer Console

You must set up an account and access the [Chrome Web Store Developer Dashboard](https://chrome.google.com/webstore/devconsole/) to publish an extension.

<figure><img src=".gitbook/assets/chromedevdashboard.png" alt=""><figcaption><p>Chrome Developer Dashboard with entry for Extension</p></figcaption></figure>

### Prepare Images for Chrome Web Store Listing



### Create a Zip File

The folder that is zipped for **Link Reveal** looks like this:

<figure><img src=".gitbook/assets/folder-zipped.png" alt=""><figcaption><p>Folder containing manifest, code and image for extension</p></figcaption></figure>

There are a couple of files that have not been discussed yet.  The `index.html` renders a web page containing a lot of different variations on links to test with.  The `nolinks.html` contains no links.  When there are no links on the user's web page, a message will appear indicating that no links were found and that a page refresh might help.  This is because some pages get put to sleep, and if the user returns to a page, the refresh will help make it available for injections.

### Prepare a Security Policy Document Link



### Publish Process







