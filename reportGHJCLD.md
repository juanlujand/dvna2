# Your Gitgat Account Security Audit
This report is the output of Gitgat, an experimental open source audit tool that will assist you in improving the security of your GitHub account.
This report is a user-view report, and includes all organizations that the user belongs to.

# Overview

Gitgat automatically analyzes GitHub account and points to potential gaps as compared to security configuration best practices.
As the project matures additional automated analyses will be added.

## Repository Public Visibility and Access
### Motivation
Public GitHub repositories enable open source collaboration.
But mistakenly exposing a private repository as public
may leak information and allow unwanted people access to your repositories.

### Key Findings
| Owner | Findings |
| --- | --- |


See [below](#repository-public-visibility-and-access-1) for a detailed report.

### Our Recommendation
Regularly review your repositories to ensure private repositories have not been made public.

Managing repositories visibility can be done through the following links:
<details>
<summary>Click to expand</summary>


</details>

## Two Factor Authentication
### Motivation
2 factor authentication protects your account from credential theft.

### Key Findings
(v) no organization has members with two factor authentication disabled.

(v) all organizations have overall enforcement.

See [below](#two-factor-authentication-1) for a detailed report.

### Our Recommendation
Require all users in your GitHub organization to turn on 2 factor authentication.
They can do it from the following link: <https://github.com/settings/security>.

Configure your GitHub organizations to enforce 2 factor authentication on all organizations’ users.
That can be done from the following link(s):
<details>
<summary>Click to expand</summary>


</details>

## Admin Permissions
### Motivation
Admin permissions allow full control over your organization.
Excessive admin permissions may be exploited, intentionally or unintentionally.
Limiting permissions will limit the potential damage of credential theft, account-takeover or developer-workstation-takeover.

### Key Findings
The following organizations do not have 2 admin members:
None

See [below](#admin-permissions-1) for a detailed report.

### Our Recommendation
Review the permissions and limit the number of users with admin permissions, to the minimum required.
You can limit the administrative permissions of members at the following links:
<details>
<summary>Click to expand</summary>


</details>

## Teams
### Motivation
Excess permissions may be exploited, intentionally or unintentionally.
Limiting permissions will limit the potential damage of credential theft, account-takeover or developer-workstation-takeover.

### Key Findings
(v) no teams are configured in the organizations.

(v) no teams with admin permissions are found.

See [below](#teams-1) for a detailed report.

### Our Recommendation
Review the permissions for team members according to our recommendations below.
Remove team members who are not active or are no longer on the team.
You can manage team permissions at the following links:
<details>
<summary>Click to expand</summary>


</details>

## Collaborators
### Motivation
Collaborators are people outside of the organization who are active in your repositories.

### Key Findings
(v) your repositories do not have out of organization collaborators.

See [below](#collaborators-1) for a detailed report.

### Our Recommendation
Regularly review the collaborators of your repositories, and block users that are not collaborators anymore.
Blocking members is done through the following links:
<details>
<summary>Click to expand</summary>


</details>

## Branch Protection
### Motivation
Branch protection are specific protection mechanisms that limit users from making dangerous modifications of your repositories.
Branch protection rules include requiring pull-request reviews, signed commits and limiting deleting history.
GitHub Branch protection rules are detailed at the following link:
<https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches>.
Branch protection is managed at the repository-branch level.

### Key Findings
(v) all branches are protected.

(i) no branches are protected.

See [below](#branch-protection-1) for a detailed report.

### Our Recommendation
You should configure branch protection for the main branches of your repositories.
Branch protection rules for these branches should include requiring pull-request-reviews, signed commits, and not allowing deletions.
This can be done from the following links:
<details>
<summary>Click to expand</summary>


</details>

## Signed Commits
### Motivation
Signing commits prevents unauthorized people from committing code into your repositories.
In case you have not deployed appropriate branch protection rules,
the following findings display the signing status of individual commits.

### Key Findings
(i) no data was fetched. The module needs configuration. Add the configuration section to the input file: 'commits': { '<owner/repo>': 'allow_unverified': [], ''history: [] }

See [below](#signed-commits-1) for a detailed report.

### Our Recommendation
You should either configure branch protection rules to enforce signed commits, or require developers to sign their commits.
Instructions for configuring your local git installation to sign commits to work with GitHub can be found here:
<https://docs.github.com/en/authentication/managing-commit-signature-verification/signing-commits>

## Deploy Keys
### Motivation
Deploy keys are an authentication tool to enable access to repositories.
Manage your deploy keys to ensure you have not left keys that can be wrongfully used.
GitHub’s explanation about deploy keys can be found here:
<https://docs.github.com/en/developers/overview/managing-deploy-keys#deploy-keys>


### Key Findings
(v) no new keys.

(v) no keys are expired.

See [below](#deploy-keys-1) for a detailed report.

### Our Recommendation
Deploy keys are SSH keys assigned to each repository that allow reading and (optional) writing to private repositories.
We recommend you review your SSH keys regularly; ensure you are familiar with the keys and their use.
In case of an upcoming expiration date - ensure you replace the keys on time.
Deploy keys can be managed at the following links:
<details>
<summary>Click to expand</summary>


</details>

## SSH Keys
### Motivation
SSH keys are an authentication tool that enables tools like git to access repositories you have access to.
In GitHub personal and organizational accounts, SSH keys are managed by the user.
Thus the following are findings regarding *your* SSH keys.

### Key Findings
(v) no new keys.

(v) no keys have expired.

See [below](#ssh-keys-1) for a detailed report.

### Our Recommendation
Your SSH keys allow full access to all the repositories over SSH.
We recommend you review your SSH keys regularly; ensure you are familiar with the keys and their use.
In case of an upcoming expiration date - ensure you replace the keys on time.
SSH keys generation is done via the following link: <https://github.com/settings/keys>.

## Fine Grained File Access Tracking

### Motivation

In many cases your repository includes sensitive files,
such as CI pipeline and IaC definitions. You should manage
who’s allowed to modify these files. To use this rule, configure
the file-name patterns of the files you want to track.

### Key Findings
There are no violating commits.

See [below](#fine-grained-file-access-tracking-1) for a detailed report.

### Our Recommendation

# Detailed Results
## Repository Public Visibility and Access
Public GitHub repositories enable open source collaboration.
But mistakenly exposing a private repository as public
may leak information and allow unwanted people access to your repositories.
Regularly review your repositories to ensure private repositories have not been made public.

Go [back](#repository-public-visibility-and-access) to the overview report.

<details open>
<summary> <b>Repositories Visibility Settings (for Public Repositories)</b> </summary>

No public repositories.
</details>

## Two Factor Authentication
2 factor authentication protects your account from credential theft.
Require all users in your GitHub organization to turn on 2 factor authentication.
They can do it from the following link: <https://github.com/settings/security>.

Configure your GitHub organizations to enforce 2 factor authentication on all organizations’ users.

Go [back](#two-factor-authentication) to the overview report.

<details open>
<summary> <b>Two Factor Disabled Members</b> </summary>

All members in all organizations have two factor authentication enabled.
</details>

<details open>
<summary> <b>Two Factor Unenforced Organizations</b> </summary>

All organizations enforce two factor authentication on their members.
</details>

## Admin Permissions
Admin permissions allow full control over your organization.
Excessive admin permissions may be exploited, intentionally or unintentionally.
Limiting permissions will limit the potential damage of credential theft, account-takeover or developer-workstation-takeover.
Review the permissions and limit the number of users with admin permissions, to the minimum required.

Go [back](#admin-permissions) to the overview report.

<details open>
<summary> <b>Admin Members</b> </summary>

None
</details>

## Teams
Excess permissions may be exploited, intentionally or unintentionally.
Limiting permissions will limit the potential damage of credential theft, account-takeover or developer-workstation-takeover.
Review the permissions for team members according to our recommendations below.
Remove team members who are not active or are no longer on the team.

Go [back](#teams) to the overview report.

<details open>
<summary> <b>Members</b> </summary>

None
</details>

<details open>
<summary> <b>Teams Permissions</b> </summary>

None
</details>

## Collaborators
Collaborators are people outside of the organization who are active in your repositories.
Regularly review the collaborators of your repositories, and block users that are not collaborators anymore.

Go [back](#collaborators) to the overview report.

<details open>
<summary> <b>Outside Collaborators</b> </summary>

None
</details>

## Branch Protection
Branch protection are specific protection mechanisms that limit users from making dangerous modifications of your repositories.
Branch protection rules include requiring pull-request reviews, signed commits and limiting deleting history.
GitHub Branch protection rules are detailed at the following link:
<https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches>.
Branch protection is managed at the repository-branch level.
You should configure branch protection for the main branches of your repositories.
Branch protection rules for these branches should include requiring pull-request-reviews, signed commits, and not allowing deletions.

Go [back](#branch-protection) to the overview report.

<details open>
<summary> <b>Branch Protection</b> </summary>

None
</details>

<details open>
<summary> <b>Unprotected Branches</b> </summary>

None
</details>

## Deploy Keys
Deploy keys are an authentication tool to enable access to repositories.
Manage your deploy keys to ensure you have not left keys that can be wrongfully used.
GitHub’s explanation about deploy keys can be found here:
<https://docs.github.com/en/developers/overview/managing-deploy-keys#deploy-keys>

Deploy keys are SSH keys assigned to each repository that allow reading and (optional) writing to private repositories.
We recommend you review your SSH keys regularly; ensure you are familiar with the keys and their use.
In case of an upcoming expiration date - ensure you replace the keys on time.

Go [back](#deploy-keys) to the overview report.

<b>Expired</b>

None

<b>All</b>

None

## SSH Keys
SSH keys are an authentication tool that enables tools like git to access repositories you have access to.
In GitHub personal and organizational accounts, SSH keys are managed by the user.
Thus the following are findings regarding *your* SSH keys.
Your SSH keys allow full access to all the repositories over SSH.
We recommend you review your SSH keys regularly; ensure you are familiar with the keys and their use.
In case of an upcoming expiration date - ensure you replace the keys on time.
SSH keys generation is done via the following link: <https://github.com/settings/keys>.

Go [back](#ssh-keys) to the overview report.

<b>Expired</b>
None

<b>All</b>
None


