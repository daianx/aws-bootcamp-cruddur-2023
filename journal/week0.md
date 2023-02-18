# Week 0 — Billing and Architecture

#### LucidChart Diagrams:
LucidChart Conceptual Diagram: https://lucid.app/lucidchart/5cf8555a-fa10-491f-9ca3-0296e9cdfdb8/edit?viewport_loc=-2883%2C-1345%2C2219%2C1103%2C0_0&invitationId=inv_25bcae99-9a50-4a9c-b0f6-1bd049494563
LucidChart Logical Diagram: https://lucid.app/lucidchart/1979ef9d-82b2-4682-ae06-7d4941c4180e/edit?viewport_loc=-11%2C-24%2C2219%2C1103%2C0_0&invitationId=inv_c102f2be-279a-41f1-af38-015265582b00

#### AWS Tasks:

I set the Receive Free Tier Usage Alerts under Billing Preferences.
I created a 0 spend and monthly 5$ budget.

I created an admin user under the Admin group and assigned the AdministrativeAccess policy. I added MFA to this account and set a password for console access.

I also activated Cloud Shell. I added AWS CLI to Gitpod using:

```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

I added the AWS_ACCESSKEY_ID, AWS_SECRET_ACCESS_KEY and AWS_DEFAULT_REGION as environmental variables and gp environmental variables.


I added the following lines to .gitpod.yml:
```
tasks:

  - name: aws-cli

    env:

      AWS_CLI_AUTO_PROMPT: on-partial

    init: |

      cd /workspace

      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

      unzip awscliv2.zip

      sudo ./aws/install

      cd $THEIA_WORKSPACE_ROOT
```


