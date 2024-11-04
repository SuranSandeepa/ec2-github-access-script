# GitHub Repository Access Checker

This project is a Bash script that interacts with the GitHub API to list users who have read access to a specified GitHub repository. 

The script is designed to work in an EC2 environment, allowing users to check collaborator access on repositories remotely. This is useful for auditing and managing access control for repositories on GitHub.

## Project Overview

- **Developed on**: EC2 instance, connected via Git Bash
- **Key Tools**: Bash, GitHub API, `jq` for JSON parsing
- **Purpose**: List users with read access to a specific GitHub repository
- **Authentication**: GitHub username and Personal Access Token (PAT) for authenticated API requests

### Script Details

The script makes a `GET` request to the GitHub API, retrieves a list of collaborators, and filters users who have read (pull) access to the specified repository.

### Prerequisites

1. **Environment**: Run on an EC2 instance, accessed through SSH from Git Bash.
2. **Git Installation**: Git must be installed on the EC2 instance.
3. **GitHub Credentials**: Set up your GitHub username and Personal Access Token (PAT) as environment variables (`GITHUB_USERNAME` and `GITHUB_TOKEN`).
4. **jq**: JSON parsing utility is required to process API responses. Install it on your EC2 instance with `sudo apt install jq`.
