# Lesson 01 · Conversation evidence

AI-drafted summary for STUDIO-001. Learner statements are quoted or paraphrased below.

## Prediction

> DNS points the calculator hostname to my DigitalOcean server. Traefik terminates HTTPS and routes traffic over the existing Docker network to the calculator container.

## Check interpretation

Learner paraphrase: HTTP 400 shows the divide-by-zero request was rejected. It does not establish that all invalid inputs are handled or that all functionality works.

## Browser observation

Pending. The learner did not personally test 6 × 7 in the deployed calculator. Automated API and browser results are separate from this observation.

## Keep decision

Learner paraphrase: Keep the deployed calculator based on the verified automated checks, with the personal browser test still pending.

## AI assistance

AI prepared and ran the deployment, verified HTTPS and API behavior, checked that existing services stayed healthy, and drafted this summary from the learner’s statements. See [launch evidence](studio/evidence.json) and [passing PR CI](https://github.com/yungjorge/my-server-studio/actions/runs/42335741107).

## Review

The learner reviewed and approved this summary for publication on November 6, 2026.
