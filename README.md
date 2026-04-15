# Secure-AWS-3-Tier-Architecture-Level-1-Zero-Trust-Foundation
Built a multi-AZ zero-trust 3-tier AWS architecture where ingress is terminated at an ALB, application servers run in private subnets with NAT-based controlled egress, and the database tier is fully isolated with SG-based identity trust.

aws-secure-3tier-zero-trust-foundation/
│
├── README.md
├── architecture/
│   ├── level1-final-architecture.png
│   └── traffic-flow.txt
│
├── docs/
│   ├── security-groups.md
│   ├── route-tables.md
│   └── troubleshooting-notes.md
│
├── scripts/
│   ├── install-nginx.sh
│   └── db-connect-test.sh
│
└── screenshots/
    ├── alb-live-browser.png
    ├── target-group-healthy.png
    ├── mysql-rds-connected.png
    └── ssm-private-ec2.png

