# ruleset-approval-test

Throwaway repo. It exists to answer one question:

> Does an approving review submitted by a **GitHub App** satisfy a repository
> ruleset's `required_approving_review_count`, or does GitHub discount it the
> way it discounts Copilot reviews?

`main` carries a ruleset requiring one approving review, plus deletion and
force-push protection.

`.github/workflows/try-app-merge.yml` mints an App installation token, tries to
merge before approving (expected to fail), approves as the App, then tries again.

Delete this repo and the App once the answer is recorded.
