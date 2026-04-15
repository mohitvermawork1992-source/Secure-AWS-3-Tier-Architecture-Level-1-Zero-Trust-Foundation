# Route Table Design

## Public Route Table
- 0.0.0.0/0 → IGW
- Associated with Public-A and Public-B

## App Route Table
- 0.0.0.0/0 → NAT Gateway
- Associated with App-A and App-B

## DB Route Table
- Local route only
- No internet route
- Associated with DB-A and DB-B
