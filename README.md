Linux SSH Brute Force Investigation Project
Introduction

In this project, I investigated suspicious SSH login attempts on a Linux server.
The goal was to check whether it was a brute force attack and if the attacker was successful.

Log Source

Log File: /var/log/auth.log

Service: SSH (Port 22)

What I Found

The log file showed multiple failed login attempts like this:

Failed password for user1 from 185.220.101.45 port 22 ssh2
Failed password for user1 from 185.220.101.45 port 22 ssh2
Failed password for user1 from 185.220.101.45 port 22 ssh2

There was no "Accepted password" entry found.

Investigation Steps

Opened the Linux authentication log file.

Checked for SSH login activity.

Observed multiple failed login attempts from the same IP address.

Checked if any successful login happened.

Confirmed that no successful login was recorded.

Analysis

Many failed login attempts from the same IP address indicate password guessing.

SSH runs on port 22 and allows remote access.

Since no successful login occurred, the attack did not succeed.

This shows it was a brute force attack attempt, but it was unsuccessful.

Final Conclusion

Brute Force Attack Attempt – Unsuccessful

Recommended Actions

Block the suspicious IP address.

Use strong passwords.

Enable account lockout policy.

Monitor the server for future attacks.

Skills Learned

Linux log analysis

Understanding SSH logs

Identifying brute force attack patterns

Writing basic incident reports
