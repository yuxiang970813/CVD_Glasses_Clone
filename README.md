# Colour Vision Deficiency Glasses Clone

## Description

### What this Application Does

Colour Vision Deficiency Glasses Clone is a chrome extension implemented to alleviate colour vision deficiency. These glasses clones are only suitable for some types of colour vision (such as protanomaly and deuteranomaly). Its function is not to allow people with the colour vision to see colours that they would not otherwise be able to see but to help them distinguish between colours and similar shades.

### Video Demo
https://youtu.be/oOOzMytJlIY

### Technologies Used

* HTML

* CSS

* JavaScript

* JSON

* SVG

### Each of the Files in this Project Contains and Does

* `manifest.json` -
Gives the browser information about this extension. Note that the `manifest.json` requires "**permissions**" of "**storage**" to store the user's last setting.

* `popup.html` -
When clicking this extension toolbar icon, a popup will display with an **ON/OFF** button for ease to use.

* `style.css` -
Normal CSS file, just stylize the popup.

* `script.js` -
This script access all the tabs that are open, and listens to the **ON/OFF** button event. When the user clicks the **ON/OFF** button, it will send the tabs"s id and current button status to the `content.js`.

* `content.js` -
The `content.js` listen to the message sent from `script.js`. It will enable or disable the filter based on the message and apply it to all current tabs. When enabled, the `content.js` embed a CSS **\<style>** tag and a SVG **\<svg>** tag into the HTML **\<body>**, and adds a **"class"** to the **\<html>** tag. The **\<style>** tag contains a filter that cut the screen into small pixels. In every pixel, the SVG filter force the pixel's colour closed to trichromatic colour, making red things more red, blues things more blue, and so on, making it easier to distinguish a similar shade. When disable, the `content.js` remove the **"class"** in the **\<html>** tag.

## How to Install and Run this Project

This is an unpacked chrome extension file. After downloading:

1. Go to `chrome://extensions`

2. Enable Developer Mode by clicking the toggle switch next to **Developer mode.**

3. Click the **Load unpacked** button and select the extension directory.

## How to Use this Project

Just click the **ON/OFF** button to enable or disable the Colour Vision Deficiency Glasses Clone filter.
