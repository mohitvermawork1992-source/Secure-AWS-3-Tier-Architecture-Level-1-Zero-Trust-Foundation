# Secure-AWS-3-Tier-Architecture-Level-1-Zero-Trust-Foundation

## 📌 Architecture
![Architecture](architecture/VPC-zero-trust-architecture.png)

---

## 🚀 Traffic Flow
Internet → ALB → Private EC2 → Private MySQL RDS

---

## 🔐 Security Controls
- ALB only public ingress
- Private EC2 application tier
- Private MySQL RDS
- NAT controlled egress
- SG-to-SG trust boundaries
- SSM private administration

---

## ✅ Validation Proof
- ALB browser test successful
- EC2 to RDS MySQL login successful
- Single-AZ DB active in DB-A subnet
- Future Multi-AZ ready with DB-B subnet

---

## 📚 Documentation
- docs/security-groups.md
- docs/route-tables.md
- docs/troubleshooting-notes.md
