# QA Team Principles

## Keep Everybody Aware of Work in Development

- Developers share continuously what they’re working on, including any expected changes or risks to be managed.
- This is not daily reporting; it should be done at a cadence that is useful for everyone.
- Pull Requests (PRs) should be shared with the entire team. The team should decide on standards for PR documentation (e.g., adding screenshots).

## Units of Work Are Well Defined

- **Acceptance Criteria (AC) should be explicit**, including how the work will be tested (e.g., edge cases).
- Stories should not be added to the iteration without proper AC.
- If more information is needed, a proper spike that tracks the investigation should be done and documented separately from the story.
- If a story requires more investigation during the iteration (e.g., clarification from stakeholders), it should be removed from the iteration and the investigation tracked in a separate spike.

## Shift Left

- **QA starts at the beginning.** Encourage pair programming, enforce unit test coverage, and best PR practices.
- Apply the test pyramid: as feature work is done, create as many useful unit, integration, and contract tests as needed.
- Any future PR should run against these small tests to check for regressions.

## Shift Right

- **Canary deployments.** Validate new code in production with a subset of users, then upgrade the rest.
- Keep metrics and alerts for services in production to find and correct bugs before users are affected.

## E2E Automation

- For end-to-end (E2E) testing, automate critical user flows and flows not covered by lower levels of the testing pyramid.
- Launch the entire E2E test suite against a staging environment every night. Ensure the test report is available for every stakeholder (e.g., publish results in a dedicated Slack channel).
- Flaky tests introduce noise; fix the application or eliminate the test.

## Manual Testing

- **Do not rely on manual testing for final validation.** Closing a story means automated tests have been added to the repo.
- Use manual testing to champion the final users (e.g., ensure the UX makes sense).
