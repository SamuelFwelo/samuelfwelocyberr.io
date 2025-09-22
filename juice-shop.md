# OWASP Juice Shop Lab

The **OWASP Juice Shop** is a deliberately vulnerable web application used worldwide to practice web application penetration testing and secure coding.  
In this project, I deployed Juice Shop in a Docker container, confirmed the service was running, and performed reconnaissance using Nmap and HTTP header analysis.  
This demonstrates my ability to set up vulnerable labs, enumerate services, and collect meaningful data for analysis and reporting.
---

## 1. Running Juice Shop
To create a safe test environment, I used **Docker Compose** to spin up Juice Shop locally.  
Docker allows me to isolate vulnerable applications without exposing my main system.
**Screenshot:**  
![Juice Shop Running](assets/2025-09-21-01-juice-shop-home.png)

📌 *Why this matters:* Being able to deploy applications in containers is a critical skill for security testing, since most enterprise environments use Docker or Kubernetes today. It also shows I can reproduce vulnerable environments for hands-on labs.

---

## 2. Docker Container Verification
Once deployed, I verified that the Juice Shop container was running and mapped correctly to port 3000.  
This ensures the service is accessible and functioning as expected.
**Screenshot:**  
![Docker Container](assets/2025-09-21-01-juice-shop-docker.png)

[View Docker PS log](logs/docker-ps.txt)
📌 *Why this matters:* Verifying container status is part of good operational security practice. In penetration testing, confirming your target is “live” before scanning saves time and ensures accurate results.

---

## 3. Nmap Scan
Next, I ran an **Nmap scan** against port 3000 with default scripts and service detection enabled.  
The scan identified an open HTTP service and returned version information along with some web headers.
**Screenshot:**  
![Nmap Scan](assets/2025-09-21-01-juice-shop-nmap.png)

[View Full Scan Log](logs/juice-scan.txt)

📌 *Why this matters:* Nmap is one of the most widely used reconnaissance tools in cybersecurity. Knowing how to run scans and interpret results is essential for vulnerability assessments, penetration testing, and even blue team defense.

---

## 4. HTTP Response Headers
Finally, I used `curl -I` to capture **HTTP response headers** from the Juice Shop application.  
Headers reveal useful metadata such as allowed methods, caching policies, security options, and server behavior. 
**Screenshot:**  
![Headers](assets/2025-09-21-01-juice-shop-headers.png)

[View Headers Log](logs/juice-headers.txt)
📌 *Why this matters:* Headers often expose misconfigurations (like missing security headers). Practicing this step helps develop the habit of checking “small details” that attackers can exploit.
---

## Key Takeaways

- ✅ Deployed a vulnerable web app using Docker to create a safe testing environment.  
- ✅ Verified container status and confirmed proper service mapping to port 3000.  
- ✅ Performed reconnaissance with Nmap and interpreted scan results.  
- ✅ Analyzed HTTP headers to identify potential weaknesses.  
- ✅ Documented results with logs and screenshots to demonstrate methodology.

## Reflection

This lab helped me practice **both offensive (red team)** and **defensive (blue team)** thinking:  
- Offensively, I learned how to discover services, gather system details, and prepare for exploitation.  
- Defensively, I saw how much information a poorly configured application reveals to attackers — highlighting the importance of secure coding and proper configuration.  

This project strengthens my portfolio by showing that I don’t just “run tools” — I understand what the output means, why it matters, and how it connects to real-world cybersecurity practices.

