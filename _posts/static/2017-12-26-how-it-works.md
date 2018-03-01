---
layout: post
howtos: true
published: true
title: How it works
permalink: howtos/how-it-works
description: What you need to know
---

Flyve MDM Agent works with the [Web MDM Dashboard](http://flyve.org/web-mdm-dashboard/) and [Flyve MDM Plugin](http://flyve.org/glpi-plugin/) for GLPI.

The Agent takes control of the iOS devices of your fleet and applies the policies and commands given from the Web Dashboard or GLPI interface.

To be able to implement this, both device and backend communicate with MQTT, a machine to machine protocol, which maintains the remote connectivity for management.

### Process

The user who owns the iOS device receives an invitation to his email account, the invitation contains a deeplink with it the App can start the enrollment, the user introduces his information and with the information provided by the Agent, the device is registered in the GLPI DB along with the user.

<br>

<div>
<img src="https://github.com/Naylin15/Screenshots/blob/master/ios-agent/enroll.png?raw=true" alt="Start Enrollment" width="300">

<img src="https://github.com/Naylin15/Screenshots/blob/master/ios-agent/enrollment.png?raw=true" alt="Enrollment" width="300">
</div>

A fleet is created with the policies required by the Administrator, later the device is assigned to it, then the Agent applies immediately the commands sent through MQTT.

The Agent provides the information of the supervisor of the device.

<img src="https://github.com/Naylin15/Screenshots/blob/master/ios-agent/information.png?raw=true" alt="User information" width="300">

Flyve MDM Agent for iOS is running on iOS 9.3 and higher.