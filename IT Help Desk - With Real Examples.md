# Troubleshooting Methodology

<img width="1121" height="602" alt="Screenshot 2025-08-18 235011" src="https://github.com/user-attachments/assets/af964a79-9cab-4dc2-8d84-f9dba24b2cf5" />


<img width="843" height="452" alt="image" src="https://github.com/user-attachments/assets/a4f3d1b1-e9e3-488d-8f93-6eaaa3ff8832" />



<img width="824" height="452" alt="image" src="https://github.com/user-attachments/assets/84d127c1-ad32-4eb0-ae93-c2bce0ce238f" />


<img width="838" height="450" alt="image" src="https://github.com/user-attachments/assets/2525dd11-bf8d-451c-b222-9553e67b355e" />


<img width="824" height="351" alt="image" src="https://github.com/user-attachments/assets/400f28bc-f73a-43fe-aea5-f2624700d9f1" />



# Join A Device to a Domain

<img width="902" height="714" alt="image" src="https://github.com/user-attachments/assets/715ea05d-e987-4885-b4b6-3dded48b85da" />


>> Computers are usually managed centrally using a system called Active Directory, and when you join a machine to the domain, it can be centrally managed by it.


>> Users can log in with their domain credentials.


>> Group policies can be applied to control settings and security, and it also helps with device tracking, updates, and access control.



>> It can also help the user do things like connect to local shares that are set up on file servers, and sign in using their single sign on to various applications.


**As a helpdesk technician, you may be asked to do this when setting up a new device or when joining a machine that was removed from the domain.**


**Troubleshooting:**
1. Make sure you have the domain name

2. The computer needs to be connected to the corporate network. Somewhere where it can talk to the AD server:
   Open up a command prompt to see if we can ping ADFS- that's the same of the Active     Directory server.

3. The username and password of the domain account with permissions to join computers to the domain is also needed.
   When prompter, we can just get Sarah to eneter in her credentials.


4. The computer also has to have a unique name on the network:

   To join a machine to the domain, simple type "Domain". The one that we want is the "Access work or school":

   <img width="830" height="478" alt="image" src="https://github.com/user-attachments/assets/4fd58bd2-2ee1-4fbb-a908-c3bd0d1cec2c" />


   
<img width="431" height="232" alt="image" src="https://github.com/user-attachments/assets/67322929-d2d1-453f-a027-44f9e9aeac59" />


<img width="176" height="162" alt="image" src="https://github.com/user-attachments/assets/07bf9cbd-dd2a-4f08-b793-bf310f4441ce" />


<img width="382" height="151" alt="image" src="https://github.com/user-attachments/assets/ca0159a1-9377-49bd-9545-fae5ac6f7366" />


<img width="777" height="443" alt="image" src="https://github.com/user-attachments/assets/a95d5e48-b75c-4564-ae55-aea867ed8144" />


<img width="709" height="420" alt="image" src="https://github.com/user-
attachments/assets/f22f50f8-a38b-459e-b376-19fba1f819c4" />



<img width="653" height="458" alt="image" src="https://github.com/user-attachments/assets/ae4dee06-7835-4d3c-b16b-11e0a9c20a75" />


>> If the computer can't contact the domain controller, we won't be able to join it.


>> The DNS server have to be pointed to the domain controller as well.


>> You might have account permissions, so make sure the account you're using has rights to join the domain.


>> If a device has a duplicate name, for example this one was removed previously and it's never been celaned up, you might have issues joining it again.



# Locked Account and Forgotten Password

**Scenario:**

Imagine we're sitting in the IT area at work, working away and all of a sudden Bruce from accounting walks on up and says that recently he was prompted to change his password. He changed it, but now when he goes to log in, he thinks he may have forgotten it because when he types in what he thinks it is, it failed a few times and now it keeps coming up with a message saying that Bruce is locked out.

**Explanation:**

In Active Directory environments there is typically a group policy called the **default domain policy**. It dictates how many times a user can try to log in before the account gets locked out.

A really important thing with this is it also sets parameters like the required password length, how ofthen we have to change our password, and then once we change them, how frequently we can change them again.


**Troubelshooting:**

> We open up server manager, go to Tools > Active Direcory users and computers

<img width="1422" height="627" alt="image" src="https://github.com/user-attachments/assets/daf89fee-5776-43ef-9f49-aeb2c59de38c" />


<img width="486" height="302" alt="image" src="https://github.com/user-attachments/assets/7ff07e70-ab48-4bba-9ed5-ea84b89c8c4e" />


<img width="287" height="221" alt="image" src="https://github.com/user-attachments/assets/0394e40d-bc64-450b-bcba-158475e16467" />


<img width="886" height="543" alt="image" src="https://github.com/user-attachments/assets/08c463b3-dac7-48c1-9d61-faeabca9cd38" />



**Few security tips when it comes to changing passwords**

>> If we ever get someone call us remotely, say we're working on the service desk, it's probably your company's policy to verify the user before giving and changing passwords.


>> There's also best practices you can set up, like multifactor authentication (MFA) and self-service password reset, where users can change their own passwords by verifying. It's the by putting in things like their mobile number and then it provide them a text message and putting in other things as well, like security questions.


**Remember, the main thing here is always ensure that you're verifying users before changing their passwords. Because it not, you are running the risk of potentially giving the passwords to a malicious actor who's calling up and using social engineering to try and trick the helpdesk into resetting a password of a user so they can breach their account.**




# Office 365 MFA Setup
