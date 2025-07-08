# AWS GuardDuty Security Alert System

This project sets up a real-time security alerting system using AWS services to monitor suspicious activity and send alerts via email.

---

## 🔐 What It Does

- Listens for **GuardDuty security findings** (e.g., suspicious shell commands)
- Uses **Amazon EventBridge** to match specific threat patterns
- Triggers **Amazon SNS** to send alerts to an email address
- Supports simulated testing with custom events

---

## 🧰 Technologies Used

- Amazon GuardDuty
- Amazon EventBridge
- Amazon SNS
- IAM (permissions)
- CloudWatch (for monitoring)
- Email alerts

---

## 📦 Architecture Diagram

