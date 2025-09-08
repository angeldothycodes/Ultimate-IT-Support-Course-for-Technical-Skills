
# WHAT ARE APPLICATIONS?

<img width="935" height="485" alt="image" src="https://github.com/user-attachments/assets/3f38a653-52bc-403f-971e-7405a9b56de8" />


<img width="928" height="488" alt="image" src="https://github.com/user-attachments/assets/7653ce13-7410-4456-a785-680ece806a57" />



Some support tasks there may include resolving compatibility issues, perhaps with different websites, clearing caches if they get too full, and cause problems with the end users websites. And troubleshooting website loading problems.



<img width="962" height="485" alt="image" src="https://github.com/user-attachments/assets/d435a0b6-7959-4904-8ab9-6de79846589d" />


<img width="942" height="477" alt="image" src="https://github.com/user-attachments/assets/f5a8e83c-919d-4102-9f3b-f15eccd26e8a" />


<img width="915" height="470" alt="image" src="https://github.com/user-attachments/assets/19fb6710-79e2-409c-aee2-dfdce7d7f2ed" />



Understanding some of these common applications, troubleshooting techniques, and best practices are going to be key to providing an effective technical support in your roles.

I implore you, if you're currently working in an IT field, go out to some common applications that your end users are using and go and see if they have a current knowledge base or documentation that you can start reading through.


# WHAT IS ACTIVE DIRECTORY?

<img width="923" height="415" alt="image" src="https://github.com/user-attachments/assets/78b47a43-216f-4ae9-9599-c2567280477d" />


Now when you go down to your local hardware store and buy a laptop or a desktop, that laptop or desktop is joined to what's called a work group.

Now, a work group is not centrally managed in any way.

Your user account will exist on that device only, and it's typically not very straightforward to set up things like file shares, print servers and everything managed by a work group.

So that's where Active Directory comes in.

Active directory is a directory service developed by Microsoft for Windows Domain Networks.

Its purpose is to manage user and computer accounts, and it allows it to control access to resources and enforces security policies so what you can do is you can spin up a local Active Directory server on your network. All your user accounts for your organization's staff will be managed by that Active Directory server.

All the computers as well.

And you can do things like create policies that apply to those users, set password restrictions.

For example, you could set that the minimum password length is ten characters.

And one of the neatest things is a user can then log into any machine connected to that domain using the username and password that you've specified on the Active Directory service.

Some of the key components of an Active Directory is the domain itself. This is the logical group of network objects the users and computers.

You have organization units which are containers used to organize these objects.

For example you may have an HR container that contains all the computers and users used by the HR department. You may split it up based on location. You may have, for example, a Los Angeles organization unit.

You may have a Detroit organization unit. 

**Group policy** are the policies we spoke about. Those centralized management of operating systems and applications.

**Group policy is an extremely powerful tool.** You can do everything from deploy applications down to these machines to restrict what websites they can visit or what apps they're able to use, restrict how many characters a password can be.

For example, you may set a 14 character minimum if you're working in a very secure environment.


Lastly, I want to talk about domain controllers, which are the servers that host this Active Directory services and respond to those authentication requests.

These aren't just limited to one.

You can have multiple Active Directory services, a sort of a redundancy in case one was to go down.

So you may have a primary and a secondary at your site for that high uptime.


<img width="919" height="493" alt="image" src="https://github.com/user-attachments/assets/4dd2e684-9d9f-47ad-93fa-9dd87cc267fc" />



As a technical support specialist, it's going to be very common for you to be working within an Active Directory environment.

Some of the more common issues that you're going to see in some of the more common help desk tickets that you are going to receive are creating and setting up new user accounts.

So as people join your organization, you're going to be setting up those accounts, giving them the correct permissions, setting their password for the first time, login, things like that.


**You're going to be modifying.**

You're going to be updating user information and resetting passwords.

So a good example is if someone was to get married and change their surname you would have to go into Active Directory, change that.

If someone has forgotten their password, maybe they've been on an extended leave or they've just forgotten it over the weekend, you'd go ahead and reset that password and help them get back into their account and of course, deactivating and deleting accounts. When a employee leaves, you're going to remove that account and ensure that they can no longer log in to the network, reducing any risk of that employee causing harm to the network.


**You're going to be troubleshooting group policy issues.**

Maybe a policy isn't applying correctly.

You would need to go into the Active Directory server and troubleshoot that group policy object.

You're going to implement new policies or maybe even update existing ones, you're going to manage user

access to shared resources.

So if there's a file share, they may be assigned that permission through Active Directory.


<img width="918" height="366" alt="image" src="https://github.com/user-attachments/assets/360e4f63-6302-49a7-807a-6648fdab94ef" />


**You're also going to be resolving login issues for users.**


So maybe a user's password has expired and they're no longer able to log in.

You're going to be helping them with that or you're going to be investigating account lockouts.

So one of the more common settings within an Active Directory environment is if a user gets their password wrong three times, it's going to lock their account out.

You're going to then need to unlock that account and assist them getting back into their computer.



<img width="967" height="389" alt="image" src="https://github.com/user-attachments/assets/39039ce2-9b13-4332-a561-892bd527a913" />


While we're on the subject of Active Directory, is there also is Microsoft now also provides a cloud-based Active Directory service, which is known as Azure AD, now also known as **Entra ID.**

Now, Azure Active Directory is a cloud based identity and access management service provided by Microsoft.

It's tied in with the Microsoft 365 bundle, and it provides secure authentication and authorization for users, devices, and applications from the cloud.

So no longer do you need that on premises infrastructure to run a domain.

You can just as long as your computer has internet connection, tie up to the Microsoft domain in the cloud that is localized to your business unit.


## BENEFITS OF AZURE AD

<img width="973" height="519" alt="image" src="https://github.com/user-attachments/assets/2083a9dd-150f-4882-aa04-078901e5e038" />

It allows for single sign on, which is where users log in once and access multiple applications using the same username and password, you can add extra layers of security just beyond passwords, which is the multi-factor authentication.

This can be things like an SMS code to your mobile, or maybe an app on your phone that cycles through six digit codes every 30s.

You can integrate Azure AD with on premises Active Directory as well for that seamless synchronization and coexistence.

Using the cloud, you can also control access to what resources and under what conditions users can access data.

And of course, conditional access is a major security benefit which implements security policies based on user and device contexts.

So for example, you can do things like geo blocking, which is where users can't log in to their office

365 account and can't log into the machines if they're outside of the country that you're currently in.



<img width="904" height="487" alt="image" src="https://github.com/user-attachments/assets/c94c1207-ea6e-4575-b01d-e94c17bd8077" />


The Azure AD scales automatically to meet the needs of any business side without the need of additional hardware.

If you're running an on premises domain and you'll have users in the thousands and thousands, you're going to need to spin up multiple servers to manage all of those users.

But with Azure AD, you don't need to worry about any of that.

It's scalability in the cloud.

All of that is put onto Microsoft to manage.

So a lot of IT engineers are moving their organizations to Azure AD for that scalability.

There's enhanced security.

So we spoke about the conditional access.

There are also things like advanced threat protection and identity protection for those users accounts.

The cost efficiency is another major benefit of why organizations are moving.

So it reduces the need for physical infrastructure, lowering your maintenance and operational costs.

And it allows you to have a pay as you go pricing model, which aligns with actual usage.

This is what we call operational expenditure over the capital expenditure of having to buy hardware and then manage and maintain it.

And then of course, there's the seamless sign on which we already spoke about, and the ability to reset users own passwords, which reduces the load on IT Support.

**Self-service password reset **in Microsoft 365 is absolutely massive right now, and it's something that Microsoft really recommends if you're signing up to their services that you set up.

And this is going to allow users to reset their own passwords by providing different authentication methods.

For example, they may have to get an email to their personal email or a text message to their personal phone, ensuring that that user is who they say they are and allowing them to go through the steps to reset their own password if they've forgotten it.


# Domains, DNS, Websites and Certificates


<img width="640" height="505" alt="image" src="https://github.com/user-attachments/assets/77bab995-f998-4aec-97b3-0d53e17e4ad1" />


**What is a Domain?**

A domain is a human readable address used to access websites.

When we talk about computers, they don't use the same language we do.

Computers are all ones and zeros. When you're going out and going to a website, your computer isn't acknowledging things like udemy.com.

What it's doing is it's translating that into an IP address that it then uses to establish a TCP protocol for you to go ahead and browse.

However, we are humans. We can't remember numbers like computers can. What we do is we purchase domains. For example Udemy.com is a domain and we have systems that translate domains into those IP addresses.


<img width="588" height="461" alt="image" src="https://github.com/user-attachments/assets/b06b41e7-e0f5-48f6-bcd1-6f0978a0dce5" />


Domains are registered through domain registrars.

So GoDaddy and Namecheap to name just a few.

And ownership must be renewed periodically so you can buy domains for a year, two years, and you have to continuously keep purchasing in order for you to own them.


<img width="655" height="534" alt="image" src="https://github.com/user-attachments/assets/e0d5c850-f609-4fe0-837d-4cf2e0945222" />


A lot of on premises infrastructure contains a DNS server that you can host locally, but you can also use public DNS servers.

So Google host a public DNS server, which is a 8.8.8.8, and Cloudflare host another very popular one, which is 1.1.1.1.



<img width="971" height="456" alt="image" src="https://github.com/user-attachments/assets/fdac25ef-a254-4762-9a03-950919d30783" />



For those wanting to get into some web design, what you're going to want to need to understand is sort of the three phases of creating a website.

>> **Design and development** is the first one where you create the layout, the design and the functionality.

>> **Testing and QA** is always important. Ensuring the website works, especially if it's something like, let's say, a sales website or an ecommerce website, you kind of want to test to make sure that end users can't do anything to break your website or potentially cause harm.

>> And of course, then there's the **deployment**. That's where you upload the website files to a web server, configure your DNS and make that site accessible.


<img width="790" height="467" alt="image" src="https://github.com/user-attachments/assets/ae6e9f16-29da-40f7-a947-58f2e7a4b81e" />

We always want to think about the security of our domains, DNS and websites. And that's why we have SSL certificates.

So SSL stands for Secure Sockets Layer certificates, are digital certificates that authenticate a website's identity and enable encrypted communications.

These certificates are to ensure data transmitted between the web server and your browser is secure.

Websites use these to build trust with users by validating the website's legitimacy.

These have to be purchased and are more often than not purchased on a yearly or two yearly subscription.

They need to be installed on the web server that's hosting the website, and this is to ensure that all web traffic can be redirected from HTTP, which is insecure, to Https, which is secure.


<img width="714" height="437" alt="image" src="https://github.com/user-attachments/assets/12d1cc3a-dbbc-4b72-8c42-dd7f08fdd5b2" />


<img width="934" height="435" alt="image" src="https://github.com/user-attachments/assets/c19a4d68-0c9f-4286-9168-47d509839aa1" />



# Backups and Disaster Recovery

<img width="516" height="384" alt="image" src="https://github.com/user-attachments/assets/3099c381-5c45-4075-acb1-21a5918fc4f7" />


<img width="766" height="506" alt="image" src="https://github.com/user-attachments/assets/a610012d-4456-40cf-9a3b-dbf9dff17332" />

<img width="413" height="439" alt="image" src="https://github.com/user-attachments/assets/7d65d010-a8a3-4b5e-9c5e-5eb50a048b4d" />


 <img width="942" height="404" alt="image" src="https://github.com/user-attachments/assets/c1fe64f9-21b3-4ff3-bf37-5906fb97ffcd" />



<img width="539" height="280" alt="image" src="https://github.com/user-attachments/assets/d94ea91a-b623-4ca1-b61f-d31832ac0167" />


It's not just enough to back up your data on premises.

You also want to look at offsite and cloud backups.

This allows you to store copies of the data in offsite locations or cloud environments.

It's going to ensure that data redundancy and protection against physical disasters.

We spoke about natural disasters occurring.

Let's say, for example, a flood if you're running servers in your office and the backups are also located in your office, and there is some sort of flood that renders all of that equipment inoperable, then you've essentially just lost everything.

But by keeping it at a different geographical location, you can reduce the risk of that happening because it's very unlikely.

Let's say, for example, you're hosting some servers in Los Angeles and your offsite backups are going to New York City.

It's highly unlikely that both of those locations are going to be affected at once by some sort of natural disaster.

More often than not, you want to keep those types of backups air gapped, however, so that something like ransomware can't infect both the Los Angeles office and the New York City office.


<img width="568" height="474" alt="image" src="https://github.com/user-attachments/assets/f767ffeb-6604-4596-b0b8-d46d8138528a" />


<img width="655" height="485" alt="image" src="https://github.com/user-attachments/assets/405bc26b-5e51-4c38-b81d-b626610d66f0" />


<img width="582" height="486" alt="image" src="https://github.com/user-attachments/assets/d3a5b452-cacf-417d-afb4-d3cf56af188a" />



# Email and Mail Filtering


Email is going to play a major part in your technical support role. Both you are going to use emails to contact your end users, perhaps through a ticketing system or through a platform like Microsoft Outlook, but you're also going to be assisting the end users with their emails, whether that be the emails that they're sending from their personal machines.

Perhaps they've set up an application that automatically their emails their customers. Let's say, for example, you're working for a company that does sales and on their website, every time someone purchases something, they're going to get an email with the purchase receipt. These are all the various things that you could be looking at as a technical support specialist.


<img width="550" height="445" alt="image" src="https://github.com/user-attachments/assets/b02a3c58-63ba-42dc-9486-258312af34f6" />


<img width="479" height="439" alt="image" src="https://github.com/user-attachments/assets/6145777c-b086-4880-be46-64ad8199817e" />


<img width="961" height="509" alt="image" src="https://github.com/user-attachments/assets/d9245e75-aaa7-4c2a-92a6-ce7a7a4cc9a0" />



The sending side is often using SMTP, Simple Mail Transfer Protocol, to send the messages to the recipient's mail server. If you're working in an on premises environment and you've got a Microsoft exchange server, your outlook client will go ahead and be connected to that Exchange server.

When you send the mail, it's going to send the mail over to the server. That server is going to send it out to the internet to whoever is receiving it. And then on the receiving end, the recipient's email client retrieves the email using, let's say, for example, exchange ActiveSync or maybe iMap or Pop3 and downloads it to their email client.

I know everyone out there seems to think that email is sort of this complex system, but it really isn't. All you need is your email clients, your email servers, and these protocols that we've talked about. And that's enough to get you up and running.



<img width="918" height="421" alt="image" src="https://github.com/user-attachments/assets/42650482-de50-4eea-9327-70f6a090fd54" />


<img width="920" height="468" alt="image" src="https://github.com/user-attachments/assets/18bfd681-a1c0-4f32-be75-e41de412c372" />


<img width="916" height="451" alt="image" src="https://github.com/user-attachments/assets/3c571c44-395e-459d-ab91-ac69e25e81f5" />


<img width="864" height="477" alt="image" src="https://github.com/user-attachments/assets/ae822f57-c41f-4cb4-93e5-f7ecc421040b" />


<img width="942" height="492" alt="image" src="https://github.com/user-attachments/assets/a9776181-3f34-4274-901a-b4742a959e7f" />


And lastly, we always want to educate our users to recognize and report phishing attempts that they receive, as it's ultimately them that are the barrier between an attack on our network and our network being safe.


<img width="938" height="501" alt="image" src="https://github.com/user-attachments/assets/3d77e330-5a7b-4523-8831-9241c9bc7383" />


When we look at implementing email filtering solutions, you can implement them on premises.

This often offers more control, but requires significant maintenance and up front costs.

Or we can look at cloud based email filtering solutions.

These are often easier to deploy and maintain with scalable costs.

Some examples are Microsoft Defender for 365 and Google Workspace Security.


<img width="897" height="408" alt="image" src="https://github.com/user-attachments/assets/858c0983-8896-4678-b0bb-53ecac723537" />

<img width="848" height="473" alt="image" src="https://github.com/user-attachments/assets/aee21a0f-201d-44b2-8ca0-512ce7639db4" />



# FILE SHARING


<img width="890" height="446" alt="image" src="https://github.com/user-attachments/assets/b306983a-9fee-472f-9e10-91127a20c778" />


If you've got a bunch of end users at your office, let's say about 50, and they're all collaborating on different folders and files.

You want to store these on a central file server, so that multiple people can work on the same folders and files at once, and that they can all access it when they need to.


<img width="736" height="524" alt="image" src="https://github.com/user-attachments/assets/8cbc4fc9-616b-41ae-877f-8ae2c29ad4bb" />


The more commonly used file servers these days are run on Microsoft Windows servers and Linux servers, but there are specialized network devices and specialized vendors out there that provide their own products for businesses in order to have these file servers. These are often highly available and can be scalable up to absolutely insane amounts of storage.


<img width="626" height="451" alt="image" src="https://github.com/user-attachments/assets/7f2d20e7-ef62-4807-8fa2-77fcfa91ada9" />


<img width="535" height="512" alt="image" src="https://github.com/user-attachments/assets/36186e34-9b6a-4de3-abb9-41cace97d3e0" />
