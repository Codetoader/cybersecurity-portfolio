Username Enumeration and Password Brute-Force Attack

Objective
Demonstrate how username enumeration and password brute-force attacks can be performed against a vulnerable login form.

Tools Used
Burp Suite Proxy
Burp Suite Intruder

Methodology
Intercepted login requests using Burp Proxy.
Sent the request to Burp Intruder.
Configured a Sniper attack.
Supplied a wordlist containing potential usernames.
Analyzed server responses to identify differences indicating a valid username.
Repeated the process using a password wordlist to identify a valid password.

Findings
Successfully identified a valid username from the supplied username wordlist.
Successfully identified a valid password using a password wordlist.
Response length, status codes, and error messages were useful indicators for identifying valid credentials.

Notes
This attack relies on the use of dictionary wordlists containing likely usernames and passwords.
Rather than trying every possible combination, a dictionary attack uses common or previously known credentials, making it more efficient.
The effectiveness of the attack depends heavily on the quality of the wordlists and the target application's authentication responses.

Remediation
Implement account lockout or temporary account suspension after a defined number of failed login attempts.
Use rate limiting to slow repeated authentication attempts.
Enforce strong password policies and encourage the use of password managers.
Implement multi-factor authentication (MFA).
Ensure authentication error messages are generic and do not reveal whether the username or password is incorrect.
Monitor and alert on excessive failed login attempts.
Consider CAPTCHA or equivalent bot-detection mechanisms after multiple failures.


References
OWASP Authentication Cheat Sheet
OWASP Brute Force Attack Guidelines
