---
description: >-
  Follow along with the Design, Creation, and Publishing of a Chrome Browser
  Extension that analyzes and reports on page links.
---

# Introduction

<figure><img src=".gitbook/assets/url-128.png" alt="Extension Icon"><figcaption><p>Extension Icon: always check the bait before you fish</p></figcaption></figure>

### What is a Browser Extension?

Browser extensions are software programs that can be added to a browser to introduce new features and functionality.  Extensions can target specific URLs or all URLs.   Once a developer has published their extension code, it is available in a store to easily add to the browser. &#x20;

* [Chrome Web Store](https://chromewebstore.google.com/)
* [Edge](https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home)
* [Firefox](https://addons.mozilla.org/en-US/firefox/)
* [Safari](https://apps.apple.com/us/story/id1377753262)

Browser extensions provide different ways to access a web page's contents and local storage. This makes them a potential security threat, but they can also help mitigate some security issues.

The instructions in this guide will walk through identifying and solving a problem using a Chrome extension.

### Use Cases for Browser Extension

If you look through the many extensions that have been published, you'll find they solve some common problems.  A list of use cases for extensions is shown below:

* Ad Blocking
* Password Management
* SEO Analytics Tracking
* Proofreading
* Shopping Deals and Product Finders

### Identifying a Problem

A browser extension can serve as a solution to a problem.  Looking at the use cases above, we can identify some problems that browser users have come across:

* How can I block ads?
* I need a tool to help manage my passwords.
* I need a tool to track SEO analytics on my web pages.
* I need help proofreading the content I write on the web.
* Where can I buy an item I want to purchase at a discount?

This guide will focus on creating a browser extension that helps mitigate phishing. Phishing is a cybersecurity threat that occurs when a user clicks on a link, leading to malware installation. Companies often have programs to make users more vigilant about phishing. For example, they can educate their employees about phishing and ask them to hover over links to ensure the underlying URL looks valid. &#x20;

When you familiarize yourself with all of the attributes available in a web page link, you realize that just hovering over a link to see the URL is not enough to know what might happen once you click on it.

```markup
<div><a href="https://www.example.com" target="_blank"
    onclick="alert('my href is unencrypted but chrome will make it secure - try http://info.cern.ch/ a browser without https applied'); return true;">Unencrypted!!</a>
</div>
```

In the anchor tag above, the URL referenced by the `href` attribute looks valid. However, clicking on the link will cause the onclick event handler to execute some JavaScript, and the user won't navigate to the URL until the JavaScript code execution is complete. This could not be detected by just hovering over the link on the web page.

In this guide, we'll develop a Chrome extension that pops up a report showing information about each link on a web page. The following sections will describe the extension's creation and how to publish it to the Chrome Web Store.

