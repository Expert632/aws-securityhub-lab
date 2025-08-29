# aws-securityhub-lab
Practical labs : Enable AWS Security Hub to Centralize AWS Security


-Objective

The goal of this lab is to **enable AWS Security Hub** in an AWS account to gain 

centralized visibility into security alerts, compliance status, and security posture across 

multiple AWS services.

---

-Prerequisites

* An active **AWS account**
* AWS Management Console or AWS CLI installed locally
* IAM user/role with **AdministratorAccess** or equivalent permissions

---

-Steps to Reproduce

  1. Sign in to AWS Console

* Go to [AWS Console](https://console.aws.amazon.com/)
* Log in with your credentials

  2. Open Security Hub

* In the AWS Console search bar, type **"Security Hub"**
* Click on **Security Hub**

  3. Enable Security Hub

* Click **Enable Security Hub**
* Select:

  * **Enable default standards (CIS AWS Foundations Benchmark, PCI DSS, AWS 

Foundational Security Best Practices)**
  * Or **customize** by choosing only the standards you want
* Click **Enable**

  4. Review Findings

* After enabling, go to **Findings** in the left-hand menu
* Review automatically generated security alerts from:

  * GuardDuty
  * Inspector
  * IAM Access Analyzer
  * And other integrated AWS services


  5. (Optional) Multi-Account Setup

* If managing multiple AWS accounts:

  * Designate a **master account** for Security Hub
  * Invite member accounts to aggregate findings in one place

  6. (Optional) Automate with AWS CLI

  -You can also enable Security Hub via CLI:

```bash
aws securityhub enable-security-hub \
  --enable-default-standards
```

  -Check findings:

```bash
aws securityhub get-findings
```

---

-Expected Results

* Security Hub is successfully **enabled**
* Default security standards (CIS, PCI DSS, AWS Best Practices) are active
* Security findings are visible in the **dashboard**
* (Optional) Multi-account visibility is centralized

---

-Key Takeaways

* Security Hub provides a **single pane of glass** for AWS security monitoring
* Helps meet **compliance requirements** (CIS, PCI DSS, etc.)
* Integrates with GuardDuty, Inspector, and other AWS security services

---

-Repository Structure

```
├── Lab-02-AWS-SecurityHub/
│   ├── README.md        # Documentation (this file)
│   ├── screenshots/     # Screenshots of each step (to be added)
│   ├── cli-commands.sh  # Optional automation script
```



