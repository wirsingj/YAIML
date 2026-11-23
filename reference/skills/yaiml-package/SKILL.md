---
name: yaiml-package
description: Package a project so someone else can run it with one click or minimal setup; use for requests to compile, export, bundle or make an app shareable for a recipient.
metadata:
  yaiml-revision: "0.58.6fc252752496e657"
---

# yaiml-package

Follow the [shared loop](../../YAIML_GUIDE.md), reusing current context. Turn the working project into a deliverable another person can launch without understanding its development environment. The running agent chooses and executes the technical approach using its expertise, project evidence and appropriate tool documentation. YAIML supplies no compiler, packaging runtime or language-specific recipe catalog. A compile-only or export-only request retains its narrower scope.

## Establish The Recipient Experience

Infer what you can from the request and existing project procedures. Resolve consequential unknowns: recipient operating system and architecture, intended task, offline needs, and restrictions on installation or administrator access. Ask only for missing facts that change the deliverable; continue independent preparation while waiting. Do not silently treat the developer's machine as the recipient's platform.

Define success in recipient terms: what they receive, what they open, and what useful result they should see. Separate first-use steps from subsequent launches. One click is the target, not a promise that hides extraction, installation, accounts, downloads or trust prompts. Preserve explicit format/platform choices and existing working packaging unless evidence justifies a change.

## Choose And Build

Inspect actual entry points, build configuration, dependencies, assets, configuration and existing release instructions. Choose the simplest practical delivery form for the recipient: for example a portable application, installer, folder with a launcher, or an authorized hosted link. Explain the choice briefly and carry it through to a usable artifact, rather than stopping at commands or advice. Do not add an application framework or redesign the product merely to package it.

Use tools suited to the actual stack; verify unfamiliar or changing tool behavior from authoritative documentation when needed. Keep build-time requirements separate from recipient requirements. Account for runtimes, native libraries, external services and required data. Cross-compilation or a successful build does not prove execution on the target platform. If the environment cannot produce the requested artifact, finish useful permitted preparation and identify the precise remaining build step without calling source files a finished package.

Keep packaging repeatable in the project's established build/release location, using a small script or configuration when useful. Keep deliverables outside memory. Stage the required files deliberately; exclude secrets, developer credentials, private data and irrelevant checkout contents, while preserving required dependency notices. Provide safe configuration defaults or an explicit first-use configuration path; never embed the developer's credentials to make launch seem effortless.

Ensure the launch path works from the delivered location, independent of the checkout, shell working directory and developer-specific paths. For an interactive tool, keep input, results and actionable errors accessible; a window that immediately disappears is not a usable launch experience. For a local service, handle readiness, user access and shutdown as needed. Store user data in an appropriate writable location and preserve it across relaunches.

Existing authority governs installation, signing, uploads, hosting costs and publication; packaging alone does not authorize public deployment or sending the artifact to someone. Complete authorized local work before requesting any missing external-action approval. Do not bypass operating-system protections to meet the click target; report signing or distribution requirements honestly.

## Verify The Handoff

Test the actual deliverable after its intended transfer/extraction/install steps, in a separate location. Launch through the recipient entry point, perform the intended useful action, close and relaunch it, and check output/data persistence when relevant. Exercise offline behavior when promised. Check likely hidden dependencies such as an activated environment, installed runtime, cached assets or a service running only on the developer's machine.

Prefer an available clean target environment or suitable existing sandbox. Do not alter the developer's system to simulate a clean machine. Where target execution or graphical launch is unavailable, perform feasible artifact and dependency checks and distinguish them from an observed recipient launch. Record the artifact identity, tested platform/environment, actual actions and outcomes. Fix packaging failures and retest the changed deliverable; avoid unlimited retries or unrelated product repairs when a prerequisite is blocked.

## Deliver And Remember

Provide the artifact or authorized live link, supported target, shortest accurate launch instructions, first-use requirements, and actual verification limits. Include only useful troubleshooting and any known service/account dependency. Report separately whether the artifact was built, launched locally, tested in a clean target environment, or actually received by another person. Do not claim universal portability or literal one-click use without evidence.

Maintain material packaging knowledge in its existing project owner: build entry point, chosen approach and rationale, recipient requirements, configuration/data locations, tested targets and unresolved limits. Keep transient build logs out of current memory. Future packaging should reuse that knowledge and recheck the changed artifact, not repeat discovery or inherit an old test result as a new pass.
