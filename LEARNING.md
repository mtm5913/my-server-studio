# Lesson 01 · Conversation evidence

AI-drafted task summary, not a transcript or grade. It may be public. Use actual
short quotes or labeled paraphrases, name any help supplied, and link actual
work. Leave missing contributions Pending. A learner can review, correct or
remove excerpts before publication; accuracy approval is not proof of learning.
Label role-play honestly rather than treating it as an actual learner response.

**Lesson:** STUDIO-001. **Available conversation context:** This coaching chat.

## Classroom example

Learner reported: “7 x 8 and got 56” at https://calc.mywebclass.org/.
This describes the classroom example, separately from the learner's deployment below.

## Prediction

Learner initially guessed: “something to do with the docker container?”
After AI asked how Traefik selects a container, learner guessed: “the key?”
AI explained DNS, HTTPS, hostname routing, and the separate purpose of SSH keys,
then expanded the explanation using a building/receptionist analogy on request.
An independent explanation of the full request path remains Pending.

## Check interpretation

Learner said the division-by-zero check “doesn't tell us what happens when
dividing by a number that isn't 0,” correctly identifying an untested case.
Learner clarified that “works” meant the expected rejection matched the actual
result. AI initially misread that wording as meaning the division succeeded;
this was not a correction of the learner's understanding of HTTP 400.

## Browser observation

At https://calc.megan373lab.xyz/, learner tried 8 ÷ 2 and reported:
“browser and api print out 4.” AI suggested this input after the check discussion.

## Keep decision

Learner chose to keep the deployment because 8 ÷ 2 returned the correct result
in both outputs, while noting that more testing would help confirm it works
(AI paraphrase). This decision is based on one observed calculation, not every case.

## Review

Learner reviewed the summary, requested the wording correction recorded above,
then approved the revised summary and authorized a commit in this chat.
This approval establishes record accuracy, not independent understanding.

## AI work and next step

AI helped configure GitHub SSH access, cloned the learner's repository over SSH,
and completed the prepared setup with Python 3.13.1. A read-only server check
found Docker, an existing Traefik container on ports 80/443, and the hosting-web
network. Learner chose calc.megan373lab.xyz and reported saving its DNS record;
AI confirmed it resolves to the intended server. The prepared read-only doctor
returned ready for launch-new. After explicit plan approval, AI created
[issue #1](https://github.com/mtm5913/my-server-studio/issues/1), launched the
pinned image, and verified trusted HTTPS, release identity, valid/invalid API
cases and preservation of nine existing containers. See [SPEC](SPEC.md),
[initial launch evidence](studio/launch-evidence.json) and
[latest verification](studio/evidence.json).
AI browser check of 6 × 7 showed 42 in both outputs. Prepared fast checks passed
(91 tests); two E2E tests were deselected because the laptop Docker daemon was
unavailable. [Full PR CI](https://github.com/mtm5913/my-server-studio/actions/runs/40956101078) passed, including the real-image E2E checks. AI supplied the routing explanation
and initially misread the learner's wording about the successful rejection check;
the learner clarified the intended meaning. No independent full request-path
explanation was recorded.
GitHub completion: the reviewed record was published; [PR #2](https://github.com/mtm5913/my-server-studio/pull/2) merged into `main`, issue #1 closed, and [post-merge CI](https://github.com/mtm5913/my-server-studio/actions/runs/40957504942) passed all three jobs. Next: submit the repository for instructor review.
