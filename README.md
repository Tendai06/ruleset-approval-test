# ruleset-approval-test

Throwaway repo. It exists to answer one question:

> Does an approving review submitted by a **GitHub App** satisfy a ruleset's
> `required_approving_review_count`, or does GitHub discount it the way it
> discounts Copilot reviews?

The `main` branch carries a ruleset that mirrors `jamf`'s org ruleset
`Simple branch protection` (id 8849721) rule-for-rule, including
`require_extra_approval_for_unattributed_changes: true`.

`.github/workflows/try-app-merge.yml` mints an App installation token, tries to
merge before approving (expected to fail), approves as the App, then tries again.

Delete this repo and the App once the answer is recorded.
