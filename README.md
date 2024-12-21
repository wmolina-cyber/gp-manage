# Active Directory Lab: Part 4  
## Account Lockouts, Enabling/Disabling Accounts, and Observing Logs  

### Overview  
In this final part of the lab, I simulated account lockouts, configured Group Policy for lockout thresholds, managed user account states, and explored system logs on both the Domain Controller and Client Machine. This exercise reinforced critical skills in managing and securing Active Directory environments.  

---

### Steps Performed  

#### 1. Simulating Account Lockouts  
- Turned on **DC-1** and **Client-1** VMs in the Azure Portal.  
- Logged into **DC-1** as `mydomain.com\jane_admin`.  
- Selected a random user account created previously.  
- Attempted to log in with the account 10 times using an incorrect password.  

**Screenshot Placeholder: Account Lockout Error Message**  

#### 2. Configuring Group Policy for Account Lockout Thresholds  
- Opened **Group Policy Management** on **DC-1**.  
- Configured the **Account Lockout Threshold** policy to lock accounts after 5 failed login attempts.  
- Attempted to log into the same user account 6 times with an incorrect password to trigger the lockout.  
- Verified that the account was locked in **Active Directory Users and Computers (ADUC)**.  

**Screenshot Placeholder: Group Policy Configuration for Account Lockout**  
**Screenshot Placeholder: Locked-Out Account in ADUC**  

#### 3. Unlocking the Account and Resetting the Password  
- Unlocked the locked-out account in **ADUC**.  
- Reset the password for the account.  
- Successfully logged into the account with the new password.  

**Screenshot Placeholder: Unlock Account and Reset Password Process**  

#### 4. Enabling and Disabling Accounts  
- Disabled the same account in **ADUC**.  
- Attempted to log into the disabled account and observed the error message.  
- Re-enabled the account in **ADUC** and verified successful login.  

**Screenshot Placeholder: Disabled Account in ADUC**  
**Screenshot Placeholder: Error Message for Disabled Account Login**  
**Screenshot Placeholder: Re-Enabled Account and Successful Login**  

#### 5. Observing System Logs  
- Examined security logs on the **Domain Controller (DC-1)** to track account lockout and login activities.  
- Observed login failure and account lockout events on **Client-1** using the Event Viewer.  

**Screenshot Placeholder: Security Logs on DC-1**  
**Screenshot Placeholder: Event Viewer Logs on Client-1**  

---

### Conclusion  
This lab provided practical experience with critical Active Directory management tasks. By simulating account lockouts, configuring lockout thresholds, managing account states, and analyzing logs, I deepened my understanding of Active Directory's security and troubleshooting mechanisms. These skills are essential for maintaining a secure and functional domain environment.  

The lab VMs were stopped in the Azure Portal to conserve costs but not deleted, ensuring they remain available for future exploration.  
