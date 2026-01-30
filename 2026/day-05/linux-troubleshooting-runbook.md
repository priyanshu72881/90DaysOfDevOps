Day 05 – Linux Troubleshooting Drill: CPU, Memory, and Logs
----------------------------------------------------------------

1. Environment Basics
uname -a
cat /etc/os-release
Observation: This showed which Linux kernel is running on the system and which version of Ubuntu is installed.

<img width="1919" height="600" alt="image" src="https://github.com/user-attachments/assets/3d851756-12c7-4172-b13f-d001f707b950" />

2. Filesystem Sanity Check
mkdir /tmp/runbook-demo
cp /etc/hosts /tmp/runbook-demo/hosts-copy
ls -l /tmp/runbook-demo
Observation: I created a new folder and copied a file into it to test the filesystem. This confirmed that the system can create and manage files and directories properly.
<img width="1913" height="353" alt="image" src="https://github.com/user-attachments/assets/01ceeaba-a508-45c2-b756-26151c58407b" />

Snapshot: CPU & Memory
Command:top
Observation: Saw live system activity and identified which processes were using the most resources.
Command:free -h
Observation: Checked how much memory is used and how much is free to make sure the system is not running out of RAM.


Check disk space usage
Command:df -h
Observation: Checked how much disk space is used and how much free space is available on the system.

Command:du -sh /var/log
Observation: Checked the total size of log files to make sure logs are not taking too much disk space.

SSH Logs Review
Command: journalctl -u ssh -n 50 --no-pager
Observation: Checked the recent SSH logs and did not find any serious or repeated errors. This confirmed that the SSH service is running normally.
