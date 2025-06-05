# Introduction to AWS platform

## Some basic things while you use AWS

- Always set your AWS Budget

- Check your free tier limit : There is always free tier available - To check - Click your name at top right -> My billing Dashboard -> Billing Preferences -> Click receive free tier usage alerts and give your email address

- Set IAM user, dont use the root user always

## Setting up Cloudwatch

- Goto Cloudwatch -> Left column -> Billing -> Create Alarm
- Select metric -> Billing -> Total estimated charge -> USD
- Threshold TYpe: Static, than 50, period 6 hrs -> Next
- In Alarm, Create new topic, My billing alarm (Topic name), Email endpoint - give your email -> Click create topic
- Goto your email and verify
- Next Name - Give some name and then click create

## Create MFA

- Login as Root user
- Go to IAM -> Add MFA for root user
- Virtual MFA device and finish the procedure



