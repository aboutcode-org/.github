
- [What should be and should NOT be reported ?](#what-should-be-and-should-not-be-reported-)
- [How to report the issue ?](#how-to-report-the-issue-)
- [What happens after you report the issue ?](#what-happens-after-you-report-the-issue-)

This document contains information on how to report security vulnerabilities in AboutCode repositories
and how security issues reported to the AboutCode organisation are handled. 

If you have any concern around Security of any AboutCode projects or believe
you have uncovered a vulnerability, we suggest that you get in touch via the
e-mail address [security@aboutcode.org](mailto:security@aboutcode.org).

Before sending the report, however, please read the following guidelines first.
The guidelines should answer the most common questions you might have about
reporting vulnerabilities.

### What should be and should NOT be reported ?

There are two ways to report vulnerbilities to AboutCode projects.

- Private Vulneribility Disclosure through GitHub
- By email to AboutCode security maintainers

**⚠️ Please do not file GitHub issues for security vulnerabilities as they are public! ⚠️**

Here is a list of repositories which have Private Vulneribility Disclosure
turned on:

- https://github.com/aboutcode-org/scancode.io
- https://github.com/aboutcode-org/scancode-toolkit

For these repositories, you can report a security vulneribility through GitHub.
Please refer to the [documentation](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability)
on reporting vulneribilities privately through GitHub.

For example, if you want to report a security issue at scancode.io, report this at
https://github.com/aboutcode-org/scancode.io/security/ using the `Report a Vulneribility`
button available at the top-right corner.

Alternatively, for other aboutcode-org projects which do not have private vulneribility reporting
turned on, you might use the e-mail address [security@aboutcode.org](mailto:security@aboutcode.org)
to communicate to us about any security vulnerbilities.

**Only** use the security e-mail address or the GitHub private disclosure feature
to report undisclosed security vulnerabilities and to manage the process of fixing
such vulnerabilities. We do not accept regular bug reports or other security-related
queries at this address. We will ignore mail sent to this address that does not
relate to an undisclosed security problem in any AboutCode project repository.
Please use our public communication platforms, our [Matrix chatroom](https://matrix.to/#/#aboutcode-org_discuss:gitter.im)
or [AboutCode Discussions](https://github.com/orgs/aboutcode-org/discussions)
for inquiries, questions and other discussions related to the process or other issues.

You might also submit security issues if they are present in docker images released by
us (for example: `ghcr.io/aboutcode-org/scancode.io`) or released as libraries/wheels at pypi
(like https://pypi.org/project/scancode-toolkit/) only if they are applicable in this specific
context or exploitable.

### How to report the issue ?

Please send one plain-text description for each vulnerability you are reporting including an explanation
of how it the security of the specific AboutCode project. It should have these details:

- A summary of the security issue
- Which part of the code (modules/functions) are vulnerable
- Vulnerable endpoint/API/API function
- Impact of the vulneibility on the application

Other additional information which could be useful to us, which would be crucial for the
reporting later and adding a fix are listed below. This can also be collaborated on
with the specific maintainers, after you submit the initial report and recieve an acknowledgement.

- A private POC of vulnerebility exploitation
- Vulnerable version range where this is applicable
- Which commit the vulneribility was introduced in
- Specific configurations where the vulnerbility is applicable

### What happens after you report the issue ?

Someone from the AboutCode team of maintainers will get back to you after assessing the report.
This will either be a reply to the email from security@aboutcode.org or a comment and acceptance on
the draft advisory at the private GitHub Advisory disclosure. You will usually get confirmation that
the issue is being worked (or that we quickly assessed it as invalid) within several business days.
Note that this is an Open-Source projects and members of the security team
are also volunteers, so please make sure to be patient. If you do not get a response within a week,
please send a kind reminder to the security team about a lack of response.
You will also be credited as a reportor for the advisory and have to accept the same.

You can also optionally, start a temporary private fork if you want to start to fix the issue.
See the [GitHub docs]https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability on how to do this
from the same draft advisory report context so that the maintainers can also have access.
Note that only the repository maintainer can merge changes from that private fork into the parent repository.
Alternatively, the maintainers will work on the fix and keep you updated once it lands on the default branch.

One or multiple maintainers will be assigned to collaborate/work on a fix, draft all the details for the
reporting and to release and announce the fix.

We typically work with the GitHub advisory workflow and apply for a CVE number within there, and
you will be notified when a `CVE` number (and a GitHub advisory with a `GHSA` ID) is assigned to
the advisory.

We will usually also let you know the release the issue is scheduled to be fixed
after we assess the issue (which might take longer or shorter time depending on the issue complexity and
potential impact, severity, whether we want to address a whole class issues in a single fix and a number
of other factors). You should subscribe to and monitor the [Matrix chatroom](https://matrix.to/#/#aboutcode-org_discuss:gitter.im)
to see the announcement of the security issue - including the CVE number
and the severity of the issue once the issue is fixed and release is public.
