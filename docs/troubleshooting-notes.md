# Troubleshooting Notes

## Issue 1 — SSM not connecting
### Root Cause
EC2 app subnet required outbound internet through NAT for SSM and package access.

### Fix
Verified app route table:
- 0.0.0.0/0 → NAT Gateway

---

## Issue 2 — Security group confusion
### Root Cause
Initially APP-SG outbound rules were not clearly mapped to DB-SG.

### Fix
Configured:
- APP-SG outbound 3306 → DB-SG
- DB-SG inbound 3306 ← APP-SG

---

## Issue 3 — RDS connectivity validation
### Fix
Installed MariaDB client on EC2 and validated:

mysql -h <rds-endpoint> -u admin -p
