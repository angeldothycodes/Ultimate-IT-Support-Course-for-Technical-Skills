<img width="961" height="680" alt="image" src="https://github.com/user-attachments/assets/15c3c617-ccad-44a6-87bd-49ef87231778" /># Troubleshooting Methodology

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


> We can see that Bruce has absolutely no access. No read, no list, no full control, no delete, no read, nothing to this folder. That must mean that in the permissions, he is not added.

<img width="556" height="282" alt="image" src="https://github.com/user-attachments/assets/54d0437c-3a86-4973-95ea-6cf138ed66f5" />


> Let's go and have a look at this group:

<img width="566" height="220" alt="image" src="https://github.com/user-attachments/assets/e177be53-aedf-4a0d-81d6-2d61ae0eee27" />


<img width="921" height="363" alt="image" src="https://github.com/user-attachments/assets/e8659b00-ffd4-46b6-b561-b6f0b5dd51cd" />


<img width="309" height="366" alt="image" src="https://github.com/user-attachments/assets/56b9a08a-0be9-46b5-a68d-62a3fee4af8d" />

<img width="484" height="487" alt="image" src="https://github.com/user-attachments/assets/fdd4219b-7089-4a5e-9991-8595a16c6df3" />


<img width="849" height="518" alt="image" src="https://github.com/user-attachments/assets/5dc59129-56d3-45d9-b638-3b77852870eb" />


> We know that folder, that security group has modified permissions, that's probably the group that Bruce needs to be a part of. So we would go ahead and get permissions from whoever we need to in our organization. Whether that's we go to service desk manager or we go to Bruce's boss and we say, hey,do they have permissions? Whoever essentially is the owner of that folder and this security group, we need their permission to be able to add Bruce. They say, yes. that's absolutely fine. This is really urgent. Please get that done straight away.


> All we need to do now is go back into the properties of the group in Active Directory > click ADD. Put Bruce in there and click Apply.

<img width="339" height="371" alt="image" src="https://github.com/user-attachments/assets/b7919209-0843-49cd-b551-a1288d37249c" />


<img width="415" height="373" alt="image" src="https://github.com/user-attachments/assets/97fb8a30-a52c-40b7-bf39-0459c1fb24f7" />



<img width="367" height="221" alt="image" src="https://github.com/user-attachments/assets/c7fb462a-a321-4cce-91bb-bd80d9cddc59" />


<img width="371" height="385" alt="image" src="https://github.com/user-attachments/assets/be779f38-a296-49af-b6bb-f286fa30f825" />


> So now, we say Bruce we'e added ou to the projects read write group


> In instances when you double check the group, and there is still no permissions for that user, sometimes what you might need to do is get the user to sign out and sign back in in order for the permissions to be applied. It's not just enough to lock in. You either need to restart it or sign in and sign out.


# Onedrive and File Backups

When you're setting up OneDrive, there's a really important tip that a lot of people skip over and not really thinking about it but it's a really powerful feature:

When signed in to OneDrive, there is a "Back up folders on this PC". What you can set up with OneDrive by default, now is a backup of certain folders to go up to the cloud. That means for your users, if you backup the documents, pictures, and desktops to the cloud, for example, any documents that they store on there. Users are notorious for storing things in folders they shouldn't be like desktop. When you do this, it's going to back them up to that cloud environment. That means if their device goes and gets stolen or they corrupt the oprating system, a piece of hardware fails, they're not going to lose all their data because it will have been synced up to the Microsoft cloud. Then all they need to do when they get their new device is log in, put the username and password in, BAM! As longs as they've got access to their OneDrive account, they'll have access to all of their documents and pictures. This way, you can give users that peace of mind that as long as you're storing your data in the correct folders, typically it should be in places like SharePoint or OneDrive or the file server. But if they are storing them on documents, pictures, and desktops and you can enable music and videos.

<img width="516" height="482" alt="image" src="https://github.com/user-attachments/assets/602f8b40-71d8-4423-b86c-462cde7dbc2b" />




# Cannot Install Application

**SITUATION:**

I am trying to install a PDF reader onto my laptop, but it keeps asking for administrator permissions.



**TROUBLESHOOTING:**

A topic that every IT support professional needs to understand well. That's a User Access Control or UAC within Windows. It's a security feature that helps prevent unauthorized changes to the operating system. When a user or a program tries to make a chnage that requires admin privileges like installing software or changing system settings, UAC steps in and prompts for approval. This is done to protect the system from malware or accidental misconfiguration.

Without UAC, any malicious program that gets on a user's machine could potentially make system level changes without their knowledge. **UAC** helps limit the damage by ensuring those critical actions need admin approval first. 

So really in an environment, admin should be the only ones installing software. When users install software on their own, even with good intentions, it can introduce serious risks to the organzation from malware infections to slowing down systems when unnecessary apps. 


This is what UAC is:

<img width="347" height="429" alt="image" src="https://github.com/user-attachments/assets/424c215c-4c98-46bc-add0-9198934f8e8e" />

It lets us verify the publisher. It lets us look at where it's trying to install from. 



# Troubleshooting Group Policy Objects


<img width="371" height="332" alt="image" src="https://github.com/user-attachments/assets/993d8655-324a-4323-a3d5-975e028e335c" />

Typically in a lot of business environments, instead of installing software manually on every single device individually, we'll create something called a **Group Policy**.

**Group Policy** can do a lot of things. It can manage system settings, it can manage security settings. But one of the main reasons we use it is it can automate deployments of software out to various groups and users so we can separate based on the different types of users, what applications they get, and it can be installed automatically over the network.

We know for a fact that there is an Active Directory server with a group policy that deploys out the 3XC app.


**TROUBLESHOOTING:**

What we need to now go and do is troubleshoot why for some reason it's not installed on Billy's machine. So we'll dive into wherever our group policies are held. In our case, we know. Thanks to our documentation. It's on the AD server.

We're going to go to Tools > Group Policy Management

<img width="577" height="328" alt="image" src="https://github.com/user-attachments/assets/36d1c081-2387-4acf-9ce2-855109d09cf9" />


Now, we know that all of our computers are held in an OU called workstations. And look at that, there is a GPO called **deploy 3CX phone**

<img width="401" height="295" alt="image" src="https://github.com/user-attachments/assets/16d5ebc6-522c-4282-a8fa-134bc8191834" />


Going over to the settings > assigned applications. We can see that the 3CX phone we've got the deployment. and it is hosted on a shared file location:

<img width="559" height="320" alt="image" src="https://github.com/user-attachments/assets/9f18e461-bb7c-441c-810e-9e95139c3fd5" />


One of the first things we can test is does Billy's machine have access to that. Because you are going to need access in order to install it. So if we do ADFS backslash software, we can see it. That gives us a big check box.

<img width="968" height="427" alt="image" src="https://github.com/user-attachments/assets/4c4c0024-6fee-45cb-b991-c0c23db70a8a" />

Next, we need to check is if Billy actually supposed to get this. In server manager, go to Tools> Active Directory Users and Computers. From there we look into the **OU(Organizational Unit)**. Otherwise, we can always just right click and do a find and type in the PC name. From here, we can check and we can make sure that desktop does appear in that group.


Sometimes when machines have been offline for a little bit of time and not checking in with the network, they might be a little bit behind on policies. We can force a policy update by opening up command prompt and running **gpupdate /force**. You don't need to run this as administrator. By running that, it's going to reach out to the group policy server and pull all the latest updates.

This is the message displayed when gpupdate /force was executed:

<img width="798" height="559" alt="image" src="https://github.com/user-attachments/assets/da1ab1c2-f49a-46c7-9dc1-baf5e5030352" />

Essentially, this entire paragraph right here is just telling us reboot your machine and then the group policy will apply.


Also, quickly check that the security filter which is under scope has authenticated users apply. Essentially, all users are going to get that policy as long as they're contained within this **OU (Organizational Unit)**

<img width="844" height="592" alt="image" src="https://github.com/user-attachments/assets/65abd8cd-68f4-4ce3-8db9-de5767ccb75a" />



Back on Billy's PC, let's take a look to see if this has applied. Aside from GPupdate, you can also do **gpresult /r** command. This is going to let us know what policies a user is part of. 


One thing we can do as well while we're waiting is we can go ahead and jump into event viewer. Event viewer is a positive way to be able to see what the system is doing. In event viewer > Application event logs, we can see any softwares attempting to be deployed.



**NOTE:**

(After doing the troubleshooting above, 3cx got installed.)


<img width="572" height="478" alt="image" src="https://github.com/user-attachments/assets/a2af9273-6628-44c4-85ef-079a9b51a70c" />



For the most part this is a very automated process. We never have to get involved, but there are instances where new policies get created and a particular workstation hasn't been turned on in a while, so it has no way of getting those new policies until someone finally turns it on, maybe gives it a gpupdate /force and reboots it.



# Release and Renew IP Addresses

If users are having trouble connecting to the network, can't access the internet, or are having strange IP conflicts, the simple command line fix can often do the trick.

When your device connects to a network, it usually gets an IP address from a DHCP server that's often your router or a dedicated DHCP server in business environments.

Sometimes things go wrong. The lease expires, the lease gets stuck. You have an incorrect or outdated IP, maybe there's a conflict with another device, or you're just switching between networks.

By releasing the IP, you're telling the device to give up its current address, and by renewing it, you're asking the DHCP server for a brand new fresh one.

Some common situations when releasing and renewing helps is when a device has no internet access despite being connected.

If you're seeing 169.254 address, this means that Windows couldn't get one. 

You are changing networks or there's an IP address conflict.


**Here's what we need to do:**

<img width="1037" height="750" alt="image" src="https://github.com/user-attachments/assets/fd361cb0-dfdf-49c5-b086-6052ef50a0c5" />


Releasing and renewing your IP address clears out a bad or outdated address. It's useful for when users can't connect or they might have switched networks or see IP conflicts in their event viewer.




# The Dreaded - Blue Screen of Death (BSOD)


Let's now talk about resolving blue screen errors in Windows. Blue screen errors, also known as BSODs, can occur if a serious problem causes windows to shut down or restart unexpectedly.

To protect itself from data loss, you might see a message that says something along the lines of Windows has been shutdown to prevent damage to your computer or a similar message. Typically, it will also come with a code number, which you can stick into Google to get the exact reason, or atleast close enough as to why it is blue screening.

We have a couple of troubleshooting steps we want to follow to try and help the user out.

First of all, we need to find out if any new hardware has been added to the PC before the error. If so, we might want to try removing that hardware and see if it resolves the issue.

The hardware could be faulty or there could be a compatibility issue.

Another option is we might want to start our PC in safe mode. A good trick to that is if you hold down your shift key on your keyboard, click Start > Power button > click restart> all the while you've got to keep holding the shift button. Keep holding it. What it's going to do is start the PC in safemode. 

<img width="1119" height="722" alt="image" src="https://github.com/user-attachments/assets/e4046c21-d149-4225-93cb-560336d3a840" />



<img width="949" height="599" alt="image" src="https://github.com/user-attachments/assets/8a02682f-2596-45e3-a485-3b23e53c65d0" />



<img width="1029" height="692" alt="image" src="https://github.com/user-attachments/assets/e2be9fdc-9b59-41a5-9054-edc1c63d8f77" />


The **startup repair** is a super handy feature, and what it's going to do is run though a prebuilt check that Microsoft has to ensure that all the files are working correctly.

<img width="789" height="355" alt="image" src="https://github.com/user-attachments/assets/b0677ae7-0de7-4416-9829-cd940cf0ac51" />


While this is going through, it's going to go and try and diagnose and fix it.

<img width="772" height="599" alt="image" src="https://github.com/user-attachments/assets/ef9c2843-c2cc-4e7b-9d2b-d93a0d85d0da" />



Some other steps outside of the safemode options is we're going to want to check the **device manager**. Right-click start menu> click on Device Manager. Otherwise we can search for it in the search menu.


<img width="1078" height="665" alt="image" src="https://github.com/user-attachments/assets/887f5d46-8d1b-482e-b4c1-dbdf2a950ad0" />


We just want to see if any devices are marked with a yellow triangle or a red exclamation point which should show if they were. This could mean that, potentially, the device is corrupted or the driver is having some sort of issues, so we many need to update the driver, which we would do with right clicking and clicking update Driver.

<img width="529" height="536" alt="image" src="https://github.com/user-attachments/assets/b5e3a355-f1bd-4edc-b7fa-50e399cf2e87" />


We're going to want to check for sufficient free space on the hard drive. 

We are also going to check to see if any Windows update have installed recently. There have been issues in the past where an update has caused blue screens for whatever reasons. If we type in the word "Windows Update" settings, we can find "View your Update" history in the list.

<img width="651" height="576" alt="image" src="https://github.com/user-attachments/assets/8e1cb2e0-409f-46ea-9a09-41b5f8cce95b" />



We can see if any were installed and we can see there were a few installed today:

<img width="709" height="534" alt="image" src="https://github.com/user-attachments/assets/3af0483a-1cbc-4dda-9296-c4dd07d1eef5" />


What we would do is start going through the process of uninstalling those updates. From there, if hat still has not resolved the issues then what we can do is potentially move on to something like checking the event viewer so we can go into the event viewer of a system again.


From there, if that still has not resolved the issue, then what we can do is potentially move on to doing something like cheking the event viewer so we can go into the event viewer of a system again. See if there are any logs under the Windows Log system that tell us why the system is going ahead, and blue screening.


There's a few more advanced tools that we can run, like the Windows Memory Diagnostic Tool and the memory dump analysis. 


More often than not, it's going to be something like these updates or the startup repair that resolves.


**TO SUMMARIZE:**

> Remove any new hardware

> Start your PC in safe mode.

> Check the device manager, check for free space, check the latest updates

> If still having issues, dive into some advanced steps like checking the Event viewer, running the Windows Memory Diagnostics tool, or looking at a memory dump analysis





# SLOW INTERNET


Our goal is to identify whether the problem is on the device, the local network, or with the wider internet connection.


First part is triage right. We need to ask some questions to understand the scope.


Imagine we got a call on the help desk and it's a user complaining that the internet is running very slow today. It's affecting things like they're not able to check their emails regularly. Web pages are timing out. Overall, the internet just feels sluggish.

The first things you really need to determine is, is this slowness affecting just them or everyone?

Let's say we are remoted onto the user's machine. What we can do is load up internet browsser and find an online speed test tool. We know for a fact based on documentation that this site has 100 megabits internet.



<img width="718" height="451" alt="image" src="https://github.com/user-attachments/assets/eec599c9-6613-4946-8c86-7d8cdf1f6c48" />



It seems like this user is capped at about nine megabits for some reason. It just doesn't seem to be getting any faster. The question that you should start thinking is if it just this user's device or is it everyone. You could ask them to maybe check with the person to their left or to their right to run the speed test. Or if we know that there's a server in the environment, we're going to jump onto the AD server that's at the same office, we can run a speed there.


<img width="795" height="868" alt="image" src="https://github.com/user-attachments/assets/a35b0155-f0a5-4596-9ee3-a420b631dedb" />



AD server is getting around 80 to 90 mbps. The AD server is in the same office using the same internet connection. It tells me that this slowness is not just affecting the internet line, it's potentially just affecting our one client here, this one user.


**TROUBLESHOOTING:**

You could also go and check things like is it only happening with specific websites or applications? Start asking questions like when did the issue start and has anything changed recently? That's a really important one because if you know, they start talking about how they move desks or something, we can start thinking, okay, well, maybe the cable is faulty. Those types of thought patterns. Another really important thing is to determine are they connected to Wifi or are they on Ethernet?


<img width="422" height="360" alt="image" src="https://github.com/user-attachments/assets/c7753d8a-ca57-4f3f-b567-650c4baaedd5" />


In our case, we can see they are cnnected to Ethernet thanks to the little computer symbol down in the bottom right hand corner here. If it was Wi-Fi, they ould appeear to be a Wi-Fi symbol


Typical IT stuff, have you tried turning it off and on again? Ttypically one of the most common tools is to just give the machine a very quick reboot.

One reboot is done, open up the browser and go to and do Speed Test. If that didn't resolve the issue, look at the task manager and go to performance tab.


**Saw that the CPU is not overloaded, the memory too is sitting at quite a steady level. The disk is not being overloaded and the Ethernet too is looking fine.

** Needs to start diagnosing and diving into the root cause.

Try going to device manager as an administrator:

1. Open CMD as admin
2. Type devmgmt.msc
3. This will log you in device manager as an administrator



<img width="474" height="414" alt="image" src="https://github.com/user-attachments/assets/c917ef11-8ae0-4d12-bb02-2fc0ac6319d3" />



Take a look at network adapters, we know they are using the Ethernet connection which is the Intel 82574L Gigabit connection. Right click on it > Properties > Advanced > Speed & Duplex. Make sure that the speed and duplex is set correctly. Right now, it's set to auto-negotiate. Let's set it to 1.0 Gbps Full Duplex.

While you are on the Device manager, you can also update the driver. Right click > update driver.

After that do another speed test. (The speedtest resulted to increase speed)


<img width="711" height="524" alt="image" src="https://github.com/user-attachments/assets/a690c703-4125-47da-b462-4d1c35b1acad" />


**NOTE:**
You've got to think to yourself that when we're doing things within here, this is the software that controls the hardware. If it's out of date, if it's got problems, if it's got bugs in the current version, it can cause a whole manner of issues, including slow internet speeds.


By following the steps that I've shown you, you'll be able to diagnose and solve most slow internet complaints or get them escalated properly.






# Remote Site - Internet Down!

It was slow all morning but now we cannot load anything at all. It's really affecting our ability to work.

One of the first things you're going to need to do on the help desk is understand the impact.

There have been calls to the help desk claiming that the internet is down and at the end of the day all taht's happened is Facebook is having some massive outage but to them that's the whole internet.

There have been sitauations where the internet is down, but in reality all it is is people can't connect to the Wifi.



<img width="1788" height="778" alt="image" src="https://github.com/user-attachments/assets/7727ccd0-476f-4c5b-ba7a-ea6679269476" />




So you need to start asking those probing questions to get a real good understanding of is everyone affected in the office or is it just individual or maybe just multiple users?

Can they reach internal systems or just not external webistes? 

Are cloud apps like Microsoft 365 loading for them or not?

This is going to be your triage process to be able to really understand where the impact is.

Let's say the documentation for this site states that is a small star, only about 4 to 5 users.

They've got a pretty cool standard Asus router out there with an ISP with a fixed line, and you've checked the ISP status page. They're not showing any outages.


You've jumped on your remote tool, and you cannot remote into any of these devices at that site. It's starting to look that the internet is actually down at the site.

We need to guide them towards checking out the network equipment. We're going to get them to probe the network, maybe just go through a few simple steps like checking on the router.


1. First thing we're gonna do is we're going to let them go over and check on the router.

<img width="600" height="729" alt="image" src="https://github.com/user-attachments/assets/5beb25f0-09bd-4132-a5d8-56d58e94ac33" />



We can see that there is a power line, but all the other lights are currently off.



<img width="748" height="676" alt="image" src="https://github.com/user-attachments/assets/a602e2d6-df3d-4a2f-a3d1-9061832cf1ac" />


The internet line is currently showing no connection.


We can get them to check that all the cables are securely fastened at the back. We can get them to check that the internet service provider is not reporting any outages in the area. Typically, a lot of ISP will have some sort of status page.


If all else fails and the internet is still not working, then what we can do is at the back here there is a little power button that we can turn off and turn back on again. Let's see if the internet reconnects.


Typically for remote sites who have business grade routers such as this, that might be okay. But for enterprise grade routers, we may not want to reboot them because the boot times can be upwards in the 5 to 10 minutes, and sometimes they have proper shutdown procedures.


For example, in the case of firewalls, a lot of them have proper shutdown procedures that need to be followed. For consumer grade routers like this and business grade routers, it should be fine.



<img width="885" height="493" alt="image" src="https://github.com/user-attachments/assets/c80f8fe8-a9bc-4601-9098-220057d46fbe" />




# Printer Issue

A user raised an issue saying they are not able to print. At the moment what they're trying to print is extremely important. 


**TROUBLESHOOTING:**

We are going to do is we're going to head an over to the settings. Open up **printers & scanners**

<img width="812" height="499" alt="image" src="https://github.com/user-attachments/assets/57e5635e-3b88-4f85-a1f0-552125a5895f" />



<img width="849" height="576" alt="image" src="https://github.com/user-attachments/assets/c708ee67-20f7-4cb2-af7a-bbf8423ce8fa" />



<img width="679" height="458" alt="image" src="https://github.com/user-attachments/assets/96a41830-b182-45e2-abea-7552c9978b52" />


We can see they are connected to the printer Canon TS3400. We can look at the print queue- it's empty.

We can print a test page just to see if it's maybe the document the user's tryign to print or if it's actually something going wrong with thr printer itself.



<img width="667" height="550" alt="image" src="https://github.com/user-attachments/assets/9454d779-a536-4173-883a-6861f26e51d9" />


We can run the troubleshooter. This is a Windows built-in troubleshooter that's going to try and fix issues.


Printers often have web interfaces, you can jump in there and let you know if it's got an issue that it's letting you know about.


Let's head back to the printer and it's telling us exactly what the problem is.


<img width="781" height="548" alt="image" src="https://github.com/user-attachments/assets/73a2c8bc-f6d3-4222-b32c-d7740c5f4568" />


When we tried to print out a test page earlier, it is telling us about what the exact error is. The trubleshooter told us the same thing as well as the little windows notifications. The printer is out of paper and it's telling us exactly how to fix it.



# Display Issues

A really common issue when it comes to either new computers or new docks or new monitors is people having issues with their displays. They may have issues like no signal to monitor. They may have something like what we're seeing right here, where the window is really small or really fuzzy. 


<img width="538" height="386" alt="image" src="https://github.com/user-attachments/assets/5d884ffb-64a3-4205-a6f4-1cf7789b203c" />



One of the best ways to troubelshoot these sorts of issues is to right click anywhere on the desktop and go into Display settings:

<img width="554" height="425" alt="image" src="https://github.com/user-attachments/assets/1b49ebce-fa41-4f76-bcd2-a9a7d1eff1ec" />


Scrolling down, we can see that currently the display resolution is set at the absolute minimum - 800x600


What we need to do is determine the best aspect ratio of this monitor, and then change the settings to meet the requirements of that monitor.


This is also where you can go if you have multiple displays. You can move them around in order to fix up how the displays are showing.


Some people as well may have this flip to portrait for whatever reason.



# Sound Issues

**Caller:**

I got a new laptop yesterday and this morning when I tried to jump into a video meeting with my team, I couldn;t hear them and had to drop out of the call. Can you help me as no sound is coming from my laptop at all?



It sound like there is potentially a sound problem with the laptop.


<img width="676" height="561" alt="image" src="https://github.com/user-attachments/assets/1b95e3a4-9fb0-46a2-a3ec-e13cb117b42c" />


Right away we notice down in the bottom right hand corner there is a little audio symbol and it's got a red cross next to it. Whenever we see a red cross or a red triangle, that's always BAD NEWS.


Right now, one of the cool things that we can do is we can actually right-click on this and click "troubleshoot sound problems"


<img width="763" height="562" alt="image" src="https://github.com/user-attachments/assets/c2f6695b-6cb5-429c-baec-4305c82425f1" />


What it's going to do is check few of the basics in the background to make sure that everything is okay with this machine because we could have a hardware error. It could be something wrong with the sound card or the sound chip in the machine.

It could also be something incredibly simple, like we're missing the drivers for the machine or for the hardware.

It could be that potentially something wasn't completed properly upon install. 



<img width="677" height="461" alt="image" src="https://github.com/user-attachments/assets/3a9108a3-152f-41a4-a506-f0e0b4b7a022" />


Upon finishing the installation by double-clicking the result above, it showed this:

<img width="471" height="363" alt="image" src="https://github.com/user-attachments/assets/c5684c86-ed51-4067-b45e-1a01497aa9c8" />



**After the restart, the audio is still showing the little red x mark down here:

<img width="518" height="313" alt="image" src="https://github.com/user-attachments/assets/0068525c-ea29-4a82-a1d8-9178f53951e5" />



Let's see if we can fix this manually:


<img width="847" height="710" alt="image" src="https://github.com/user-attachments/assets/a340b041-a9a8-4c72-af6a-f4aee9965dc4" />


The high definition audio device is currently showing a down arrow which means it's disabled. Let's enable it to see if it fixes the issue.

<img width="467" height="340" alt="image" src="https://github.com/user-attachments/assets/4eb28418-094a-4cb7-8a1d-c1bfa2f14424" />


Remember, I had to do this as an administrator account. Remember you can't do anyhting in Device Manager as a standard user. You have to log in with someone as a domain admin.



# Slow Loading Applications / Slow PC Troubleshooting



**ISSUE/TICKET:**

Hey, it's Derek over at project Deliverables here. My computer is crazy slow today. Every application is taking a minute or two to load. Fies won't open correctly and I can barely get any work done. I have a presentation to the board coming up so I really need you to fix it as soon as possible.


**DISCUSSION:**

In this lesson, we're going to walk through how to investigae and troubleshoot a slow PC. 

When a user calls in and says "my computer is running really slow." It can mean a number of things. 

As helpdesk professionals, our job is to ask the right questions, run some basic, and identify whether the issue is performace related, software related, or even user related. 

**Right questions to ask:**

- When did the slowness start?

- Is it slow all the time or only during certain tasks?

- Is it specific to one application or the whole system?

- Have there been any recent changes or updates lately and are they working locally or remotely?


Document all of your findings into your ticket because the more context you gather, the faster you're going to be able to find the root cause.


**TROUBLESHOOTING:**

1. Check the Task Manager. We can see that this machine is getting heavily hit in the CPU


<img width="1063" height="789" alt="image" src="https://github.com/user-attachments/assets/9b36a494-61d5-4db5-8597-d387b7e70f2a" />

Straight away, we know there is something wrong with this machine that we are hitting 100% CPU utilization.


If we head over to Processes and sort the columns to see the exact processes using up all the memory. 

In Task Manager, we have the ability to track CPU, memory, disk, and network.


<img width="496" height="387" alt="image" src="https://github.com/user-attachments/assets/3134e7ca-5d62-4d35-ba83-90c678b249a8" />



We can see that Microsoft Edge right here is using 99% of CPU. Clearly, something is going wrong with this program.



<img width="715" height="516" alt="image" src="https://github.com/user-attachments/assets/fbf7b777-1bd3-4dfd-af96-496c5f5de631" />

What happens if we close it? After we issued the end task, let's head back to the performance graph. Straight away we see a massive reduction in the amount of processes and processor power that this machine is using.


We can go and ask Derek to try a couple of applications out to see if computer is more responsive.

**Derek opened Adobe Acrobat and opened Edge- it opened immediately.

So now we know that the culprit was Microsoft edge. Then we can start doing some investigation as to what they were looking at in their browser and what may have been causing that.

It's not always as straightforward as this. Sometimes, we have to dive deeper to find the root cause.

For example, we might want to run a quick malware check. Malware of unwanted software is a common cause of slow performance on machines, so there's nothing wrng with jumping into the security center, clicking on virus and threat protection, and just doing a quick scan.

<img width="868" height="453" alt="image" src="https://github.com/user-attachments/assets/dfde1402-1ef7-4bc1-825e-4085e65764c2" />

<img width="679" height="331" alt="image" src="https://github.com/user-attachments/assets/e4f1a650-6943-4f7f-94cd-9d6358eba753" />



There's also some time to maybe do some light optimization while this is running. You can clean up temporary files using disk cleanup or storage centers. If we go to the start menu and we just type in the word cleanup, we can open up the disk cleanup utility here. We can clean out anything that might be lingering.


<img width="672" height="518" alt="image" src="https://github.com/user-attachments/assets/a2a48f3c-0ac1-4604-a820-4c30caa50762" />



<img width="992" height="693" alt="image" src="https://github.com/user-attachments/assets/9ac06231-5611-40d5-a066-166215dfba9b" />


By default, we can see what it's able to clear. We can tick all the boxes and click Okay.


<img width="1044" height="794" alt="image" src="https://github.com/user-attachments/assets/ee75828b-f244-4a76-88e4-890163ab9531" />


<img width="754" height="630" alt="image" src="https://github.com/user-attachments/assets/84e77a7c-3823-41d9-98f8-31157db1b556" />


Otherwise if we wanted to dive deeper into the system, we need administrative rights which we'll put in. This is going to allow us to clean up even more system files that are no longer needed. Things like old update files, the recycle bin delivery optimization files.


We might want to go and uninstall unused programs in the program center. Head on into the control panel and head on to uninstall a program.

If there's a hard drive on the machine we might start looking at defragmenting it. These days most people have SSDs.


Another thing we can look at is running Windows and driver updates. We can also look at checking for hardware issues. We may run a memory test, or we may check the status of the hard drive.


<img width="647" height="363" alt="image" src="https://github.com/user-attachments/assets/0278d04f-0f2c-48f1-92b3-9efe34d69f7d" />


A really good command to check hard drive status is if we open CMD, we can run wmic diskdrive get status. It is going to tell us if the status of the hard drive or the SSD is okay.



We may even need to consider hardware upgrades in the most extreme cases. If this still had a hard disk in it, we might want to look at putting in an SSD. If we had maybe less than eight GB of RAM, we could look at upgrading that, or if potentially, the CPU is quite old as well.



Modern operating systems do use a lot more resources because thay're doing a lot more in the background. So we're always going to make sure our machines are specked out adequately.




The most improtant things is always update the ticket with the user's description of the problem, what checks you've performed, and any changes you've made. If you do manage to resolve the issue, what the final resolution was or if you need to escalate the ticket.



# Using an Emulator When You're Unfamiliar with an Operating System

As an IT professional, you'll often encounter operating systems that you don't work with everyday. Maybe a user calls in using the latest iPhone that you haven't had a chance to play around with yet.

Or maybe they're calling in with a browser tha you don't typically use. In these cases, that's where emulators can really help us out.


CHASMS emulator. The whole idea behind it is it provides IT professionals an emulation platform for you to be able to go out and test and try and even walk users through issues that you may not have a lot of experience with.

CHasms is a web-based OS emulator that runs various Linux distriutions, desktop environments, browsers, etc. It's free, it's fast, and it's perfect for practice or quick troubleshooting.


<img width="661" height="359" alt="image" src="https://github.com/user-attachments/assets/6d42d09a-51bf-4140-aedf-3f5d6dd740e2" />



# Hard Drive Disk Space Issues

Whethere you're supporting a small office or large organization, running low on disk space can lead to performance issues, failed updates, and in some cases, complete system failure.

Applications are crashing, or they're seeing warning messages from Windows saying something like you are running low on disk space.

You might even hear complaints that they can't save new files or install software. 

1. Access the machine and check for available space. The quickest way to do that is open up the File Explorer.

<img width="1288" height="747" alt="image" src="https://github.com/user-attachments/assets/c2ed510f-ad24-4f2b-9d4d-1d8fae66fbf4" />

We can see that in this computer it's only got abut  6GB free of the hard disk. That immediately raises some red flags.


2. Now that we know the issues and that we understand it, we need to start looking at cleaning it up and identifying what's taking up the space. Disk cleanup is a handy tool. It can be run as a non-administrator but it's only going to be able to cleanup some directories. As an adminstrator, you can cleanup system files as well. It will pull C: drive and give us a list of what files are no longer needed by the system. There are cases where it can clear up a lot of data. Cases where machines hold on to 10GB of old update files that they no longer need.

<img width="961" height="680" alt="image" src="https://github.com/user-attachments/assets/e1e4a91f-7d64-4b0f-b775-03d048b6e992" />


3. In this case, only 1GB of system files got cleaned up. We really need to start identifying what's taking up space. You can use some 3rd party tools. There are PowerShell scripts available as well, but the 3rd party tools in my experience are pretty much easier and create a visual map of what folders and files are taking up the most space. **Windirstat**. If we double-click on it, we can choose to scan all of our drives. It's going to go through and start giving us a really nice visual map of what is using the most data on this system. If it is run as a standard user, it has limited scope that it can scan.



<img width="1180" height="740" alt="image" src="https://github.com/user-attachments/assets/387a4242-2e81-4416-a797-c0a7c78be4d2" />

A standard user can't look through all the directries of the other users who may have used this machine. 

If we run this as administrator, we should be able to see al the other user profiles.


<img width="1505" height="705" alt="image" src="https://github.com/user-attachments/assets/f2724d34-0054-4959-baa9-69106c9047fa" />

It's telling us that 45% of the disks is someone under the Users drive. In windows, each user that signs in gets their home directory- the download folder, desktop, documents, pictures, videos, etc.

Every user that signs in that will stay there forever unless cleaned up.


<img width="716" height="272" alt="image" src="https://github.com/user-attachments/assets/16947f46-5d97-4895-acfd-900150cd7136" />


There is a user called Robert that is using 25GB of space in the user's Robert downloads folder. We can chat Robert if they still exist at the company to offer backing up his data or moving it onto OneDrive or SharePoint or something to clean it off of the PC. 


Moving forward, we're going to want to encourage our users to save any large personal files like videos or photos to some soft of cloud storage or the file server and not individual computers because we could end up filling up the drives.

It important to educate users, encoruage them to do regular cleanups, to move old files off the system, and always be mindful what they're downloading and what they're installing.


As a helpdesk professional, your job isn't just to fix the problem, it's to prevent it from happening again.



# Virus/Malware on a Device


**SCENARIO:**

A panieked call from our user who claim thatt hey were browsing a shoe store website. In doing so, they may have accidentally clicked something and downloaded a virus.


**DISCUSSION:**

First things first, we really need to talk about an important part of your role in the help desk- that's Incident Response. 

Specifically, when a user contacts you and thinks that they may have done something to compromise the security of their machine- stay calm and professional.

The user is already stressed out as you hear in their voice, and your job is to guide them step by step with confidence.

If they hear you panic, they're going to panic and then no one benefits as a result.

Some steps when we think about Incident response and what we need to do now.

Company by company will have some sort of Incident Response playbook and you really need to understand it and get to grips with it so you can follow the correct procedures.

However, there are going to be a few steps in common and that's what we're going to focus on.

1. First of all, you are going to want to try and isolate the device. In this instance, we know that the user is on the first floor. So we can just pop in the elevator, head down to them and disconnect the device from the network. The goal it to prevent further spread if there is a virus on there. However, if you're not in the same physical location, you can politely ask the user to disconnect from the network. This can be done by turning off the Wi-Fi or unplugging the Ethernet cable.

If they're on a VPN, ask them to disconnect immediately. This helps contain any potential malware before it spreads to shared drives or other systems.

2. Start gathering information. Ask clear and concise questions. This is once the device has been isolated- remember that. Ask them what exactly happened. What website were they on? Did they open an email attachment? Did they click a popup or install a program that turned out to be malicious? When did this happen? These information help you assess the scope and severity of the situation.

In our case, we know they were browsing a shoe store website so we can start to gather some information as to what that website is and what type of file they downloaded. 


A really important tip is never shame or blame the user. It discourages people from reporting incidents. Instead, thank them for letting IT know. Early reporting can prevent damage. We want to give the confidence to the users that reporting it is not going to end up in any sort of hot water.

At the end of the day, everyone makes mistakes, right? It's not our job to lay blame. Our job is to handle the incident.


3. Start doing all this investigation but we need to escalate or log the incident. Depending on your company's policy, you're going to log a ticket with all the details, tag it as a potential malware or security incident and let the cybersecurity team or the IT team lead immediately know if required.



4. If you role includes basic remediation, then let's proceed but proceed with caution. Open Windows Security Center > Virus & Threat protection > Protection History. You can see there if a threat is blocked.

<img width="905" height="441" alt="image" src="https://github.com/user-attachments/assets/1bb8a721-cfb1-4369-b394-72150e492dda" />


<img width="768" height="484" alt="image" src="https://github.com/user-attachments/assets/c53037ee-8111-4658-ba94-70227840cdb6" />

<img width="809" height="466" alt="image" src="https://github.com/user-attachments/assets/a9025794-6abb-4294-b77e-58966198307d" />


<img width="551" height="507" alt="image" src="https://github.com/user-attachments/assets/961054d2-b52b-4646-8f3e-e1a234a229e9" />


EICAR file= it is to simulate a virus, all the virus scanners of the world, or at least all the good ones pick it up because of how it is written.




5. We can see the status is removed. We can't just call it a day. We still need to make sure that no company data or no threats still linger in the background. 

<img width="551" height="507" alt="image" src="https://github.com/user-attachments/assets/0392f91e-7dc4-44de-b31e-b99176486c9c" />


We can see a bit of details about why it was blocked, the affected items and you can even take some actions like allow. You would only do this in an instance where this was a false positive.

6. What we want to do now is initiatite a scan. Quick scan is okay but better option is to go into the options and do a full scan of the machine.

<img width="548" height="465" alt="image" src="https://github.com/user-attachments/assets/2ddec9ef-2ab0-42c7-9c4d-dec5a886f1ec" />

This chekcs all files and running programs on the hard disk, but this scan can take some time. More importantly is we need to check that our virus and threat protection updates have been running.


<img width="715" height="571" alt="image" src="https://github.com/user-attachments/assets/184f4bb6-8806-4881-a952-da62bb634336" />


For the Full Scan, you may want to do this in booting into safemode if possible. Otherwise, doing it on the machine whilst it's isolated is absolutely fine.

For the time being, if there was a threat, we might need to preserve the evidence so we might not want to wipe or re-image the machine straight away unless we're directed by our team leader. Sometimes the IT Security team may need analyze the device for forensics.

7. Finally, once the situation is under control do remind the user, but in a friendly way that avoid clicking on links or downloading files from untrusted sources.



# Can you Spot a Phishing Email?


phishingquiz.withgoogle.com



<img width="1708" height="987" alt="image" src="https://github.com/user-attachments/assets/7d52f971-7592-4c20-a9b5-4389e411b2df" />


Even if you have the best firewall on the planet, if you're someone in your company clicks on a phishing link, attackers could get in as IT professionals or aspiring IT administrators we're not just responsible for managing devices and networks. We are also responsbile for protecting users and the organization. That's why it's crucial that you know what phishing looks like, and that you can teach others how to spoit it too.

Remember as well that phishing attacks are getting harder to spot thanks to the use of artificial intelligence. Attackers are now creating emails that are more realistic, more personalized and more common than ever before. Whereas spam emails used to be really common because there would be tons of grammatical and spelling mistakes. These days with the help of AI, they have all but eliminated that and these are getting much, much more sophisticated. So spotting the difference between real and fake isn't as easy as it used to be.




# Device Out of Compliance (Windows Updates)


**ISSUE:**

"Hi, IT SUpport. I've been on annual leave for a few months and not turned on my company laptop in all that time. When I booted it up this morning, it keeps telling me I am out of compliance and need to contact my system administrator. I am not really sure what this means. Can you please help?"


**DISCUSSION:**

We're going to be covering a key help desk scenario when a user's device is out of compliance because it's missing updates. This is a very common issue, especially in modern hybrid environments, and in managed environments where devices must meet certain update requirements to access corporate resources like VPN, email, or cloud apps.

What does out of compliance mean? It typically means that the device does not meet your organization's security or update policies. For example, it's missing critical windows security patches. It may have failed updates from the last cycle, or updates aren't installed within the required time.

If your company uses a MDM tool like Intune, SCCM, or Endpoint Manager, this noncompliant status can cause restrictions like blocking them from their email sync, VPN access, or even logging in.


**TROUBLESHOOTING:**

We heard from the call that the user explained that they've been on annual leave for a few months. More than likely, they've fallen out of date with those patching requirements that our systems security polices would set.

1. If the user reports they're blocked or receiving a compliance error, ask what they see. Get them to describe the exact error message to you. If you have permissions to open up the MDM platform, take a look at their company PC name and see what the status is there.

In this case, let's pretend that we have found that the reason for it is that they are out of compliance due to missing updates.

How do we go and run updates manually?

<img width="950" height="544" alt="image" src="https://github.com/user-attachments/assets/906afe57-83b7-4851-a61f-84ee920f1410" />

No matter what operating system they're running, you can just type in the word "update" into the search bar and hit Enter.

<img width="1410" height="734" alt="image" src="https://github.com/user-attachments/assets/33f2d5a8-fe2d-454f-bfc2-d6a3c39c9ebb" />


You can just click on the check for updates button. If it finds any, it's going to download and install them. Always restart the machine ven if not prompted. And recheck the compliance in the company portal or MDM tool if you have permissions to do that.



# How to be that stand-out employee!


<img width="932" height="967" alt="image" src="https://github.com/user-attachments/assets/ca2b1865-b574-410d-866f-5d9114d88c6e" />


