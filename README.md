
<h1> Analyse and visualise data with splunk for : Common Wealth Bank Cyber security Job Simulation </h1>

<h2>Description</h2>
Developed skills in building data visualization dashboards using Splunk to uncover patterns and insights in historical customer data, aiding in fraud detection.
<br />


<h2>Tools Required</h2>

- <b>Virtual Machine</b> 
- <b>SEIM : Splunk</b>

<h2>Environments Used </h2>

- <b>Kali Linux</b>
  
<h2>Program walk-through:</h2>
<p> Import data into Splunk
 After installing Splunk Enterprise and creating an account, import “prepared_data.csv” by
 selecting “Add Data”s</p>

 ![image](https://github.com/MohebAwichewi/Projects/assets/149394585/9dbda82b-fcb3-4a91-aa8f-522abfa84882)
<p>  Then, click on “Upload files from my computer”. This means that the “prepared_data.csv” file
 should already be saved on your computer </p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/52ed06bd-b81b-4997-88a6-10aa0a701338)
<p>Select the file from your computer, then click on next. In the “Set Source Type” section, you
 may see a caution sign error, as shown below</p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/6bd28b5b-49ce-41e2-aa3e-96fdf8fe6c60)
<p>Go to Timestamp on the left and change from “Auto” to “Current time”, then click on “Save
 As”. You can name this “fraud_dectection.csv” and save</p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/4429e069-2d2f-4f9a-9ec9-8e260202165e)
<p>Click on “Next” until you get the result below</p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/04813a38-9c9b-4dc7-aec6-1096545a07a2)
<p>Analysing the Data
 Click on “Start Searching” to start analysing. On the left, you can find the “Interesting Fields”
 section</p>
 
 ![image](https://github.com/MohebAwichewi/Projects/assets/149394585/b5c05e49-79f8-4211-99e6-103ca1fa3e46)

 <p>Creating the Dashboard
 One of the ways to create a dashboard in Splunk is via search</p>
 
 ![image](https://github.com/MohebAwichewi/Projects/assets/149394585/839e947a-3dcd-4bd3-93ff-37d47cd2b907)
 <p>For example, to add “Count by category” to your dashboard, type out
 sourcetype="fraud_detection.csv" | top category in the search field. This action counts
 the number in each category, and you should get something like the example below</p>
 
 ![image](https://github.com/MohebAwichewi/Projects/assets/149394585/8992138f-2f12-4e17-96fe-e3367f207277)

 <p>To add this chart to your dashboard, go to “Save As > New Dashboard > Dashboard Title =
 “Fraud Detection Dashboard” > Classic Dashboards > Save to Dashboard. This creates your
 dashboard</p>
 
 ![image](https://github.com/MohebAwichewi/Projects/assets/149394585/de0ffd1b-73bd-4698-a402-23fd7f392ed9)
 <p> To get “Fraud detected by category”, type sourcetype="practicesplunk.csv" fraud="1" |
 stats count values(fraud) by category in the search field. This counts the number of
 fraudulent activities recorded for each category.
 To get “Gender with the most fraudulent activity by category”, type
 sourcetype="practicesplunk.csv" fraud="1" gender="F'" | stats count values(fraud) by
 category.
 To add more charts, you need to add to “Existing Dashboard” and select the one you’ve
 created. Also, for more chart options (e.g., histograms, line charts), see below</p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/b7277247-454f-4985-a568-9a1f58c60560)
<p>You can rearrange your dashboard to suit your liking by clicking the “Edit” button</p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/d6e6de9c-7cdb-44c1-ad76-b426d9a17373)
<p>To export the dashboard, click the “Export PDF” button</p>

<h1> Penetration Testing : Hackthissite </h1>

<h2>Description</h2>
 HackThisSite.org isanonlineplatformthatprovidesa legal andsafeenvironment for
 individuals to improve theircyber securityskills throughavarietyofchallengesand
 CapturetheFlag(CTF)events.Establishedin2003, it isnot justawebsiteforhacker
 simulationsbut ratheracommunityof like-mindedindividualswhoarededicatedto
 sharing and gaining knowledge in ethical hacking, programming, and technical hobbies.
<br />


<h2>Tools Required</h2>

- <b>Virtual Machine /laptop</b> 
- <b>Knowledge in programmation and Web Dev</b>
-<b>ANALYTICAL SKILLS</b>

<h2>Environments Used </h2>

- <b>Windows</b>
  
<h2>Program walk-through:</h2>
<p>  Appendix
 ● Basic Level 1</p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/aa4093c5-2ee7-4163-9e93-23fe4cbef4f2)
<p> ● Basic Level 3 </p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/4ddb9e15-284a-4604-a20a-4b12f939896b)

<p> ● Basic Level 4&5 </p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/8287930a-d947-42c2-a8e0-1d47fc6100c3)
<p> ● Basic Level 7 </p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/a29d5c76-49d5-4fa9-969d-31f7703cd576)

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/d453c01f-b8a7-495e-a0fb-7d601f48c128)
<p> ● Basic Level 8 </p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/5eb0c572-a71a-4170-931f-06eb4b216c46)

<p> ● Basic Level 9 </p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/a79b9873-0bf2-4c64-8936-5fa4c05da50f)

<p> ● Basic Level 10 </p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/b0b5c99f-f355-432c-b459-b0ce45386f81)

<p> ● Basic Level 11 </p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/8b9b8cef-6e3f-4f0f-a709-91dd10a105f1)
<p>Conclusion : In conclusion, the penetration testing report found several vulnerabilities in the "Basic"
 web challenge from HackThisSite.org. These vulnerabilities included hardcoded
 passwords, no password file, location of the password hidden in the source code,
hardcoded credentials within the application, weak encryption and command injection.
 These vulnerabilities could potentially lead to a breach of confidentiality, integrity and
 availability that could result in business, financial or reputational loss for an
 organisation. The report provided recommendations for better securing the web
 application and highlighted the importance of proper web application security. It's
 important to note that regular penetration testing and vulnerability assessments can
 help you to identify and fix security vulnerabilities before they can be exploited by
 attackers. </p>

 <p> PENETRATION TESTING REPORT </p>
 
[hack this site pentesting report.pdf](https://github.com/MohebAwichewi/Projects/files/14358260/hack.this.site.pentesting.report.pdf)













