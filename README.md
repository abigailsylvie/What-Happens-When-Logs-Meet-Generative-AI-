# Log Analysis with AWS CloudWatch and Generative AI

## Overview
This project demonstrates how to use AWS services such as CloudWatch, Lambda, and Amazon Bedrock to analyze and summarize logs. By combining native log management with generative AI, the solution provides clear insights from raw log data, reduces noise, and highlights anomalies or security-relevant events.

## Architecture
1. **CloudWatch Logs**  Collects and stores log data from various AWS services.
2. **Lambda Function** Processes the logs and invokes Amazon Bedrock.
3. **Amazon Bedrock**  Generates summaries and insights from the logs using a large language model.
4. **CloudWatch Custom Widgets** Displays summarized results in a clear and accessible format.

**Flow:**  


## Features
- Automatic summarization of log events.
- Anomaly and security findings detection.
- Flexible prompts for different use cases (e.g., ignore 200 OK responses, detect cost anomalies).
- CloudWatch custom widget for visualization of AI-generated insights.

## Deployment
The solution is deployed using an AWS CloudFormation template.

1. Deploy the CloudFormation stack in your AWS account.
2. Provide the ARN of the log group you want to analyze.
3. Once deployed, configure a CloudWatch dashboard with a custom widget that calls the Lambda function.
4. Logs will be summarized automatically in the dashboard.

## Example Use Cases
- Identify failed login attempts from authentication logs.
- Highlight unusual activity in CloudTrail logs.
- Detect potential cost anomalies from billing-related events.
- Summarize application errors for quick troubleshooting.

## Requirements
- AWS account with permissions to use CloudWatch, Lambda, Bedrock, and CloudFormation.
- Log group ARN from CloudWatch to analyze.
- Standard access tier logs (required for `GetLogEvents` API).

## Future Enhancements
- Integration with additional log sources.
- Custom prompts tailored to organization-specific requirements.
- Support for custom-trained models for specialized log analysis.

## Conclusion
This project shows how combining AWS CloudWatch with Generative AI can transform raw log data into actionable insights, making investigations faster and more efficient.
