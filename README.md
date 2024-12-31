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
![20](https://github.com/user-attachments/assets/16b05848-17a3-4549-afdd-f7d05c6bffbe)

#### 2. Configuring Group Policy for Account Lockout Thresholds  
- Opened **Group Policy Management** on **DC-1**.  
- Configured the **Account Lockout Threshold** policy to lock accounts after 5 failed login attempts.
![8](https://github.com/user-attachments/assets/28f36407-2600-4540-94d9-cdded7c65bcb)
- Attempted to log into the same user account 6 times with an incorrect password to trigger the lockout.  
- Verified that the account was locked in **Active Directory Users and Computers (ADUC)**.  
![25](https://github.com/user-attachments/assets/6d6999ac-d046-43c2-ace4-9d08cb1f36fb)


#### 3. Unlocking the Account and Resetting the Password  
- Unlocked the locked-out account in **ADUC**.  
- Reset the password for the account.  
- Successfully logged into the account with the new password.  
![30](https://github.com/user-attachments/assets/982edfeb-2b3d-4253-9f8d-598d282b954b)

#### 4. Enabling and Disabling Accounts  
- Disabled the same account in **ADUC**.
![32](https://github.com/user-attachments/assets/fc42c049-a522-47de-a05e-f812c7541f35)
- Attempted to log into the disabled account and observed the error message.
![36](https://github.com/user-attachments/assets/e0deac8e-94cd-450a-96de-894295a764ba)
- Re-enabled the account in **ADUC** and verified successful login.  
![38](https://github.com/user-attachments/assets/6547cc69-bca1-4394-ac55-91eafa7977df)
![40](https://github.com/user-attachments/assets/eb7256a7-9632-4931-a964-a78fd596e1e8)

#### 5. Observing System Logs  
- Examined security logs on the **Domain Controller (DC-1)** to track account lockout and login activities.  
- Observed login failure and account lockout events on **Client-1** using the Event Viewer.  
![45](https://github.com/user-attachments/assets/4953cb2b-4258-4aa0-a6e1-c0c85b215d79)

---

### Conclusion  
This lab provided practical experience with critical Active Directory management tasks. By simulating account lockouts, configuring lockout thresholds, managing account states, and analyzing logs, I deepened my understanding of Active Directory's security and troubleshooting mechanisms. These skills are essential for maintaining a secure and functional domain environment.  

