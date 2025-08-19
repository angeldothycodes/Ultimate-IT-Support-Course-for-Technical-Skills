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

How you could walk through a new user logging in for the first time to their Office 365 account.

> Once an administrator has set up an account, you're going to go ahead and log into **login.microsoftonline.com**. You can also browse to **portal.office.com** and you're going to put in their username.

> More than likely, they would have gotten their username and password in an email, or they would have gotten it handed to them by a helpdesk agent or maybe even their manager.


<img width="552" height="507" alt="image" src="https://github.com/user-attachments/assets/2ed74780-84f5-4b74-b5de-d76fa612b558" />


<img width="620" height="477" alt="image" src="https://github.com/user-attachments/assets/c279031e-bbc9-47ff-b4b5-f5bf7111c715" />


<img width="549" height="476" alt="image" src="https://github.com/user-attachments/assets/01df57e1-fa74-41a7-8c8e-18140ee15a4c" />


<img width="1384" height="646" alt="image" src="https://github.com/user-attachments/assets/c8316fb3-88bb-4f10-9fea-2510d588954b" />


<img width="476" height="358" alt="image" src="https://github.com/user-attachments/assets/8ea4a710-a3ac-4353-b395-c3ccdc347b80" />


<img width="452" height="248" alt="image" src="https://github.com/user-attachments/assets/0ecc78ec-22c1-43d7-8960-5e0ec3942672" />


<img width="775" height="444" alt="image" src="https://github.com/user-attachments/assets/033926e2-4d8e-4353-a27e-4cbaa99e1988" />




# Cannot Access File Share Folders

**ISSUE:**
Let's take a look about a very common issue that confronts the help desk frequently. And that's permission issues when it comes to folders and files.

<img width="874" height="635" alt="image" src="https://github.com/user-attachments/assets/0aa258d9-1088-48f4-b01a-9d4994c14bd0" />


We are remoted onto his machine, he opened up his File Explorer. We can see that he has browsed to the File server in the nvironment, and there is a folder called **projects** but when he double-click on it, this is the error he gets:

<img width="1275" height="682" alt="image" src="https://github.com/user-attachments/assets/8e19113a-5d65-46f2-b680-9f28474f5568" />

> As far as we've been told so far, it's not a problem with everyone. It's just particularly Bruce that's having the problem. It's a good thing to check off our list that the server is up, we can remote onto it, we can access that folder. So there must be particularly wrong with Bruce's account or his permissions.


**TROUBLESHOOTING:**

Head on over to our Active Directory server:

> Let's open up server manager to begin.


> When we're in server manager for any file servers, there is going to be a role called **"file and storage services"**. 

<img width="1143" height="607" alt="image" src="https://github.com/user-attachments/assets/55612b51-4352-420f-8360-2d14cf88560a" />

> Navigate to **"file and storage services"** and navigate to the shares. This is going to show all the shares the are currently exist on that system.

<img width="940" height="492" alt="image" src="https://github.com/user-attachments/assets/7ec13f59-d8cb-4b1d-b7b0-24d65383049b" />

> We can see there is one called **"projects"**. The actual folder itself is located in the C:\projects. Now, typically in a real environment, you probably would not have the shared drives on the C:\ volume. You would create dedicated disks or dedicated raids for them.

<img width="860" height="479" alt="image" src="https://github.com/user-attachments/assets/9a26c173-98e8-4b7a-95f0-cb850024dd32" />



> We can right click on the share and go to properties. 

<img width="808" height="555" alt="image" src="https://github.com/user-attachments/assets/b2715cfd-8183-4eb8-95bc-4dd256334202" />

> Then go to "Permissions" > Customize permissions

<img width="965" height="631" alt="image" src="https://github.com/user-attachments/assets/aa94091c-4508-482b-a644-0ef325bb753c" />


> Who has access? Administrators, the system, the creator have full control.


> There's a security group called "Projects_ReadWrite" that has modify access.


<img width="1113" height="751" alt="image" src="https://github.com/user-attachments/assets/be518849-a6d7-4503-aa6f-5c654fcb0793" />


> In Windows, you can go to Effective Access tab. Not a lot of people use it. "Select a user" in our domain


<img width="699" height="511" alt="image" src="https://github.com/user-attachments/assets/0d332ad6-7b9c-436c-aaf7-e3d855d833ab" />


> We can go check Bruce. We've got Bruce at the empty lot local. 

<img width="376" height="258" alt="image" src="https://github.com/user-attachments/assets/0e5a0440-a9f5-451a-9de6-d8eb4cdc6bd9" />

> We'll go ahead and view his effective access


<img width="665" height="444" alt="image" src="https://github.com/user-attachments/assets/ae5e0529-c230-42a3-a983-8fbf356d7aa1" />


> We can see that Bruce has absolutely no access. No read, no list, no full control, no delete, no read, nothing to this folder.

<img width="556" height="282" alt="image" src="https://github.com/user-attachments/assets/54d0437c-3a86-4973-95ea-6cf138ed66f5" />

