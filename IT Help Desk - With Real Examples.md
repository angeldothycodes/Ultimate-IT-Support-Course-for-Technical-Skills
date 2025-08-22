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

