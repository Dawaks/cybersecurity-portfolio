# Linux File Monitoring with Auditd

## Overview

In this project, I used the Linux Audit daemon (`auditd`) to monitor changes made to files on an Ubuntu system.

I created audit rules to watch for file modifications, made changes to a monitored file, and then reviewed the audit logs to find the events that were generated.

## Tools Used

* Ubuntu/Linux
* auditd
* auditctl
* ausearch
* Vim
* Linux command line

## Investigation Process

### 1. Set Up Auditd

I installed `auditd` on the Ubuntu VM and checked that the service was running correctly before creating any monitoring rules.

### 2. Create a File to Monitor

I created a test file and added some content to it using Vim. This gave me a file that I could use to test the monitoring rule.

### 3. Create an Audit Rule

I created an audit rule that watched the file for write activity.

The rule used a filter key so I could easily search for events connected to that specific file later.

### 4. Trigger the Rule

After setting up the rule, I modified the monitored file to generate an audit event.

### 5. Review the Audit Logs

I first looked at the audit log and saw how much information was being recorded.

I then used `ausearch` with the filter key to narrow the results down to the events related to the file I was monitoring.

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

I also learned how audit rules and filter keys make it easier to find specific activity in large audit logs. Instead of searching through every event manually, I could use the rule key to focus on the activity I wanted to investigate.
