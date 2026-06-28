# Software-Security-Portfolio
1. Briefly summarize your client, Artemis Financial, and its software requirements. Who was the client? What issue did the company want you to address?
Artemis Financial is a consulting firm that handles sensitive, individualized financial plans. They needed their public web application modernized and secured. I was tasked with addressing data in transit vulnerabilities by implementing secure cryptographic hashing (SHA-256) and secure communications (HTTPS).

2. What did you do well when you found your client’s software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall well-being?
I successfully implemented a "shift-left" security approach by integrating automated dependency scanning directly into the build pipeline. Secure coding is vital for a financial company to protect client assets, maintain consumer trust, and prevent catastrophic regulatory fines (like GLBA or PCI-DSS compliance failures).

3. Which part of the vulnerability assessment was challenging or helpful to you?
Navigating the National Vulnerability Database (NVD) server outages and Cloudflare 524 timeouts during the automated dependency check was challenging. However, it was highly helpful because it taught me how to configure API keys, manage rate limits, and document "fail-closed" DevSecOps pipeline failures.

4. How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use?
I layered security by enforcing HTTPS via a self-signed JKS certificate (Transport Layer), applying SHA-256 checksums for data integrity (Application Layer), and utilizing the OWASP Dependency-Check plugin (Supply Chain Layer). In the future, I will continue embedding automated SAST (Static Application Security Testing) tools directly into the CI/CD pipeline.

5. How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities?
I compiled the Spring Boot application and manually verified the RESTful endpoint in a web browser to ensure the TLS tunnel was active. To verify no new vulnerabilities were introduced, I executed a full, clean OWASP dependency-check scan against the updated NIST database.

6. What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks?
I utilized Java Keytool for certificate generation, Maven for build automation, Spring Boot for rapid web deployment, and the OWASP Dependency-Check plugin mapped to the NIST API for vulnerability scanning.

7. Employers sometimes ask for examples of work that you have successfully completed to show your skills, knowledge, and experience. What might you show future employers from this assignment?
I would showcase the pom.xml configuration to demonstrate my ability to automate DevSecOps gates. I would also highlight the keystore.jks implementation for TLS encryption and the pipeline failure report detailing how I engineered around a third-party API timeout.
