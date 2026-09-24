# Linux File Monitoring with Auditd

## Overview

In this project, I used the Linux Audit daemon (`auditd`) to monitor changes made to files on an Ubuntu system.

I created an audit rule to watch a file for changes, edited the file, and then checked the audit logs to see what was recorded.

## Tools Used

* Ubuntu/Linux
* auditd
* auditctl
* ausearch
* Vim
* Linux command line

## Investigation Process

### 1. Set Up Auditd

I installed `auditd` on my Ubuntu VM and checked that the service was running before creating any rules.

### 2. Create a File to Monitor

I created a test file and added some content to it using Vim. I used this file to test whether Audit could detect changes made to it.

### 3. Create an Audit Rule

I created an audit rule to watch the file for write activity.

I also added a filter key to the rule so I could easily search for events connected to that file later.

### 4. Trigger the Rule

After setting up the rule, I made a change to the monitored file so that Audit would record the activity.

### 5. Review the Audit Logs

I first looked through the audit log and noticed that it contained a lot of system activity.

I then used `ausearch` with the filter key from my rule to narrow down the results and find the events connected to the file I changed.

## Skills Demonstrated

* Linux system monitoring
* Auditd configuration
* File integrity monitoring
* Audit rule creation
* Linux log analysis
* Host-based intrusion detection
* Command-line investigation
* Event filtering
* Incident investigation

## What I Learned

This project helped me understand how host-based monitoring can be used to track changes made directly on a system.

I also learned how useful filter keys can be when working with large audit logs. Instead of going through every event manually, I could search using the key from my rule and quickly find the activity I was looking for.
