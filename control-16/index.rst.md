# CIS Control 16: Application Software Security

Manage the security life cycle of in-house developed, hosted, or
acquired software to prevent, detect, and remediate security weaknesses
before they can impact the enterprise.

**Why is this CIS Control Critical?**

Applications provide a human-friendly interface to allow users to access
and manage data in a way that is aligned with business functions. They
also minimize the need for users to deal directly with complex (and
potentially error-prone) system functions, like logging into a database
to insert or modify files. Enterprises use applications to manage their
most sensitive data and control access to system resources. Therefore,
an attacker can use the application itself to compromise the data
instead of an elaborate network and system hacking sequence that
attempts to bypass network security controls and sensors. This is why
protecting user credentials (specifically application credentials)
defined in CIS Control 6 is so important. Lacking credentials
and application flaws are the attack vectors of choice. However, today's
applications are developed, operated, and maintained in a highly
complex, diverse, and dynamic environment. Applications run on multiple
platforms: web, mobile, cloud, etc., with application architectures that
are more complex than legacy client-server or database-web server
structures. Development life cycles have become shorter, transitioning
from months or years in long waterfall methodologies to DevOps cycles
with frequent code updates. Also, applications are rarely created from
scratch and are often "assembled" from a complex mix of development
frameworks, libraries, existing code, and new code. There are also
modern and evolving data protection regulations dealing with user
privacy. These may require compliance with regional or sector-specific
data protection requirements. These factors make traditional approaches
to security, like control (of processes, code sources, run-time
environment, etc.), inspection, and testing are much more challenging.
Also, the risk that an application vulnerability introduces might not be
understood except in a specific operational setting or context.
Application vulnerabilities can be present for many reasons: insecure
design, insecure infrastructure, coding mistakes, weak authentication,
and failure to test for unusual or unexpected conditions. Attackers can
exploit specific vulnerabilities, including buffer overflows, exposure
to Structured Query Language (SQL) injection, cross-site scripting,
cross-site request forgery, and click-jacking of code to gain access to
sensitive data or take control over vulnerable assets within the
infrastructure as a launching point for further attacks. Applications
and websites can also be used to harvest credentials data or attempt
to install malware onto the users who access them. Finally, it is now
more common to acquire Software as a Service (SaaS) platforms, where
software is developed and managed entirely through a third party. These
might be hosted anywhere in the world. This brings challenges to
enterprises that need to know what risks they are accepting with using
these platforms, and they often do not have visibility into the
development and application security practices of these platforms. Some
of these SaaS platforms allow for customizing of their interfaces and
databases. Enterprises that extend these applications should follow this
CIS Control, similar to if they were doing ground-up customer
development.
