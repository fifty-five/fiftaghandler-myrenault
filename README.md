FIFTagHandler cordova plugin
============================

* [Introduction](#introduction)
* [Installation](#installation)
* [Getting started](#getting-started)

## Introduction

This plugin provides Apache Cordova/Phonegap support for the FIFTagHandler using the native sdks for Android & iOS. The FIFTagHandler SDK is a wrapper above the Google Tag Manager SDK. It enable iOS/Android developers to track their apps using only GTM. The FIFTagHandler SDK currently support the following trackers: Google Analytics, Facebook, Localytics, ATInternet, MobileAppTracker and Follow Analtics.

Android Native SDK v4 (using Google Play Services SDK)
iOS Native SDK v3
This plugin provides support for some of the most specific analytics functions (screen, event & exception tracking, custom metrics & dimensions) and also the more generic set and send functions which can be used to implement all of the Google Analytics collection features.

## Installation

#### Using the Cordova CLI
To install the FIFTagHandler plugin in your app, use the following command-line

```shell

	cordova plugin add https://github.com/fifty-five/fiftaghandler-myrenault

```



## Getting started

#### Initialize the FIFTagHandler SDK

To initialize the FIFTagHandler SDK, use the `initWithContainerId` function. Make sure to pass the Google Tag Manager container identifier as parameter.

```js

	var fiftaghandler = navigator.fiftaghandler;

	//activate verbose mode 
	fiftaghandler.setVerboseLoggingEnabled()
	
	// Init using the GTM container id
	fiftaghandler.initWithContainerId('GTM-XXXX');

```

#### Push key / value object to the DataLayer

Once the FIFTagHandler SDK is initialized, you can push events / data to the Google Tag Manager DataLayer. Using the `push` function to push any key/value pair. For instance, just after initializing the FIFTagHandler, we push an appStarted event to the DataLayer

```js

	// Push appStarted event to the DataLayer
	fiftaghandler.push({'event': 'applicationStart'});

```


