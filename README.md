# CTF
<h1>SQL INJECTION </h1>

<h2>Description</h2>
In-Band SQL Injection is the easiest type to detect and exploit; In-Band just refers to the same method of communication being used to exploit the vulnerability and also receive the results, for example, discovering an SQL Injection vulnerability on a website page and then being able to extract data from the database to the same page.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Virtual Machine</b> 
- <b>SQL</b>

<h2>Environments Used </h2>

- <b>Kali Linux</b> 

<h2>Program walk-through:</h2>

<p align="center">
Launch Sqlinjection: <br/>
<img src="https://i.imgur.com/5i7h3x3.png" height="80%" width="80%" alt="SQLinjection Steps"/>
<br />
<br />
This statement should produce an error message informing you that the UNION SELECT statement has a different number of columns than the original SELECT query. So let's try again but add another column:  <br/>
<img src="https://i.imgur.com/k0wavVR.png" height="80%" width="80%" alt="SQLinjection Steps"/>
<br />
<br />
Same error again, so let's repeat by adding another column: <br/>
<img src="https://i.imgur.com/042LDC5.png" height="80%" width="80%" alt="SQLinjection Steps"/>
<br />
<br />
Success, the error message has gone, and the article is being displayed, but now we want to display our data instead of the article. The article is being displayed because it takes the first returned result somewhere in the web site's code and shows that. To get around that, we need the first query to produce no results. This can simply be done by changing the article id from 1 to 0.:  <br/>
<img src="https://i.imgur.com/0n8jyql.png" height="80%" width="80%" alt="SQLinjection Steps"/>
<br />
<br />
You'll now see where the number 3 was previously displayed; it now shows the name of the database, which is sqli_one.
Our next query will gather a list of tables that are in this database.:  <br/>
<img src="https://i.imgur.com/h3LJedl.png" height="80%" width="80%" alt="SQLinjection Steps"/>
<br />
<br />
There are a couple of new things to learn in this query. Firstly, the method group_concat() gets the specified column (in our case, table_name) from multiple returned rows and puts it into one string separated by commas. The next thing is the information_schema database; every user of the database has access to this, and it contains information about all the databases and tables the user has access to. In this particular query, we're interested in listing all the tables in the sqli_one database, which is article and staff_users. 
As the first level aims to discover Martin's password, the staff_users table is what is of interest to us. We can utilise the information_schema database again to find the structure of this table using the below query.:  <br/>
<img src="https://i.imgur.com/h3LJedl.png" height="80%" width="80%" alt="SQLinjection Steps"/>
<br />
<br />
This is similar to the previous SQL query. However, the information we want to retrieve has changed from table_name to column_name, the table we are querying in the information_schema database has changed from tables to columns, and we're searching for any rows where the table_name column has a value of staff_users.
The query results provide three columns for the staff_users table: id, password, and username. We can use the username and password columns for our following query to retrieve the user's information.
Again we use the group_concat method to return all of the rows into one string and to make it easier to read. We've also added ,':', to split the username and password from each other. Instead of being separated by a comma, we've chosen the HTML <br> tag that forces each result to be on a separate line to make for easier reading.
You should now have access to Martin's password to enter to move to the next level.

:  <br/>
<img src="https://i.imgur.com/ggFMAVI.png" height="80%" width="80%" alt="SQLinjection Steps"/>
</p>


<h1>Wpa/Wpa2 Wifi Hacking </h1>

<h2>Description</h2>
In-Band SQL Injection is the easiest type to detect and exploit; In-Band just refers to the same method of communication being used to exploit the vulnerability and also receive the results, for example, discovering an SQL Injection vulnerability on a website page and then being able to extract data from the database to the same page.
<br />


<h2>Tools Required </h2>

- <b>Network Adapter (e.g., TL-WN722N V2) with monitoring mode support.</b> 
- <b>Aircrack-ng</b>
- <b>Airodump-ng</b>
- <b>Airmon-ng</b>
-<b>Crunch</b>
<h2>Environments Used </h2>

- <b>Kali Linux</b> (21H2)

<h2>Program walk-through:</h2>
<p>Monitoring Mode Setup
Step 1: Kill Interrupting Services
Before enabling monitoring mode, identify and kill services that might interrupt the process</p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/dd5fc52d-7e17-412f-b610-e02d669956bc)

<p>Step 2: Enable Monitoring Mode
Stop the WLAN interface and enable monitor mode:</p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/7ff8fc4e-1bd6-484f-baba-3be7437ca605)

<p>Verify the mode using: iwconfig</p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/0e78f00c-9da3-4f45-ac0f-56f92ed9fa40)

<p>Packet Capture and 4-way Handshake
Step 3: Capture BSSID and Monitor Network
Use airodump-ng to capture BSSID information:airodump-ng wlan0 </p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/2c8bdbe7-b257-4127-addb-aeabb3c25a81)
<p>Select a specific BSSID for monitoring and run:airodump-ng -c 1 -w Scan_network --bssid EW:WV:4H:J7:A5:28 wlan0 </p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/ae365eef-823b-4f01-ad7b-71ac6513efe7)
<p>Step 4: Deauthentication Process
Deauthenticate the target Wi-Fi to capture the 4-way handshake:
sudo aireplay-ng -0 0 -a EW:WV:4H:J7:A5:28 wlan0</p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/3e0ada97-b5ca-4cd2-bae2-ea4d86d6cdb9)
<p>Run the command until you see the 4-way handshake in the background code.</p>

<p>Final Stage: Password Cracking with Crunch and Aircrack-ng
After capturing the 4-way handshake, the final step involves cracking the Wi-Fi password using Crunch and aircrack-ng. It's important to note that the success of this process heavily depends on various factors, including the complexity and length of the password.
Using Crunch for Password Generation
In this example, I used Crunch to generate possible passwords. Since I knew the Wi-Fi password consisted of only numeric characters, the command was tailored accordingly:
sudo crunch 8 8 123456780 | aircrack-ng -w - Scan_Kamalesh-01.cap -e KamaleshD</p>

![image](https://github.com/MohebAwichewi/Projects/assets/149394585/196a444e-22da-4718-801a-7b98a2db694b)






