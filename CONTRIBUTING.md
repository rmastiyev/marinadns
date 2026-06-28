# Contributing to MarinaDNS

Thanks for using [marinadns.io](https://marinadns.io). The codebase is not open source, but contributions in the form of **bug reports**, **tool suggestions**, and **data quality feedback** are genuinely useful and welcome.

---

## Bug Reports

Open an issue if:

- A tool returns an incorrect or unexpected result
- A tool hangs, times out, or shows an error
- The UI is broken on your browser or device
- A language translation is wrong or missing

**Include in your report:**
- The tool URL (e.g. `https://marinadns.io/prop`)
- The input you used (domain, IP, etc.)
- What you expected vs. what you got
- Browser and OS (for UI bugs)

---

## Tool Suggestions

Have a tool you wish existed here? Open an issue with the tag `tool request`.

Good requests include:
- What the tool does
- What input it takes and what output it produces
- Why it's useful for sysadmins/DevOps/infosec
- Any existing implementations you know of (so we can evaluate accuracy)

---

## Data Quality

MarinaDNS uses a private Unbound resolver and queries real DNS/RDAP infrastructure. If you spot stale, incorrect, or missing data:

- For **RBL/blacklist** results: include the IP and which list is wrong
- For **WHOIS/RDAP**: include the domain and what's incorrect
- For **propagation**: include the domain, record type, and which resolver gave the wrong answer

---

## Feature Feedback

Not a bug, not a tool request — just a thought? Open an issue tagged `feedback`. Things like:

- UX friction points
- Missing record types in DNS lookup
- Translation improvements (RU/TR especially welcome)
- Tool output that's technically correct but hard to read

---

## What We Won't Accept

- Pull requests (no public codebase)
- Requests to add advertising, affiliate links, or referrals
- Requests to remove working upstreams for competitive reasons

---

## Contact

Prefer not to use GitHub Issues? Reach out via the site at [marinadns.io](https://marinadns.io).
