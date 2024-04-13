# Week 0 — Billing and Architecture

Create budget for ourself:

aws budgets create-budget \
    --account-id $AWS_ACCOUNT_ID \
    --budget file://aws/json/budget.json \
    --notifications-with-subscribers file://aws/json/notifications-with-subscribers.json


aws sns subscribe \
    --topic-arn="arn:aws:sns:us-east-2:936368949982:billing-alarm" \
    --protocol=email \
    --notification-endpoint=mjresch19@gmail.com

    