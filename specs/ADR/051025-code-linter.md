# Code Linter
*Date:* 5/10/2025

## Context / Problem
As our team scales, we need a consistent and scalable way to ensure code quality. Relying solely on tools or a single person is risky, and we need a method that balances thoroughness with workflow efficiency.

## Options Considered
- *Manual review scaling with issue size:* Require 1, 2, or 3 reviewers based on whether the issue is small, medium, or large.
- *Designated DevOps reviewer:* One person (or team) handles all merge approvals and linting enforcement.

## Decision & Outcome
We chose the manual review system with variable approval counts depending on issue size:
- Small: 1 reviewer
- Medium: 2 reviewers
- Large: 3 reviewers

## Pros & Cons

- *Pros:*
  - Reduces bus factor risk
  - Brings multiple perspectives to critical code
  - Encourages team-wide code familiarity

- *Cons:*
  - Merge times may increase
  - Asynchronous review process may slow overall progress
