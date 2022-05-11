# My Serverless Architecture

## Processing flow
::: mermaid
graph LR;
classDef s3 fill:#4A902A,stroke:#333,stroke-width:4px,color:#fff;
classDef lam fill:#dc6c11,stroke:#333,stroke-width:4px,color:#fff;
classDef rds fill:#3c48cc,stroke:#333,stroke-width:4px,color:#fff;
classDef ses fill:#6980e9,stroke:#333,stroke-width:4px,color:#fff;
classDef sns fill:#DD3070,stroke:#333,stroke-width:4px,color:#fff;
classDef api fill:#8450e1,stroke:#333,stroke-width:4px,color:#fff;

A01(API Gateway):::api --> B01(Lambda:Function 1):::lam
B01 --> C01[\S3:Bucket 1/]:::s3
C01 --> D01(Lambda:Function 2):::lam ;
D01 --Stored Procedure--> E01[(RDS:My Instance)]:::rds
C01 --> F01[/SNS:Alert Topic/]:::sns
F01 -.ben AT alerts.com.-> G01((SES:Email)):::ses
:::