---

# DomainInsight

DomainInsight is a Python tool developed to gather comprehensive information about domains and IP addresses. It utilizes various techniques to retrieve DNS information, WHOIS details, SSL certificate information, and performs Nmap scanning to identify open ports and services.

## Features

- **DNS Information**: Retrieve DNS records (e.g., A records) associated with a domain.
- **WHOIS Lookup**: Fetch WHOIS information for domain registration details.
- **SSL Certificate Details**: Obtain SSL certificate information (subject, issuer, expiration date) for HTTPS-enabled domains.
- **Nmap Scanning**: Perform Nmap scans to identify open ports, services, and detect the operating system (OS) of the target host.

## Requirements

- Python 3.x
- Required Python libraries (install using `pip`):
  ```bash
  pip install python-whois dnspython python-nmap
  ```

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/DomainInsight.git
   ```

2. Navigate to the project directory:
   ```bash
   cd DomainInsight
   ```

3. Run the tool:
   ```bash
   python domain_insight.py
   ```

4. Enter a domain name or IP address when prompted.

## Example Output

```plaintext
Enter a domain or IP address: example.com

IP Address: 93.184.216.34
DNS Info: {'domain': 'example.com', 'ip_address': ['93.184.216.34']}
WHOIS Info:
{
  "domain_name": "EXAMPLE.COM",
  "registrar": "RegistrarName",
  "creation_date": "1995-08-14T04:00:00Z",
  "expiration_date": "2023-08-13T04:00:00Z",
  ...
}
SSL Info:
Subject: {'organizationName': 'Internet Corporation for Assigned Names and Numbers', 'commonName': '*.example.com'}
Issuer: {'organizationName': 'DigiCert Inc', 'commonName': 'DigiCert TLS RSA SHA256 2020 CA1'}
Expiration Date: 2023-09-10 12:00:00

Starting Nmap scan for 93.184.216.34...
Nmap Scan Results for 93.184.216.34:
Port 80: http (nginx 1.14.0), OS: Linux
Port 443: https (nginx 1.14.0), OS: Linux
```

## Disclaimer

- Use this tool responsibly and only on systems and networks you have permission to scan.
- Respect the privacy and terms of service of external services (e.g., WHOIS databases, SSL certificate providers).

---
