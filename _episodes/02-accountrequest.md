---
title: "Account Request & Login via SSH"
teaching: 0
exercises: 0
questions:
- "How can I join this awesome US-ATLAS analysis facility?"
objectives:
- "Get a computing account and sign into UChicago analysis facility "

keypoints:
- "Look out! paste only the content of your SSH public key!, and never share the content of your SSH private key!"
---

> ## Main steps
>
> - <a href="#account">Account request via CIConnect</a>
>
> - <a href="#key">Upload public SSH key</a>
>
> - <a href="#login">Login via SSH</a>
{: .callout}

<!------------------------------------------------------------------------------------->
<!------------------------------ Account request -------------------------------------->
<h2 id="account">Account Request via CIConnect</h2>


Go to <a href="https://af.uchicago.edu">UChicago Analysis Facility Website</a> and click Sign-Up
![image info](./../fig/i_a1signup.png/){:width="700" }

Accept use policy and continue.
![image info](./../fig/i_a2policy.png/){:width="700"}

Globus site: use your CERN or institutional account and login.
![image info](./../fig/i_a3organiz.png){:width="700"}

After your organization is found, continue.
![image info](./../fig/i_a3organizlog.png){:width="700"}

Check details, agree to privacy policy and continue.
![image info](./../fig/i_a4details.png){:width="700"}

Allow CI-Connect to acess info
![image info](./../fig/i_a5useinfo.png){:width="700"}
Good! now you will create your profile.
![image info](./../fig/i_a6profile.png){:width="700"}

<!------------------------------------------------------------------------------------->
<!------------------------------ Upload public ssh key--------------------------------->

<h2 id="key">Upload public SSH key</h2>

To create your profile just type in the information required.

Now you will upload an SSH public key, **important: do not copy the contents of a file that does not end in `.pub`. You mus only upload the `public`(.pub)** part of the key.
if you are not sure if you have generated an SSH Public Key before, try the following instructions on your laptop command line.
![image info](./../fig/i_a7oldkey.png){:width="700"}

Follow the next steps if you don't have a public key or want to create an additional one for this analysis facility (it is recommended to use a new SSH key for each instance) for example by replacing "rsa" with "rsa_uc" in the following instructions
![image info](./../fig/i_a8newkey.png){:width="700"}

Paste the contents of the clipboard on the next text box and update your profile!!

Remember to check you didn't add any blank space or additional characters
![image info](./../fig/i_a9pastekey.png){:width="700"}


<!------------------------------------------------------------------------------------->
<!------------------------------ login via ssh--------------------------------->
<h2 id="login">Login via SSH</h2>

Now that you signed up on the Analysis Facility website and uploaded a key, it will take a little bit of time to process your profile and add your account to the system. After 10-15 minutes, you ought to be able to login via SSH:

```bash
ssh <your_unix_username>@login.af.uchicago.edu
```
After logged in you should see something like the following images, containing a welcome message, links to information resources, and your file system quota report

![image info](./../fig/i_a10insshlogo.png){:width="500"}

If it does not work, please double check that you have been approved, have a public key uploaded and have waited at least 15 minutes. If you still have an issue, feel free to reach out to us for help.


<!----------------------------------- fin --------------------------------------------->
{% include links.md %}

