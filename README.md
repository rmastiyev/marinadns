# MarinaDNS

**A no-friction DNS and network toolkit for sysadmins, DevOps engineers, and infosec professionals.**

🌐 **[marinadns.io](https://marinadns.io)** · 39 free tools · English, Русский, Türkçe

No captchas. No broken UI. No rate-limit walls. Just fast, reliable tools.

---

## NODA: DNS health and best-practice scoring

[**NODA Check**](https://noda.marinadns.io/) audits a domain with 30+ checks across NS, SOA, MX, SPF, DKIM, DMARC and blacklists, and reports a Health score and a Best Practice score separately. The scoring is documented in the open [NODA Methodology](https://noda.marinadns.io/methodology), and sector studies built on it are published under [NODA Research](https://noda.marinadns.io/research).

---

## Tools

### DNS
| Tool | What it does |
|---|---|
| [DNS Lookup Tool](https://marinadns.io/dig) | Query any DNS record type for any domain using our local recursive resolver. |
| [DNS Propagation](https://marinadns.io/prop) | Check DNS propagation across major global public resolvers. |
| [DNSSEC Checker](https://marinadns.io/dnssec) | Validate the DNSSEC chain of trust: DNSKEY, DS record and RRSIG verification. |
| [Reverse DNS](https://marinadns.io/ptr) | Resolve an IP address to its hostname via PTR record, with forward-confirmed check. |
| [WHOIS Lookup](https://marinadns.io/whois) | Query WHOIS registration data for any domain, IP address or ASN. |
| [DNS Blacklist Checker](https://marinadns.io/bl) | Check an IP address against 12 DNS blacklists and mail RBLs at once. |

### Email authentication
| Tool | What it does |
|---|---|
| [SPF / DKIM / DMARC Checker](https://marinadns.io/mailauth) | Check SPF, DKIM and DMARC alignment for a domain. |
| [SPF Record Generator](https://marinadns.io/spf) | Build a valid SPF TXT record for your domain interactively. |
| [DMARC Record Generator](https://marinadns.io/dmarc) | Generate a DMARC policy TXT record with every option explained. |
| [Email Header Analyzer](https://marinadns.io/emailheader) | Trace delivery hops, detect spoofing, and extract SPF/DKIM/DMARC results from raw headers. |

### Network
| Tool | What it does |
|---|---|
| [IP Lookup Tool](https://marinadns.io/ip) | Geolocation, ASN, ISP and network info for any IPv4 or IPv6 address. |
| [ASN Lookup](https://marinadns.io/asn) | Organization, announced prefixes, country and peers for an Autonomous System. |
| [Online Ping Test](https://marinadns.io/ping) | ICMP ping from our server: round-trip latency and packet loss. |
| [Online Traceroute Tool](https://marinadns.io/trace) | Hop-by-hop path from our server to your target, with latency per hop. |
| [MTR Online (My Traceroute)](https://marinadns.io/mtr) | Traceroute and ping combined: continuous per-hop loss and latency. |
| [Online Port Scanner / Checker](https://marinadns.io/port) | Test whether a TCP port is open and accepting connections. |

### HTTP, TLS & IP
| Tool | What it does |
|---|---|
| [HTTP Headers Checker](https://marinadns.io/headers) | Full HTTP request and response headers for any URL. |
| [HTTP Status Code Checker](https://marinadns.io/status) | Status code check that follows redirects and shows response time. |
| [Redirect Tracer & Checker](https://marinadns.io/redirects) | Every redirect hop with its status code. |
| [SSL Certificate Checker](https://marinadns.io/ssl) | Certificate validity, expiry, issuer, SANs and chain depth. |
| [Online TLS Scanner](https://marinadns.io/tls) | Supported TLS versions, weak ciphers and an HTTPS configuration grade. |
| [CIDR / Subnet Calculator](https://marinadns.io/cidr) | Network address, broadcast, usable IPs and subnet mask for a CIDR block. |
| [IP Range / CIDR Converter](https://marinadns.io/range) | Start/end IP pair to CIDR, or CIDR to IP range. |
| [MAC Address Lookup](https://marinadns.io/mac) | Vendor and manufacturer for a MAC address from the OUI database. |

### Security
| Tool | What it does |
|---|---|
| [Security Headers Checker](https://marinadns.io/secheaders) | Grade CSP, HSTS, X-Frame-Options and other security headers. |
| [CSP Generator / Builder](https://marinadns.io/csp) | Build a Content Security Policy header directive by directive. |
| [CT Log Search](https://marinadns.io/ct) | Search certificate transparency logs for subdomains and issued certificates. |
| [IP Reputation Checker](https://marinadns.io/reputation) | Abuse score and report history for an IP via AbuseIPDB. |
| [JWT Decoder](https://marinadns.io/jwt) | Decode a JWT header, payload and signature. No secret needed. |

### Developer utilities
| Tool | What it does |
|---|---|
| [Base64 Encoder & Decoder](https://marinadns.io/b64) | Encode text to Base64 or decode it back. |
| [URL Encoder / Decoder](https://marinadns.io/urlencode) | Percent-encode a URL or query string, or decode it. |
| [Text Encoding Detector](https://marinadns.io/encode) | Detect whether a string is Base64, URL-encoded, hex or plain text, and decode it. |
| [JSON Formatter](https://marinadns.io/json) | Pretty-print, validate and minify JSON. |
| [Regex Tester](https://marinadns.io/regex) | Test a regular expression with live match highlighting. |
| [Hash Generator](https://marinadns.io/hash) | MD5, SHA-1, SHA-256 and SHA-512, computed in your browser. |
| [Password Generator](https://marinadns.io/pwgen) | Strong random passwords with custom length and character sets. |
| [Unix Timestamp Converter](https://marinadns.io/epoch) | Unix timestamps to dates and back, in any timezone. |
| [MIME Type Checker](https://marinadns.io/mime) | MIME type by file extension, or extensions for a MIME type. |
| [robots.txt Tester](https://marinadns.io/robots) | Fetch robots.txt and test whether a URL is allowed or blocked. |

Every tool is also available in Russian (`https://marinadns.io/ru/<tool>`) and Turkish (`https://marinadns.io/tr/<tool>`). A Japanese pilot covers five email and DNS tools at [marinadns.io/ja](https://marinadns.io/ja).

---

## Learn

- [DNS Admin Course](https://marinadns.io/course/dns-admin): 11 lessons from resolution basics to DNSSEC, in English, Russian and Turkish
- [Guides](https://marinadns.io/guides): CNAME vs A vs ALIAS, DNS propagation, resolvers, SPF/DKIM/DMARC, domain spoofing, DMARC reports, NXDOMAIN/SERVFAIL/REFUSED, SSL certificate chains
- [Knowledge Base](https://marinadns.io/kb): how to read the results of every tool, grouped by topic

---

## Stack

- **Web server:** Nginx
- **Backend:** PHP 8.3-FPM
- **DNS resolver:** Private Unbound (all DNS/RBL queries go through a local resolver, with no public resolver leakage)
- **Database:** SQLite
- **CDN/proxy:** Cloudflare (Full Strict mode)
- **Hosting:** Contabo VPS, Germany

---

## Languages

- 🇬🇧 English: `marinadns.io/<tool>`
- 🇷🇺 Russian: `marinadns.io/ru/<tool>`
- 🇹🇷 Turkish: `marinadns.io/tr/<tool>`
- 🇯🇵 Japanese (pilot, 5 tools): `marinadns.io/ja/<tool>`

---

## Design Philosophy

- **No captchas**: tools should be frictionless
- **No broken results**: resolvers are tested; dead or unreliable upstreams are removed
- **Always fast**: queries go to private infrastructure, not third-party APIs where avoidable
- **Workbench, not a homepage**: all tools are visible immediately, no marketing fluff

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Changes to the NODA methodology are tracked in [CHANGELOG.md](CHANGELOG.md).

---

## License

The codebase is proprietary. Tool suggestions, bug reports, and feedback are welcome via [GitHub Issues](../../issues).
