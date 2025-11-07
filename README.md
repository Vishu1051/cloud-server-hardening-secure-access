# cloud-server-hardening-secure-access ( ssh + firewall + IAM )

☁️ Cloud Server Hardening – Secure Access
🧩 1️⃣ SSH Security

🔹 🔑 Use Key-based Authentication
  → Disable password login (PasswordAuthentication no)

🔹 🚪 Change Default SSH Port
  → e.g. from 22 → 2222

🔹 👤 Allow Specific Users Only
  → Edit /etc/ssh/sshd_config:
    AllowUsers admin ops

🔹 🕒 Enable Idle Timeout
  → Auto logout inactive sessions

🔹 🧱 Use Fail2Ban
  → Blocks IPs after failed attempts

🔥 2️⃣ Firewall Configuration

🔹 🔒 Enable Default-Deny Policy
  → Block all, allow only required ports

🔹 🌐 Allow Only Trusted IPs
  → Restrict SSH (e.g. office VPN only)

🔹 🧩 Common Ports

Service	Port	Action
SSH	22 / custom	Allow (limited IPs)
HTTP	80	Allow (if web)
HTTPS	443	Allow
Others	—	Deny

🔹 ⚙️ Use Tools:
  ufw, firewalld, iptables

👥 3️⃣ IAM (Identity & Access Management)

🔹 👤 Principle of Least Privilege
  → Give users minimal permissions

🔹 🔁 Use Roles & Groups
  → Manage access via IAM roles, not individuals

🔹 🧩 MFA Everywhere
  → Multi-Factor Authentication for admin access

🔹 🔍 Audit & Logging
  → Enable CloudTrail / Activity logs

🔹 🗝️ Rotate Keys Regularly
  → Remove unused credentials

🧠 Bonus Tips

✅ Keep OS & Packages Updated
✅ Monitor login attempts (/var/log/auth.log)
✅ Use Bastion Host for SSH access
✅ Automate compliance checks (e.g. AWS Config, Azure Policy)
