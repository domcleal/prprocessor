# Pull Request Processor for Foreman

prprocessor is a web service which receives GitHub webhooks/notifications and helps sync PRs to Redmine and Jenkins.

Documentation available [on the Foreman wiki](http://projects.theforeman.org/projects/foreman/wiki/PrProcessor).

## Environment Variables

* `ENV['GITHUB_OAUTH_TOKEN']`: An OAuth token with repos access to update PR labels
* `ENV['GITHUB_SECRET_TOKEN']`: The secret token for verifying GitHub webhooks
* `ENV['REDMINE_API_KEY']`: Redmine API key to use for making API update
* `ENV['JENKINS_TOKEN']`: Jenkins secret token for activating builds

## Configuration Files

* config/redmine_issue_required_repos.yaml: List of repositories where commit titles must adhere to a standard and include a Redmine issue number.
* config/users.yaml: List of GitHub usernames against Redmine user IDs to automatically assign tickets to PR authors.
