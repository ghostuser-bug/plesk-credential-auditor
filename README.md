# 🛡️ Plesk Credential Auditor & Security Testing Tool

This Go-based tool is designed for **security audits and penetration testing of Plesk servers**.  
It performs bulk credential validation using a `list.txt` file and supports multi-threading for faster execution. Results are saved in organized files for audit or reporting purposes.

> ⚠️ **Use responsibly:** Only test servers and accounts you are authorized to access.

---

## 🔐 Cybersecurity Use Cases

- **Internal security audits** of Plesk-hosted infrastructure  
- **Password policy verification** and weak credential detection  
- **Red team engagements** to simulate compromised accounts  
- **Automated audit reporting** for system administrators

---

## 🚀 Features

- Multi-threaded credential checking for high-speed processing  
- Validates successful and failed login attempts  
- Organized results:
  - `result/Success.txt` for valid logins  
  - `result/Failed.txt` for invalid logins  
- Simple CLI interface for quick deployment  
- Scalable to large credential lists

---

## 📦 Installation

### Prerequisites
- Go 1.18 or later  
- Internet connection  
- `list.txt` file containing login credentials in `username:password:host` format

### Clone Repository
```sh
git clone https://github.com/ghostuser-bug/plesk-credential-auditor.git
cd plesk-credential-auditor
````

### Build the Tool

```sh
go build -o plesk-checker
```

No external dependencies beyond the Go standard library.

---

## ⚙️ Usage

### Running the Tool

```sh
./plesk-checker
```

1. Enter the number of threads when prompted
2. The tool will read credentials from `list.txt`
3. Results will be saved in:

   * `result/Success.txt` for valid logins
   * `result/Failed.txt` for invalid logins

### Example `list.txt`

```
admin:password123:example.com
user:testpass:plesk.hosting.com
```

### Sample Output

```sh
Enter number of threads: 10
[SUCCESS] - user:testpass:plesk.hosting.com
[FAILED] - admin:password123:example.com
Done.
```

---

## ⚠️ Legal Disclaimer

This tool is intended for **authorized security testing only**.
Unauthorized access to systems or accounts may violate laws and Plesk’s terms of service.

---

## 🤝 Contributing

Pull requests and improvements are welcome to enhance functionality, add protocol support, or improve efficiency.

---

## 📜 License
```
MIT License
```
