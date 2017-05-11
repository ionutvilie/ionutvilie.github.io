---
layout: post
title:  "Prometheus Alert Automation"
date:   2017-05-11 10:00:00 0000
categories: prometheus.io automation golang
---
In order to start to automate something, eg: prometheus, you must first start to observe patterns.

After starting to define alerts, some patterns popped up related to type of alerts (sla, cpu, etc), conditions and labels. 
Main problem will be labels and condition, so ended up defining a template for each one.

I have wrote an app that uses golang's "text/templates". 
The data i need, i get from a control center api.

Below is a sample of the code. The entire app is not shared as it is useless to anybody else, i hope the idea is not.

<script src="https://gist.github.com/ionutvilie/b4ee4f80292c4e33efcbc1b53df87fc5.js"></script>


