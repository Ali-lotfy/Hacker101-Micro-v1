<h1>Hacker101 CTF Micro-CMS v1</h1>

<h2>Title and Basic Information</h2>
<b>Title:</b> Micro-CMS v1 Capture the Flag Walkthrough

<b>Author:</b> ALi Lotfy

<b>Date:</b> [14/10/2024]

<b>Challenge Difficulty:</b> Easy

<b>Skills:</b> Web Application Security

<h2>CTF Report Structure for Micro-CMS v1</h2>

- *Title and Basic Information*  
- Objective  
- Environment Setup
- Methodology and Approach
- Detailed Walkthrough
- Challenges Faced and Solutions
- Tools Used
- Lessons Learned
- Conclusion
- References



<h2>Objective</h2>

The goal of the Micro-CMS v1 CTF challenge is to exploit vulnerabilities in a web-based content management system to gain access and capture the flag.
The challenge focuses on web application vulnerabilities such as SQL Injection and improper access controls.

<h2>Environment Setup</h2>


- <b>Platform:</b> Hack The Box
 
- <b>Target:</b> Micro-CMS v1 web application

- <b>My System:</b> Kali Linux 2023.3

- <b>Tools Used:</b> Nmap, SQLMap, Browser (Firefox), and the terminal.

<h2>Methodology and Approach</h2>

 - <b>Reconnaissance:</b> Performed initial information gathering using Nmap to identify open ports and services.

- <b>Enumeration:</b> OWASP ZAP to manually analyze web application requests and responses, searching for vulnerabilities like SQL Injection.

- <b> Exploitation:</b>  Automated the exploitation of discovered vulnerabilities using SQLMap to extract the database and gain access.

- <b> Flag Capture:</b>  Navigated through the CMS to locate and retrieve the flag.

<h2>Detailed Walkthrough Micro-CMS v1</h2>
- <b>Reconnaissance:</b>Conducted a port scan using Nmap, identifying open services and potential entry points for the Micro-CMS application.

- <b>Enumeration:</b>Used OWASP ZAP to inspect HTTP requests and responses, identifying SQL Injection vulnerabilities in various input fields of the CMS.Observed that certain page numbers (e.g., 6) returned a “Forbidden” message, which hinted at hidden resources.
  
- <b>Exploitation:</b>Leveraged SQLMap to exploit SQL Injection vulnerabilities, gaining access to the CMS database.Found restricted content by manually modifying the URL (e.g., accessing page 6), leading to the flag.
  
- <b>Flag Capture:</b>After modifying the page URL, accessed sensitive information on page 6, which revealed the flag.Submitted the flag successfully through the CMS interface, completing the challenge.


<h2>Detailed Walkthrough Micro-CMS v1:</h2>

<p align="center">
Walkthrough Micro-CMS v1: <br/>
<img src="https://imgur.com/mZ9POwy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>Detailed Testing Markdown Page:</h2>

- <b>Testing Markdown Page Description:</b> The image displays the first page with the "Testing" markdown test and the option to create a new page.
  
- <b>Explanation:</b> This is the starting point where you click on the "Testing" markdown to begin testing the web application's vulnerabilities.

<p align="center">
Testing Markdown Page: <br/>
<img src="https://imgur.com/MgaQdZf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>Page 1 Testing Address:</h2>

- <b>Page 1 Testing Address Description:</b> This image shows that the current page is "Testing," and it appears as page 1 in the address bar.
  
- <b>Explanation:</b> It demonstrates how the web application assigns page numbers based on URLs, which helps during enumeration.
  
<p align="center">
Page 1 Testing Address: <br/>
<img src="https://imgur.com/mXqoF1d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>Navigating to Markdown Test:</h2>

- <b>Navigating to Markdown Test Description:</b> Clicking on "Markdown Test" takes you to another page.
  
- <b>Explanation:</b> This screenshot shows navigation within the CMS, leading to the second page for further exploration.
  
<p align="center">
Navigating to Markdown Test: <br/>
<img src="https://imgur.com/mXqoF1d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>Address Bar Check:</h2>

- <b>Navigating to Markdown Test Description:</b> The image shows that "Markdown Test" is marked as page 2 in the address bar.
  
- <b>Explanation:</b> The address bar confirms this page’s number, an important detail for locating hidden pages during the CTF challenge.
  
<p align="center">
Address Bar Check: <br/>
<img src="https://imgur.com/SxqR6Zw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>Creating a New Page:</h2>

- <b>Creating a New Page Description:</b> This screenshot captures the creation of a new page with the title “testing”.
  
- <b>Explanation:</b> After clicking "Create a new page," you input a title, and the system generates a new page, which later helps uncover vulnerabilities.
  
<p align="center">
Creating a New Page: <br/>
<img src="https://imgur.com/mTGfgvZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>New Page Created:</h2>

- <b>New Page Created Description:</b> The page created is numbered 12 (or another number based on the system).
  
- <b>Explanation:</b> The page number allocation is crucial for identifying potential hidden pages and vulnerabilities.
  
<p align="center">
New Page Created: <br/>
<img src="https://imgur.com/Y99QpiS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />




<h2>The page with address number 3 in the URL results in a "Not Found" message:</h2>

- <b>New Page Created Description:</b> The page with address number 3 in the URL results in a "Not Found" message.
- This indicates that the requested page does not exist or has been removed from the web application.
  
- <b>Explanation:</b> This behavior is expected during enumeration in Capture the Flag (CTF) challenges, where testing different page numbers can reveal sensitive information or hidden vulnerabilities.
- In this case, page 3 is a dead link, but continuing to test other page numbers may lead to discovering restricted or vulnerable pages, as demonstrated later in the challenge.
  
<p align="center">
The page with address number 3 in the URL results in a "Not Found" message: <br/>
<img src="https://imgur.com/Eu0TFkT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>Forbidden Page 6:</h2>

- <b>Forbidden Page 6 Description:</b> The image shows that page 6 is forbidden.
  
- <b>Explanation:</b> Finding this forbidden page indicates that it could contain sensitive information, which leads you to investigate further.
  
<p align="center">
Forbidden Page 6: <br/>
<img src="https://imgur.com/N63PyTX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>Editing the Forbidden Page:</h2>

- <b>Editing the Forbidden Page Description:</b> The address bar is changed to manually access page 6, and the flag is revealed.
  
- <b>Explanation:</b> This demonstrates the exploitation of improper access controls, where manually editing the page number gives access to the flag.
  
<p align="center">
Editing the Forbidden Page: <br/>
<img src="https://imgur.com/gMW1sfw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>Submitting the Flag:</h2>

- <b>Submitting the Flag Description:</b> The flag is copied and pasted into the submission field.
  
- <b>Explanation:</b> After retrieving the flag from the forbidden page, this step shows the process of flag submission.
- 
<p align="center">
Submitting the Flag: <br/>
<img src="https://imgur.com/KhY1a8G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>The page shows the creation of a new page within the CMS:</h2>

- <b>The page shows the creation of a new page within the CMS Description:</b> The page shows the creation of a new page within the CMS by adding a specific code in the title field and then submitting the form.
  
- <b>Explanation:</b> This step is part of the CTF process where the user creates a new page with the intention of exploiting the CMS’s vulnerabilities.
- This is typically done to observe the system’s response or to insert malicious code.

<p align="center">
The page shows the creation of a new page within the CMS: <br/>
<img src="https://imgur.com/h2xv9ai.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>The user returning to the home screen:</h2>

- <b>The user returning to the home screen Description:</b> After creating the page, the screenshot shows the user returning to the home screen.
  
- <b>Explanation:</b> Returning to the home page confirms the successful creation of the new page.
- The goal is to check if the CMS reflects the new page or if any unexpected behavior occurs, which could hint at potential vulnerabilities.


<p align="center">
The user returning to the home screen: <br/>
<img src="https://imgur.com/aiyY8SG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />



<h2>The flag being displayed:</h2>

- <b>The flag being displayed Description:</b> After creating the page, the screenshot shows the user returning to the home screen.
  
- <b>Explanation:</b> The flag, which is the key to completing this CTF, appears after exploiting the CMS vulnerabilities.
- The user copies the flag in this step to submit it and complete the challenge successfully.


<p align="center">
The flag being displayed: <br/>
<img src="https://imgur.com/mm6XTsQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>Flag Submission Confirmation:</h2>

- <b>Flag Submission Confirmation Description:</b> After creating the page, the screenshot shows the user returning to the home screen.
  
- <b>Explanation:</b> This final image confirms successful submission, completing the CTF challenge.


<p align="center">
Flag Submission Confirmation: <br/>
<img src="https://imgur.com/R2Ym6WB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

 
<h2>Challenges Faced and Solutions </h2>

- <b>Challenge:</b> Difficulty in identifying vulnerable pages through manual browsing.
  
- <b>Solution:</b> Manually iterating through multiple page numbers in the CMS and using OWASP ZAP for deeper insight.
  
- <b>Challenge:</b> Navigating forbidden pages without clear indication.
  
- <b>Solution:</b> Used URL manipulation and SQLMap to gain unauthorized access to restricted resources.
  

<h2>Tools Used </h2>

- <b>Nmap:</b> For port scanning and service enumeration.

- <b>OWASP ZAP:</b> For manual request analysis and vulnerability detection.

- <b>SQLMap:</b> For automating the exploitation of SQL Injection.

- <b>Firefox Browser:</b> For navigating the web application and observing behavior.
 
- <b>Kali Linux:</b> As the primary operating system to run all tools.


<h2> Lessons Learned </h2>

- <b>Enumeration is Key:</b> A thorough enumeration process is crucial for discovering hidden or vulnerable resources in web applications.

- <b>SQL Injection Exploitation:</b> This challenge highlighted the importance of identifying and exploiting SQL Injection vulnerabilities.

 - <b>Manual Testing:</b> URL manipulation, combined with automated tools like SQLMap, can lead to the discovery of forbidden or hidden pages.

 
<h2> Conclusion </h2>

 The Micro-CMS v1 CTF challenge successfully demonstrated the importance of systematic enumeration and vulnerability testing in web applications.
 
 By exploiting SQL Injection vulnerabilities and bypassing access controls, the flag was captured, showcasing key techniques in web application security.

<h2>  References  </h2>

 Hack The Box Micro-CMS v1 Challenge

 OWASP ZAP Documentation
 
 SQLMap Official Guide
 
 Kali Linux 2023.3 Documentation

