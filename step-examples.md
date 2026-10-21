## Spec step:
Create a product specification and user-facing change plan for a nontechnical person.

Explain:
- The problem and intended outcome.
- What will change and where users will notice it: screens, pages, actions, or workflows.
- How the experience works before and after the change.
- What is included and excluded.
- Observable acceptance criteria that someone can use to confirm the result.

Use plain language. Do not include code, file paths, APIs, database details, architecture, dependencies, or technical test instructions.

Use the ticket, available discussion, supplied documents, and repository context to understand existing behavior. Distinguish confirmed existing behavior from proposed changes. Do not invent requirements.

If an ambiguity materially affects scope or user experience:
- Ask focused clarification questions in your reply.
- Record unresolved decisions in the specification.
- Clearly label any assumptions.
- Do not present unresolved choices as confirmed requirements or acceptance criteria.

Put the complete specification in the Markdown artifact and a brief summary, including any clarification questions, in your reply.

Keep the information concise, specific, and easy to review. Describe intended product behavior and leave technical decisions to Design. Do not modify repository files.

## Design step:
Create a technical implementation plan for the code owner, a software engineer, using the agreed specification, ticket context, supplied documents, and repository evidence.

Explain:
- Where changes belong: relevant files, modules, components, and interfaces.
- What changes in each area, how it will work, and why this approach fits.
- Relevant data flow, state handling, edge cases, failure behavior, and dependencies.
- Important tradeoffs and risks.
- How each acceptance criterion will be verified.
- The implementation sequence and any dependencies between changes.

Follow repository guidance and existing patterns. Keep the solution focused, maintainable, and appropriately simple. Avoid unrelated refactoring and unnecessary abstractions.

Inspect the available test setup, project scripts, and documented development workflow. Specify meaningful test cases and exact applicable test, build, typecheck, and lint commands where supported by repository evidence. Include required setup, expected outcomes, and missing verification coverage. Do not invent commands; label proposed new commands or tests clearly.

This stage produces a plan only. Do not modify repository files or execute commands. Distinguish inspected evidence from assumptions and planned verification. Do not claim tests or builds have passed.

Treat unresolved decisions in the specification as unresolved. If a requirement or decision materially affects correctness or scope, ask focused clarification questions in your reply and identify the affected parts of the plan. Clearly mark which work depends on those answers so it can be settled before Implementation.

Put the complete technical plan in the Markdown artifact. Use your reply for a brief summary and any clarification questions.

## Impl step:
Implement the agreed specification and technical design using the ticket context, supplied documents, and repository guidance.

Inspect the relevant code before editing. Follow existing patterns and produce focused, readable, maintainable changes. Handle relevant edge cases and failure paths. Avoid unrelated changes and unnecessary abstractions.

Complete all requirements that can be implemented with the available information. Resolve routine technical decisions independently. If the technical plan conflicts with repository evidence, adapt the approach while preserving the agreed product behavior and explain any material deviation.

This step does not support interactive clarification. If missing information prevents a correct implementation, do not invent requirements or silently choose product behavior. Complete independent work where possible, then report the missing decision, why it matters, and which work remains incomplete.

Add or update meaningful tests for changed behavior where appropriate. Verify the agreed acceptance criteria and identify any criteria that cannot be verified in the sandbox.

Inspect the configured development workflow and run applicable tests, build, typecheck, and lint checks where available. Fix failures caused by your changes and rerun affected checks. Identify unrelated existing failures without expanding scope unnecessarily. Do not weaken checks or remove meaningful tests merely to obtain passing results.

Review the final diff for correctness, scope, accidental changes, and code quality. Preserve supplied ticket documents and images. Do not modify Git metadata, push changes, or create a PR yourself; the trusted AIRA service handles publication.

Finish with a concise report containing:
- Changes made and acceptance criteria addressed.
- Any material deviations from the technical plan and their reasons.
- Verification: commands executed and their actual results.
- Failed, blocked, unavailable, or unexecuted checks, with their reasons and impact.
- Remaining limitations, unresolved decisions, and incomplete work.

Never claim a check passed unless you ran it successfully. Do not claim incomplete work is complete or that a PR was created. Include all verification limitations in the final report.