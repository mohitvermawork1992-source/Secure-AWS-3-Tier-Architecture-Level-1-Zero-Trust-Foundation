# Security Groups Design

## ALB-SG
### Inbound
- HTTP 80 from 0.0.0.0/0
- HTTPS 443 from 0.0.0.0/0

### Outbound
- HTTP 80 to APP-SG

---

## APP-SG
### Inbound
- HTTP 80 from ALB-SG

### Outbound
- MySQL 3306 to DB-SG
- HTTPS 443 to 0.0.0.0/0 (package updates via NAT)

---

## DB-SG
### Inbound
- MySQL 3306 from APP-SG

### Outbound
- Default all outbound
