Checking running processes

Command: ps aux | head

Observation: Viewed the currently running processes along with their CPU and memory usage.

----------------------------

Live process monitoring

Command: top

Observation: Saw system activity in real time, including running programs and how much CPU and memory they were using.

-----------------------------

Service Practice (systemd)

Checking SSH service

Command: systemctl status ssh

Observation: The output showed that the SSH service is active and currently running on the EC2 instance.

-----------------------------

Listing running services

Command:systemctl list-units --type=service --state=running | head

Observation: This command shows which services are currently active and running in the system.

------------------------------

Log Practice

Checking SSH service logs

Command: journalctl -u ssh --no-pager | tail -n 20

Observation: Saw recent SSH activity, like login attempts and connections.

------------------------------

Checking system logs

Command: sudo tail -n 30 /var/log/syslog

Observation: This showed what the system was doing recently and messages from programs running in the background.



