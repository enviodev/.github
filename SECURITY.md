# Security Policy

Envio builds blockchain data infrastructure: HyperIndex, HyperSync, HyperRPC, and
Envio Cloud. We take reports about the security of these products seriously, and we
appreciate the people who take the time to tell us about a problem properly.

This is a coordinated vulnerability disclosure policy. Envio does not run a public
bug bounty programme.

## How to report

Email **security@envio.dev**.

For issues in a specific open-source repository, you may instead use GitHub's private
vulnerability reporting ("Report a vulnerability" in the repository's Security tab).
Either channel reaches the same people.

Please do not report security issues through public GitHub issues, the support
widget, Discord, Telegram, or social media. Those channels are public or
support-facing and are not monitored for security reports.

## What a useful report contains

We can only act on reports that let us reproduce the problem. Please include:

- The affected product, and the exact URL, endpoint, package version, or commit.
- A clear description of the vulnerability and what an attacker can actually do with
  it. Describe the impact concretely: whose data, which account, what action.
- Step-by-step reproduction instructions, with the requests, payloads, or code
  needed to follow them. A short proof-of-concept script or a minimal video is ideal.
- Anything you noticed about scope: how many accounts or projects this would affect,
  and whether it needs a valid account, a specific role, or user interaction.
- If you used automated tooling, tell us which. Raw scanner output on its own is not
  a report; we need the demonstrated impact.

Reports in English are easiest for us to handle quickly.

If you are not sure whether something is a real issue, send it anyway with what you
have. A short, specific "here is the request, here is the response, here is why I
think it matters" is worth far more to us than a long report with no reproduction.

## What to expect from us

- We acknowledge every report, sent by either channel above, within **3 business
  days**.
- We give you our initial assessment, including whether we consider the report valid
  and in scope, within **10 business days** of acknowledgement.
- While an accepted issue is open, we update you at least every **30 days**, and we
  tell you when it is fixed.

These are the timelines we commit to keeping, not our targets. In practice we
usually respond faster, and a report that shows real, demonstrated impact gets
attention the same day.

We will not respond to follow-ups asking for a payment quote before we have assessed
the report, and we do not negotiate over reports whose details have not been shared.

## Scope

In scope:

- **envio.dev** and its application and API endpoints, including the Envio Cloud
  dashboard and the authenticated APIs behind it.
- **docs.envio.dev**.
- **Publicly reachable HyperSync and HyperRPC query endpoints**, and the
  authentication and quota enforcement in front of them.
- **Hosted indexer endpoints served by Envio Cloud**, but only for a project you own
  or have written permission to test. Notably: anything that lets one customer read,
  modify, or affect another customer's project, data, deployments, tokens, or
  billing.
- **The code we publish**: our public repositories under
  https://github.com/enviodev, and the packages we publish from them (for example
  the `envio` and `@envio-dev/hypersync-client` npm packages, our Rust crates, and
  our Go client libraries).

The kinds of issue we care most about: cross-tenant access of any sort, broken
authentication or authorisation, token or API-key handling flaws, remote code
execution, injection that crosses a trust boundary, escapes from a build or indexer
container to the platform or to another tenant, exposure of customer data or
credentials, and anything that lets someone bypass usage metering or billing at
scale.

## Out of scope

The following are not accepted under this policy. Reports consisting only of the
items below will be closed without a detailed reply.

**Reports without demonstrated impact**

- Output from an automated scanner, linter, or "attack surface" tool with no working
  proof of concept and no explanation of impact.
- Theoretical issues, best-practice opinions, or "this could be exploited if" with
  no demonstration.
- Reports offering to disclose details only after a payment is agreed. We assess
  reports on their merits; we do not negotiate before we have seen them.
- Reports that describe pages, endpoints, parameters, or features that do not exist
  on our systems. If a report does not match our product, we treat it as a template
  submitted without testing against us.
- Proof-of-concept code that does not actually execute against our systems, including
  payloads that fail silently and markup whose selectors do not match the elements
  they claim to target. Please run your proof of concept against the live target
  before sending it.
- Duplicate reports, and issues we are already tracking or have already fixed.
- Vulnerabilities in third-party services, dependencies, or upstream software that
  we merely use, unless you can show a working exploit against our deployment of it.
  Report those to the maintainer.

**Findings whose impact depends on a separate attack**

- Issues that only become exploitable if an attacker first runs a phishing or
  social-engineering campaign, already knows our users' email addresses or identities,
  or has already compromised an account or device. We fix phishing-resistant
  weaknesses where we can, but we assess reports on what the vulnerability itself
  achieves, not on what a determined campaign around it might achieve.
- Attacks requiring a privileged network position, a malicious browser extension, or
  physical access to an unlocked device.

**Configuration findings without a working exploit**

- Missing or misconfigured HTTP security headers (CSP, HSTS preload, X-Frame-Options,
  Referrer-Policy, Permissions-Policy, and similar), absent a demonstrated attack
  that the header would have prevented.
- SPF, DKIM, DMARC, BIMI, MTA-STS or other email-configuration observations,
  including "your DMARC is p=none" and spoofing of addresses at domains we do not
  send mail from.
- Clickjacking, tabnabbing, or missing frame protections on pages with no
  authenticated state-changing action, including marketing pages and documentation.
  For a clickjacking report to be in scope, it must identify the specific sensitive
  action on a real page of ours and demonstrate a working overlay against it.
- TLS/SSL configuration opinions: supported cipher suites, protocol versions,
  certificate chain preferences, OCSP stapling, key sizes.
- Software version disclosure, banner grabbing, and reports that a version we run is
  "known vulnerable" without a demonstrated exploit against our deployment.
- Publicly accessible files that are intended to be public: `robots.txt`,
  `.well-known/` contents, source maps, public metrics or health endpoints, open
  directory listings of public assets.
- Cookie flags (`Secure`, `HttpOnly`, `SameSite`) on cookies that carry no session or
  authorisation value.
- Absence of a security feature (CAPTCHA, 2FA, certificate pinning, subresource
  integrity, CSRF tokens on non-state-changing endpoints) without a demonstrated
  attack.
- Reports about domains, hostnames, or IP ranges we do not control, and hosts that do
  not resolve publicly.

**Application-level noise**

- Self-XSS, and anything requiring the victim to paste attacker-supplied content into
  their own console or devtools.
- Missing rate limiting or brute-force protection on unauthenticated marketing,
  documentation, or informational endpoints.
- Username, email, or account enumeration through login, signup, or password-reset
  responses.
- Content spoofing and text injection with no HTML or script execution.
- Open redirects with no demonstrated ability to steal a credential or token.
- Issues that only affect users on unsupported or end-of-life browsers.
- Session-management preferences: session lifetime, concurrent sessions, "logout does
  not invalidate every other session", lack of re-authentication on sensitive
  actions, without a demonstrated attack.
- Behaviour of our OAuth login that is a documented property of the identity provider
  rather than of our integration.

**Expected behaviour of the products**

- HyperSync and HyperRPC serve **public blockchain data**. Reading blockchain data
  that is already public on the chain is not a vulnerability. Neither is querying an
  endpoint that we intentionally serve without authentication.
- Envio Cloud **builds and runs code that customers supply**. Executing your own code
  inside your own build or your own indexer is the product working as intended. This
  is only a security issue if you can show that it crosses a boundary: reaching
  another tenant, reaching platform infrastructure, or escaping the isolation we put
  around your workload. Please show the crossing, not just the execution.
- A hosted indexer endpoint that its owner has chosen to leave unauthenticated is a
  customer configuration choice, not a flaw in the platform. Report it to the owner.
- Rate limits, quotas, and tier limits being reachable by normal use.

**Testing we do not permit**

- Denial of service, volumetric load testing, stress testing, or resource-exhaustion
  testing of any kind against our systems.
- Social engineering, phishing, or pretexting of Envio employees, contractors,
  customers, or service providers.
- Physical attacks on offices, hardware, or personnel.
- Automated scanning that degrades service for other users. Keep request rates
  reasonable and identifiable.
- Any testing against a customer's project, data, deployment, or endpoint that you do
  not own or have written permission to test.
- Accessing, modifying, deleting, or exfiltrating data that is not your own; use a
  test account of your own instead.
- Compromising credentials, whether by purchase, credential stuffing, or reuse of
  leaked data.

If you find something in an out-of-scope category that you genuinely believe is
serious in our specific case, tell us why in two or three sentences and we will look.
The list exists to save everyone's time, not to refuse real findings.

## Safe harbour

If you make a good-faith effort to follow this policy, we will treat your research as
authorised, we will not pursue or support legal action against you over it, and we
will work with you if a third party does.

Good faith means: you stay within the scope above, you use only your own accounts and
test data, you stop as soon as you have proof of a vulnerability rather than pushing
further into our systems or other people's data, you do not access, modify, retain,
or share data that is not yours, you avoid degrading service for others, and you give
us a reasonable opportunity to fix the issue before telling anyone else.

This is our commitment about how we will respond, not legal advice, and it cannot
bind third parties whose systems you might reach.

## Disclosure

Please keep the details private until we have released a fix.

We aim to resolve valid reports within **90 days** of confirming them. We are happy
for you to publish after that, and we would rather coordinate the timing and the
wording with you than be surprised. If an issue is complex and we need longer, we
will tell you why and agree a new date with you rather than let the clock run out in
silence. If a fix is straightforward, we would often rather you published sooner and
we will say so.

We will let you know when the fix is out, and we will tell you if we find the issue
being exploited, since that usually changes the timeline for both of us.

## Recognition

With your permission we credit reporters of valid issues by name or handle in the
release notes or advisory for the fix, and we are glad to confirm the details of your
report in writing if it is useful to you professionally. Tell us how you would like
to be credited, or say that you would rather stay anonymous.

## Compensation

Envio does not run a bug bounty programme, and we do not publish a reward schedule or
severity payout table. We will not enter into a negotiation about price before a
report has been assessed.

That said, we recognise that good security research is real work. Where a report
turns out to be valid, material, and new to us, we may at our sole discretion offer a
reward that reflects the seriousness of the issue and the quality of the work. That
decision is ours, it is made after we have assessed and reproduced the finding, and
it is not a commitment or an entitlement. Please report because you want the issue
fixed and credited; if we do decide a reward is warranted, we will raise it with you.

## Contact

security@envio.dev
