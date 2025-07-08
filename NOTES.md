# Manual Setup Guide: GuardDuty to Email Alerting

### Step 1: Enable GuardDuty
- Go to AWS Console → Search GuardDuty
- Click “Enable”
- Now AWS monitors for suspicious activity (DNS, EC2, etc.)

---

### Step 2: Create an SNS Topic
- Go to SNS → Topics → Create topic
- Type: Standard
- Name: GuardDutyTopic

---

### Step 3: Create an Email Subscription
- SNS → Your Topic → Create Subscription
- Protocol: Email
- Endpoint: your email address
- Confirm the email you receive from AWS

---

### Step 4: Create EventBridge Rule
- Go to EventBridge → Rules → Create Rule
- Pattern: use `event-pattern.json`
- Target: SNS topic

---

### Step 5: Testing (Optional)
- Edit the rule temporarily to use source: `test.guardduty`
- Go to EventBridge → Event buses → default → Send events
- Use the content in `test-event.json`
- You will receive an email alert

---

### Step 6: Revert Rule to Real GuardDuty
- Change event pattern back to source: `aws.guardduty`

---

✅ All done — real GuardDuty findings will now trigger email alerts!
