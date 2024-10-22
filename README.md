Hacker101 CTF Micro-CMS v1

Title and Basic Information
Title: Micro-CMS v1 Capture the Flag Walkthrough
Author: ALi Lotfy
Date: [14/10/2024]
Challenge Difficulty: Easy
Skills: Web Application Security

CTF Report Structure for Micro-CMS v1

Title and Basic Information
Objective
Environment Setup
Methodology and Approach
Detailed Walkthrough
Challenges Faced and Solutions
Tools Used
Lessons Learned
Conclusion
References



Objective
The goal of the Micro-CMS v1 CTF challenge is to exploit vulnerabilities in a web-based content management system to gain access and capture the flag. The challenge focuses on web application vulnerabilities such as SQL Injection and improper access controls.

Environment Setup
Environment Setup:
- Platform: Hack The Box
- Target: Micro-CMS v1 web application
- My System: Kali Linux 2023.3
- Tools Used: Nmap, SQLMap, Browser (Firefox), and the terminal.

Methodology and Approach
Reconnaissance: Performed initial information gathering using Nmap to identify open ports and services.
 Enumeration: OWASP ZAP to manually analyze web application requests and responses, searching for vulnerabilities like SQL Injection.
 Exploitation: Automated the exploitation of discovered vulnerabilities using SQLMap to extract the database and gain access.
 Flag Capture: Navigated through the CMS to locate and retrieve the flag.

Detailed Walkthrough Micro-CMS v1
Reconnaissance:Conducted a port scan using Nmap, identifying open services and potential entry points for the Micro-CMS application.Enumeration:Used OWASP ZAP to inspect HTTP requests and responses, identifying SQL Injection vulnerabilities in various input fields of the CMS.Observed that certain page numbers (e.g., 6) returned a “Forbidden” message, which hinted at hidden resources.Exploitation:Leveraged SQLMap to exploit SQL Injection vulnerabilities, gaining access to the CMS database.Found restricted content by manually modifying the URL (e.g., accessing page 6), leading to the flag.Flag Capture:After modifying the page URL, accessed sensitive information on page 6, which revealed the flag.Submitted the flag successfully through the CMS interface, completing the challenge.

(screenshot) https://imgur.com/mZ9POwy

Testing Markdown PageDescription: The image displays the first page with the "Testing" markdown test and the option to create a new page.Explanation: This is the starting point where you click on the "Testing" markdown to begin testing the web application's vulnerabilities.

( add screenshot) https://imgur.com/MgaQdZf

Page 1 Testing AddressDescription: This image shows that the current page is "Testing," and it appears as page 1 in the address bar.Explanation: It demonstrates how the web application assigns page numbers based on URLs, which helps during enumeration.

( add screenshot) https://imgur.com/9D9DU4o

Navigating to Markdown TestDescription: Clicking on "Markdown Test" takes you to another page.Explanation: This screenshot shows navigation within the CMS, leading to the second page for further exploration.

( add screenshot) https://imgur.com/mXqoF1d

Address Bar CheckDescription: The image shows that "Markdown Test" is marked as page 2 in the address bar.Explanation: The address bar confirms this page’s number, an important detail for locating hidden pages during the CTF challenge.

( add screenshot) https://imgur.com/SxqR6Zw

 Creating a New PageDescription: This screenshot captures the creation of a new page with the title “testing.”Explanation: After clicking "Create a new page," you input a title, and the system generates a new page, which later helps uncover vulnerabilities.

  ( add screenshot) https://imgur.com/mTGfgvZ

New Page CreatedDescription: The page created is numbered 12 (or another number based on the system).Explanation: The page number allocation is crucial for identifying potential hidden pages and vulnerabilities.

  ( add screenshot) https://imgur.com/Y99QpiS

Description: The page with address number 3 in the URL results in a "Not Found" message. This indicates that the requested page does not exist or has been removed from the web application.Explanation: This behavior is expected during enumeration in Capture the Flag (CTF) challenges, where testing different page numbers can reveal sensitive information or hidden vulnerabilities. In this case, page 3 is a dead link, but continuing to test other page numbers may lead to discovering restricted or vulnerable pages, as demonstrated later in the challenge.

  ( add screenshot) https://imgur.com/Eu0TFkT

Forbidden Page 6Description: The image shows that page 6 is forbidden.Explanation: Finding this forbidden page indicates that it could contain sensitive information, which leads you to investigate further.

  ( add screenshot) https://imgur.com/N63PyTX

Editing the Forbidden PageDescription: The address bar is changed to manually access page 6, and the flag is revealed.Explanation: This demonstrates the exploitation of improper access controls, where manually editing the page number gives access to the flag.

  ( add screenshot) https://imgur.com/gMW1sfw

Submitting the FlagDescription: The flag is copied and pasted into the submission field.Explanation: After retrieving the flag from the forbidden page, this step shows the process of flag submission.

  ( add screenshot) https://imgur.com/KhY1a8G

Description: The page shows the creation of a new page within the CMS by adding a specific code in the title field and then submitting the form.Explanation:This step is part of the CTF process where the user creates a new page with the intention of exploiting the CMS’s vulnerabilities. This is typically done to observe the system’s response or to insert malicious code.

  ( add screenshot) https://imgur.com/h2xv9ai

Description: After creating the page, the screenshot shows the user returning to the home screen.Explanation:Returning to the home page confirms the successful creation of the new page. The goal is to check if the CMS reflects the new page or if any unexpected behavior occurs, which could hint at potential vulnerabilities.

  ( add screenshot) https://imgur.com/aiyY8SG

Description: This page shows the flag being displayed after performing the correct steps in the challenge.Explanation:The flag, which is the key to completing this CTF, appears after exploiting the CMS vulnerabilities. The user copies the flag in this step to submit it and complete the challenge successfully.

  ( add screenshot) https://imgur.com/mm6XTsQ

  Flag Submission ConfirmationDescription: A confirmation is shown after submitting the correct flag.Explanation: This final image confirms successful submission, completing the CTF challenge.

  ( add screenshot) https://imgur.com/R2Ym6WB

Challenges Faced and SolutionsChallenge: Difficulty in identifying vulnerable pages through manual browsing.Solution: Manually iterating through multiple page numbers in the CMS and using OWASP ZAP for deeper insight.Challenge: Navigating forbidden pages without clear indication.Solution: Used URL manipulation and SQLMap to gain unauthorized access to restricted resources.

Tools UsedNmap: For port scanning and service enumeration.OWASP ZAP: For manual request analysis and vulnerability detection.SQLMap: For automating the exploitation of SQL Injection.Firefox Browser: For navigating the web application and observing behavior.Kali Linux: As the primary operating system to run all tools.

 Lessons LearnedEnumeration is Key: A thorough enumeration process is crucial for discovering hidden or vulnerable resources in web applications.SQL Injection Exploitation: This challenge highlighted the importance of identifying and exploiting SQL Injection vulnerabilities.Manual Testing: URL manipulation, combined with automated tools like SQLMap, can lead to the discovery of forbidden or hidden pages.

 ConclusionThe Micro-CMS v1 CTF challenge successfully demonstrated the importance of systematic enumeration and vulnerability testing in web applications. By exploiting SQL Injection vulnerabilities and bypassing access controls, the flag was captured, showcasing key techniques in web application security.

 ReferencesHack The Box Micro-CMS v1 ChallengeOWASP ZAP DocumentationSQLMap Official GuideKali Linux 2023.3 Documentation

