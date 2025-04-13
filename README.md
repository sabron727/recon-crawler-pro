# recon-crawler-pro
for pentest or bug bounty hunter
# Recon Crawler Pro

**Recon Crawler Pro** is a powerful Python-based web crawling and vulnerability scanning tool designed for bug bounty hunters and penetration testers. It automates the process of crawling websites, discovering subdomains, and identifying common vulnerabilities such as **SQL Injection (SQLi)**, **Cross-Site Scripting (XSS)**, **Local File Inclusion (LFI)**, **Server-Side Request Forgery (SSRF)**, and more.

## Features

- **Crawl websites** for links and JavaScript files.
- **Automated vulnerability scanning** for:
  - SQL Injection (SQLi)
  - Cross-Site Scripting (XSS)
  - Local File Inclusion (LFI)
  - Server-Side Request Forgery (SSRF)
- **Brute-force subdomains** with customizable wordlist.
- **Integrations with Burp Suite** and **OWASP ZAP** for output exports.
- **Support for Wayback URLs** and **gau** (GetAllURLs) to gather past URLs.
- **Configurable crawling options**, such as delay between requests, follow redirects, and more.

## Installation

1. Clone this repository:
    ```bash
    git clone https://github.com/USERNAME/recon-crawler-pro.git
    cd recon-crawler-pro
    ```

2. Install required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

Run the script with various options:

```bash
python3 recon_crawler_pro.py --url https://target.com --vuln-scan --export-burp
Available Options:

    --url (required): Target URL to crawl.

    --threads (optional): Number of threads for crawling. Default is 10.

    --delay (optional): Delay in seconds between requests. Default is 0.5.

    --resume (optional): Resume crawling from previously visited URLs.

    --js-parser (optional): Extract JavaScript file URLs.

    --vuln-scan (optional): Enable vulnerability scanning (LFI, SSRF, SQLi, XSS).

    --subdomains (optional): Path to wordlist for subdomain brute-forcing.

    --gau (optional): Use gau to gather past URLs.

    --export-burp (optional): Export crawled URLs in Burp Suite XML format.

    --export-zap (optional): Export crawled URLs in OWASP ZAP text format.

    --xssscan (optional): Enable XSS scanning.

    --sqlscan (optional): Enable SQLi scanning.

    --json-mode (optional): Extract JSON fields if available in the response.

    --follow-redirect (optional): Follow HTTP redirects.
