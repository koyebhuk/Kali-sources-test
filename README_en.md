# Kali Source Test Tool

This project is a web tool for testing the status, latency, and download speed of multiple Kali Linux image sources. Users can test all sources with one click, select the best update source based on the test results, and support one-click copy of source configurations.

## Features

- One-click testing of multiple Kali image sources for availability, latency, and download speed
- Results can be sorted by speed or latency
- Automatically suggests the best source (lowest latency)
- Support one-click copy of source configuration to clipboard
- Result summary and configuration preview are highlighted
- Responsive design, suitable for desktop and mobile

## How to use

1. Download the [Kali-sources-test.html](https://kali-sources-test.pages.dev/) file directly with your browser, no server environment is required.
2. Click the "Start Test All Sources" button and wait for the test to complete.
3. You can click the "Sort by Speed" or "Sort by Delay" button as needed.
4. The recommended source and optimal configuration will be automatically displayed after the test is completed, and you can also click the "Copy Configuration" button in each source card to get the corresponding configuration.
5. When the "source repository" does not test, directly use the "Copy Configuration" button to obtain the corresponding configuration.

## Replication configuration function

There are two buttons at the bottom of each source card:
- Retest: Retest the source individually
- Copy Configuration: Generate the full configuration information for the source, for example:
```text
# USTC: Kali Rolling Update Branch
deb http://mirrors.ustc.edu.cn/kali kali-rolling main non-free contrib 
deb-src http://mirrors.ustc.edu.cn/kali kali-rolling main non-free contrib
```

After clicking the "Copy Configuration" button, the configuration information will be displayed in the preview area at the bottom of the page, and you can:

1. Read the configuration directly
2. Click the "Copy Configuration" button to copy the content to the clipboard
3. Paste into your Kali system source configuration file ('/etc/apt/sources.list').

## Dependencies

- [Font Awesome](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css)
	Provides a library of scalable vector icons (SVG icons) that can be called via CSS without the need to download image files.
- [Google Fonts - Roboto](https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap)
	Dynamically load Roboto fonts (modern sans-serif fonts designed by Google) from Google servers.

The above dependencies are automatically loaded through the CDN and do not need to be manually installed.

## File description

- ['Kali-sources-test.html']: The main page and all functions are implemented

## Screenshots

[Preview not shown. Click to view the effect.](https://kali-sources-test.pages.dev/)

## Disclaimer

The test results of this tool are for reference only, actual speed and availability may be affected by the network environment. Please test regularly for the best experience.

---

If you have suggestions or questions, please feel free to submit an issue or PR!