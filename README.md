# Faculty Development Connect — public demonstration

A working demonstration of the system the **Duke University Center for Teaching
and Learning** uses to track faculty development work — consultations, programs,
and events — running entirely on invented people.

**Live site:** https://sensemaking-the-loop.github.io/fdconnect-demo/

---

## Everything here is fictional

Every person, engagement, program, date, and number in this demonstration was
generated for it. No real faculty record appears anywhere on this site. The
intake form accepts input and saves nothing.

What *is* real is the taxonomy — engagement types, topic areas, program names,
rank categories, and school and unit names — and the workflow those categories
sit inside. That distinction is the point of the demonstration: the data is
invented, but the structure is one a working team settled on and revised in use.

See [about.html](about.html) for a fuller account.

## This repository is build output, not source

The files here are **derived** from a private canonical repository by a
derivation script. They are not edited directly, and edits made here would be
overwritten by the next build.

Derivation resets every configuration value to a placeholder, replaces the
internal application links with local ones, and injects the demonstration
banner. A build is published only after every assertion in the derivation gate
passes, which includes screening all synthetic names against the real contact
roster so that no invented person can coincide with an actual one.

`provenance.json` records the source revision each build came from, the date it
was generated, and a SHA-256 for every published file. It is written by a tool
that refuses to stamp a build derived from uncommitted sources, or one whose
gate run did not pass.

Because derivation reduces every real value to a fixed placeholder, a build made
from redacted sources is byte-identical to one made from configured sources. The
published file hashes in `provenance.json` are therefore verifiable by anyone,
without access to any private configuration.

## The four surfaces

| File | What it is |
| --- | --- |
| `index.html` | Front page — the three doors into the system |
| `quicklog.html` | The intake form a consultant uses to log an engagement |
| `dashboard.html` | Activity by month, type, topic, school, and fiscal year |
| `DossierDirectory.html` | Searchable, filterable index of every contact |
| `DossierFullView.html` | One page per person — engagement history and notes |
| `about.html` | What this demonstration is and is not |

In the live system the directory and dossier pages are served by a Google Apps
Script web application and read from a single spreadsheet acting as the system
of record. Here they run as static files against synthetic data embedded in the
page, which is what makes the demonstration possible without a backend.

## Questions

Built and maintained by the CTL faculty development team at Duke University.
