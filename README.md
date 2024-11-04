# PASTA Lab - Process for Attack Simulation and Threat Analysis

### Overview
In this activity, you will practice using the Process of Attack Simulation and Threat Analysis (PASTA) threat model framework. You will determine whether a new shopping app is safe to launch.

Threat modeling is an important part of secure software development. Security teams typically perform threat models to identify vulnerabilities before malicious actors do. PASTA is a commonly used framework for assessing the risk profile of new applications.

### Scenario
You’re part of the growing security team at a company for sneaker enthusiasts and collectors. The business is preparing to launch a mobile app that makes it easy for their customers to buy and sell shoes. 

You are performing a threat model of the application using the PASTA framework. You will go through each of the seven stages of the framework to identify security requirements for the new sneaker company app.

# Part 1 - Access the resources
### Step 1: Access the template
To use the template for this course item, click the following link and select Use Template. 

Link to template: 
<a href="https://docs.google.com/document/d/1wHFh3n6ZWkgK9Gs9VfO86Pnr7D-7UCAZ/edit?usp=sharing&ouid=105064495821226407439&rtpof=true&sd=true">PASTA worksheet</a>

### Step 2: Access supporting materials
The following supporting materials will help you complete this activity. Keep them open as you proceed to the next steps. 

To use the supporting materials for this course item, click the following link and select Use Template. 

Link to supporting materials: 

<a href="https://docs.google.com/presentation/d/1RfNwds5LCkYkJ2xWr4QdXhWCbjZ6tyL_/edit?usp=sharing&ouid=105064495821226407439&rtpof=true&sd=true">PASTA data flow diagram</a>

<a href="https://docs.google.com/presentation/d/1UgeiU9GyrTTzs1ucNUmxRbr5iYHEQWNx/edit?usp=sharing&ouid=105064495821226407439&rtpof=true&sd=true">PASTA attack tree</a>

# Part 2 - Complete the PASTA stages
### Stage 1: Identify the mobile app's business objectives
The main goal of Stage I of the PASTA framework is to understand why the application was developed and what it is expected to do.

**Note:** Stage I typically requires gathering input from many individuals at a business.

First, review the following description of why the sneaker company decided to develop this new app:

**Description:** Our application should seamlessly connect sellers and shoppers. It should be easy for users to sign-up, log in, and manage their accounts. Data privacy is a big concern for us. We want users to feel confident that we’re being responsible with their information.

Buyers should be able to directly message sellers with questions. They should also have the ability to rate sellers to encourage good service. Sales should be clear and quick to process. Users should have several payment options for a smooth checkout process. Proper payment handling is really important because we want to avoid legal issues.

In the **Stage 1** row of the **PASTA worksheet**, make **2-3 notes** of business objectives that you’ve identified from the description.

<table>
  <tr>
    <td>Define business and security objectives</div></td>
    <td>
      <ul>
        <li><b>User-Centric Design:</b> The application should prioritize user experience, making it easy for users to sign up, log in, manage accounts, and navigate the platform.</li>
        <li><b>Data Privacy and Security:</b> The application must adhere to strict data privacy regulations and implement robust security measures to protect user information.</li>
        <li><b>Seamless Transactions:</b> The platform should facilitate smooth and secure transactions, offering various payment options and ensuring proper payment handling.</li>
      </ul>
    </td>
  </tr>
</table>

### Stage 1 Notes:
  * The primary business objective is to create a user-friendly platform that facilitates seamless transactions between buyers and sellers. Key security objectives include protecting user data privacy, ensuring secure payment processing, and preventing unauthorized access to system resources.
# 

### Stage 2: Evaluate the app's components
In Stage II, the technological scope of the project is defined. Normally, the application development team is involved in this stage because they have the most knowledge about the code base and application logic. Your responsibility as a security professional would be to evaluate the application's architecture for security risks.

For example, the app will be exchanging and storing a lot of user data. These are some of the technologies that it uses:

  * **Application programming interface (API):** An API is a set of rules that define how software components interact with each other. In application development, third-party APIs are commonly used to add functionality without having to program it from scratch.

  * **Public key infrastructure (PKI):** PKI is an encryption framework that secures the exchange of online information. The mobile app uses a combination of symmetric and asymmetric encryption algorithms: AES and RSA. AES encryption is used to encrypt sensitive data, such as credit card information. RSA encryption is used to exchange keys between the app and a user's device.

  * **SHA-256:** SHA-256 is a commonly used hash function that takes an input of any length and produces a digest of 256 bits. The sneaker app will use SHA-256 to protect sensitive user data, like passwords and credit card numbers.

  * **Structured query language (SQL):** SQL is a programming language used to create, interact with, and request information from a database. For example, the mobile app uses SQL to store information about the sneakers that are for sale, as well as the sellers who are selling them. It also  uses SQL to access that data during a purchase.

Consider what you've learned about these technologies: 

  * Which of these technologies would you evaluate first? How might they present risks from a security perspective?

In the Stage II row of the PASTA worksheet, write 2-3 sentences (40-60 words) that describe why you choose to prioritize that technology over the others.

<table>
  <tr>
    <td>Define the technical scope</div></td>
    <td>List of technologies used by the application:<br>
      <ul>
        <li><b>Application programming interface (API)</b></li>
        <li><b>Public key infrastructure (PKI)</b></li>
        <li><b>SHA-256</b></li>
        <li><b>SQL</b></li>
      </ul>
      The API should be prioritized due to its role in data exchange and potential exposure to vulnerabilities. Its broad reach and handling of sensitive information make it a critical component to secure. However, a detailed analysis of the specific APIs used is necessary to identify potential risks and implement appropriate security measures.
    </td>
  </tr>
</table>

### Stage 2 Notes:
  * Among the technologies listed, the API should be prioritized for initial security evaluation. APIs serve as the interface between the application and external systems, making them a critical point of entry for potential attacks.

  * The API should be prioritized due to its role in data exchange and potential exposure to vulnerabilities. Its broad reach and handling of sensitive information make it a critical component to secure. However, a detailed analysis of the specific APIs used is necessary to identify potential risks and implement appropriate security measures.
# 

### Stage 3: Review a data flow diagram
During Stage III of PASTA, the objective is to analyze how the application is handling information. Here, each process is broken down.

For example, one of the app's processes might be to allow buyers to search the database for shoes that are for sale. 

Open the **PASTA data flow diagram** resource. Review the diagram and consider how the technologies you evaluated relate to protecting user data in this process.

**Note:** Software developers usually have detailed data flow diagrams available for security teams to use and verify that information is being processed securely.

<table>
  <tr>
    <td>Decompose application</div></td>
    <td><a href="https://docs.google.com/presentation/d/1RfNwds5LCkYkJ2xWr4QdXhWCbjZ6tyL_/edit?usp=sharing&ouid=105064495821226407439&rtpof=true&sd=true">PASTA data flow diagram</a></td>
  </tr>
</table>

### Stage 3 Notes:
In Stage III, the focus is on analyzing the application's data flow to identify potential vulnerabilities and security weaknesses. By reviewing the data flow diagram, it's crucial to ensure that the database is configured securely, with proper input validation and sanitization to prevent SQL injection attacks. Additionally, securing data transmission between components is essential to protect sensitive information.
# 

### Stage 4: Use an attacker mindset to analyse potential threats
Stage IV is about identifying potential threats to the application. This includes threats to the technologies you listed in Stage II. It also concerns the processes of your data flow diagram from Stage III.

For example, the apps authentication system could be attacked with a virus. Authentication could also be attacked if a threat actor social engineers an employee.

In the **Stage IV** row of the **PASTA worksheet**, list **2 types** of threats that are risks to the information being handled by the sneaker company's app. 

Pro tip: Internal system logs that you will use as a security analyst are good sources of threat intel

<table>
  <tr>
    <td rowspan="2">Threat analysis</div></td>
    <td><b><u>Internal Threats:</u></b>
      <ul>
        <li><b>Accidental Data Deletion or Modification:</b> Human error, such as accidental deletion or modification of critical data, can lead to data loss or corruption.</li>
        <li><b>Insider Threats:</b> Malicious insiders, such as disgruntled employees or compromised accounts, can exploit vulnerabilities to steal sensitive data or disrupt operations.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td><b><u>External Threats:</u></b>
      <ul><li><b>Cyberattacks:</b> Malicious actors can launch various attacks, including hacking, phishing, and malware, to compromise the application's security and steal data.</li>
        <li><b>Data Breaches:</b> Unauthorized access to sensitive data can lead to data breaches, exposing confidential information and damaging the organization's reputation.</li>
      </ul>
    </td>
  </tr>
</table>

### Stage 4 Notes:
Stage IV focuses on identifying potential threats to the application, including those targeting the underlying technologies. Injection attacks on the SQL database and session hijacking due to insecure cookie handling are significant risks. By understanding these threats, organizations can implement appropriate security measures to protect the application and its data.
# 

### Stage 5: List vulnerabilities that can be exploited by those threats
Stage V of PASTA is the vulnerability analysis. Here, you need to consider the attack surface of the technologies listed in Stage II.

For example, the app will use a payment system. The form used to collect credit card information might be vulnerable if it fails to encrypt data.

In **Stage V** of the **PASTA worksheet**, list **2 types** of vulnerabilities that could be exploited.

Pro tip: Resources like the <a href="https://cve.mitre.org/cve/search_cve_list.html">CVE® list</a> and <a href="https://owasp.org/www-community/vulnerabilities/">OWASP</a>  are useful for finding common software vulnerabilities.

<table>
  <tr>
    <td>Vulnerability analysis</div></td>
    <td>
      <ul>
        <li><b>Insecure Coding Practices:</b> Weak or vulnerable code can lead to a variety of security issues, such as SQL injection, cross-site scripting (XSS), and buffer overflows. These vulnerabilities can be exploited by attackers to gain unauthorized access or compromise the application's integrity.
</li>
        <li><b>Database Vulnerabilities:</b> Misconfigurations, weak passwords, and outdated database software can expose the database to attacks like SQL injection, unauthorized access, and data breaches.</li>
      </ul>
    </td>
  </tr>
</table>

Stage 5 Notes:
  * Stage V focuses on identifying specific vulnerabilities within the application's design and implementation. Insecure coding practices, such as the absence of prepared statements in SQL queries, can lead to injection attacks. Additionally, improper handling of session cookies can increase the risk of session hijacking.
# 

### Stage 6: Map assets, threats, and vulnerabilities to an attack tree
In Stage VI of PASTA, the information gathered in the previous two steps are used to build an attack tree.

Open the **PASTA attack tree** resource. Review the diagram and consider how threat actors can potentially exploit these attack vectors.

**Note:** Applications like this normally have large, complex attack trees with many branches.

<table>
  <tr>
    <td>Decompose application</div></td>
    <td><a href="https://docs.google.com/presentation/d/1UgeiU9GyrTTzs1ucNUmxRbr5iYHEQWNx/edit?usp=sharing&ouid=105064495821226407439&rtpof=true&sd=true">PASTA attack tree</a></td>
  </tr>
</table>

### Stage 6 Notes:
Attack trees are a valuable tool for visualizing potential attack paths and identifying critical vulnerabilities. By mapping out potential attack scenarios, security teams can prioritize mitigation strategies and allocate resources effectively. The MITRE ATT&CK framework provides a comprehensive taxonomy of attack techniques, which can be used to inform threat modeling and incident response planning.
# 

### Stage 7: Identify new security controls that can reduce risk
PASTA threat modeling is commonly used to reduce the likelihood of security risks. In Stage VII, the final goal is to implement defenses and safeguards that mitigate threats.

<table>
  <tr>
    <td>Vulnerability analysis</div></td>
    <td>
      <ul>
        <li><b>Strong Password Policies:</b> Enforcing strong password policies, including complexity requirements and regular password changes, can significantly reduce the risk of unauthorized access.</li>
        <li><b>Network Security:</b> Implementing robust network security measures, such as firewalls, intrusion detection systems (IDS), and intrusion prevention systems (IPS), can help protect the application from external threats.</li>
        <li><b>Data Encryption:</b> Encrypting sensitive data both at rest and in transit can help protect it from unauthorized access and data breaches.</li>
        <li><b>Regular Security Audits and Penetration Testing:</b> IConducting regular security assessments and penetration testing can identify and address vulnerabilities before they can be exploited by attackers.</li>
      </ul>
    </td>
  </tr>
</table>

In **Stage VII** of the **PASTA worksheet**, list **4 security controls** that you have learned about that can reduce the chances of a security incident, like a data breach.
