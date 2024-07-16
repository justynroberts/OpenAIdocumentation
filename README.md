# GenAI Documentation Assistant for Rundeck

## Description

The GenAI AutoDocumentation is a Rundeck job that automates the process of creating and updating documentation for Rundeck jobs using OpenAI's GPT models. This tool can significantly streamline your documentation workflow by:

1. Fetching job definitions from a Rundeck server
2. Generating new documentation based on the job definition using OpenAI
3. Updating the job's description in Rundeck with the new content
4. Optionally uploading the generated documentation to Confluence

This automation helps maintain up-to-date, comprehensive documentation for your Rundeck jobs with minimal manual effort.

## Prerequisites

Before using this job, ensure you have:

- An active Rundeck instance with at least one accessible job
- A valid OpenAI API token
- Python environment with the `requests` and `openai` libraries installed
- (Optional) Confluence access if you plan to upload documentation there

## Setup

1. Import the provided JSON file into your Rundeck instance.
2. Configure the job options (see below) according to your environment.
3. Ensure your Rundeck server has the necessary Python environment and libraries installed.

## Job Options

| Option Name | Description | Default Value |
|-------------|-------------|---------------|
| Job UUID | The UUID of the Rundeck job to document | N/A |
| OpenAI API Token | Your OpenAI API token | N/A (Stored securely) |
| RBA TOKEN | Your Rundeck API token | N/A (Stored securely) |
| Runbook Automation Server | URL of your Rundeck server | http://sparks.local:4440 |
| Upload to Confluence? | Whether to upload docs to Confluence | No |
| Confluence Server | Your Confluence server URL | YOUR CONFLUENCE URL |
| Confluence Username | Your Confluence username | youruser@company.com |
| Confluence Token | Your Confluence API token | N/A (Stored securely) |
| Confluence Space | Your Confluence space key | CD |
| OpenAI Model | The GPT model to use | gpt-4o |

## Usage

1. Navigate to the job in your Rundeck instance.
2. Fill in the required options, particularly the Job UUID and API tokens.
3. Run the job.
4. The job will fetch the specified job's definition, generate new documentation, update the job in Rundeck, and optionally upload to Confluence.

## Features

- Automatic documentation generation using OpenAI's GPT models
- Seamless integration with Rundeck for fetching and updating job definitions
- Optional Confluence integration for centralized documentation storage
- Customizable OpenAI model selection
- Secure handling of API tokens

## Disclaimer

This Rundeck job and its documentation are provided "as is" without warranty of any kind, express or implied. Users assume all risks associated with its use. The creators or contributors are not liable for any damages or liabilities arising from the use of this job.

## Contributing

Contributions to improve the GenAI Documentation Assistant are welcome. Please feel free to submit issues or pull requests on the GitHub repository.

## License

This project is licensed under the MIT License. See the LICENSE file in the repository for full details.
