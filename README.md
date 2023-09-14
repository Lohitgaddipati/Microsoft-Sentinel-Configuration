# Microsoft-Sentinel-Configuration


Step 1: I started by creating a log analytic workspace to add my in-Sentinel workspace 

Step 2: Install hub content solutions 
 
In this step, I installed four Microsoft offered solutions which are mentioned below
Starting with Microsoft Azure Active Directory for identity and access management data 

Then Microsoft Azure Activity for creating policy that should be followed by Microsoft Defender 365 and Windows Security Event. 

Step 3: I explored for a little while and then I started configuring data connectors, starting with Active directory, which enables a check box configuration. Here I get to choose the types of data I want ingested.

Next, I moved on to Azure activity, which is a little different from the connectors. For this, I needed to create a policy that the organization must comply to. 

Once redirected, I had to figure out the scope and parameters of the policy which can be done by selecting the respected resource group

One of the most important settings here was remediation. Meaning if you want to implement this policy starting with the new devices or for all the previously existing devices as well. Remediation allows to include previous devices into the policy which by default would not be included. 
 
Once all the setting we configured, I then submitted my configurations. It took some time, but I got the successful creation message. 

Finally, I moved to configure the Windows security events uses Data collection rules to collect data. So I had to create a DCR. Here I had an option to choose what kinds of data I wanted to send across which includes all data, alert data or custom.

Step 4: Now, I started working on enabling and creating analytic rules. 

Here I have had access to a couple of pre-defined templated which were helpful in for the first time in creating these rules. These analytic rules co-relates the data collected from your data connectors and compares them to the rules create to determine its alert based on which incidents are reported. 

Step 5: I also wanted to automate a few processes for which I used automation rules. This can also be done while creating analytic rules, but I wanted to do this separately to document. 

This rule takes the appropriate actions defined by me, based on the logic, which will also be decided by me. I also got to select the time for which this rule can be active. 

Analytics offers Automation rules and playbooks. Automation rules are easy tasks at management level whereas playbooks use azure logic to allow more control and function related to incident. 

Step 6: Once, all that was done I wanted to see the coverage of my security. For this, sentinel has MITRE ATT&CK. This provides a cohesive look of your security posture based on the collection all the data from a non-profit organization. 

Step 7: 

I also want to see the data depected in a visual form which makes it easier for me and anyone else who looks at it. For which I create a workbook which is a graphical tool to analyze data. 

Workbook has some predefined templets that can be used to create your workbook


All the resources and security we added is completely isolated under one resource group, which if need can be deleted with rest of your work. 
![image](https://github.com/Lohitgaddipati/Microsoft-Sentinel-Configuration/assets/101139863/a298a8cd-fce8-423f-abfa-bb5356d2823a)
