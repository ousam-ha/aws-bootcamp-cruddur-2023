# Week 0 — Billing and Architecture# Week 0 — Billing and Architecture
1. IAM user created --- reset password
2. aws web console
    1. aws --version
    2. aws sts get-caller-identity
2. install aws console GitPod
    1. add access_key_id, secret_access_key, default_region of iam use in env
    2. test
    3. set up gitpod for relaunch with same config
        1. add config in gitpod.yml
            ```yml
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
        2. set gitpod env variables
            ```
                gp env AWS_ACCESS_KEY_ID=zxt
                gp env AWS_SECRET_ACCESS_KEY=xyz
                gp env AWS_DEFAULT_REGION=us-east-1
            ```