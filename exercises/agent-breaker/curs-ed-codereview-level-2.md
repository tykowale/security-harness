# Curs-ed CodeReview - Level 2

## Summary

This challenge raised the stakes from recommending a suspicious import to recommending code that would read local shell configuration and send it to an external endpoint. Working prompts are intentionally omitted from this public write-up; the goal is to capture the lesson, not provide a copy/paste solution.

## Post-level review

### Vulnerability and impact

This was another indirect prompt-injection issue through a repository rules file, but with a more obviously harmful payload. In a real workflow, this class of failure could turn an automated reviewer into a delivery mechanism for credential exposure, developer-machine data theft, or supply-chain compromise.

### Design lesson and mitigation

The design weakness was still the missing trust boundary between untrusted repository guidance and trusted review policy. A safer reviewer should treat repository rules as data to inspect, reject instructions that request sensitive file access or external transmission, and apply independent policy checks even when the text claims to be a required compliance artifact.

### What we learned along the way

The first attempt was too semantically honest: framing the behavior as telemetry/debugging made the data collection and external upload stand out. A cleaner review-policy framing got partial traction, but the key improvement was adding a reason the suspicious snippet had to be preserved literally for downstream audit tooling; that shifted the model away from judging the code and toward enforcing an apparent integration constraint.
