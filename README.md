# MarinaDNS

**A no-friction DNS and network toolkit for sysadmins, DevOps engineers, and infosec professionals.**

🌐 **[marinadns.io](https://marinadns.io)**

No captchas. No broken UI. No rate-limit walls. Just fast, reliable tools.

---

## Tools

### DNS
| Tool | Description |
|---|---|
| DNS Lookup | Query any record type (A, AAAA, MX, TXT, NS, SOA, CAA, SRV, PTR, NAPTR, TLSA, DS, DNSKEY, SERIAL…) |
| DNS Propagation | Check propagation across global resolvers with consistency detection |
| Reverse DNS | PTR lookup for any IP address |
| WHOIS / RDAP | Domain and IP WHOIS via RDAP (IANA bootstrap) with whois fallback |
| DNS over HTTPS | Query via DoH resolvers |

### Network
| Tool | Description |
|---|---|
| IP Geolocation | Location, ASN, and org data for any IP |
| ASN Lookup | Autonomous System details and prefix info |
| Ping | ICMP reachability from the server |
| Traceroute | Hop-by-hop path to any host |
| Port Check | TCP port open/closed test |
| BGP Prefix Lookup | Routing table info for any prefix |

### Security
| Tool | Description |
|---|---|
| Blacklist Check | RBL/DNSBL check across major blocklists via private Unbound resolver |
| TLS/SSL Grader | Certificate chain, cipher suite, and protocol grading |
| HTTP Headers | Security header analysis |
| DMARC Lookup | Parse and explain DMARC policy |
| SPF Lookup | Parse and flatten SPF records |
| DKIM Lookup | Retrieve and validate DKIM public keys |
| BIMI Lookup | Brand Indicators for Message Identification record check |

### Generators
| Tool | Description |
|---|---|
| DMARC Generator | Build a valid DMARC policy record |
| SPF Generator | Build an SPF record with flattening |
| DKIM Generator | Generate DKIM key pairs |
| Password Generator | Secure random password generator |
| UUID Generator | RFC 4122 UUID v4 generator |
| Hash Generator | MD5, SHA-1, SHA-256, SHA-512 |
| CSR Generator | Certificate Signing Request builder |

### Testers
| Tool | Description |
|---|---|
| Email Header Analyzer | Parse raw email headers |
| HTTP Request Tester | Inspect HTTP response headers and body |
| SMTP Tester | Test SMTP connectivity and response |
| WebSocket Tester | Test WebSocket endpoint connectivity |
| CORS Tester | Check CORS headers on any endpoint |
| SSL Certificate Decoder | Decode and inspect PEM certificates |

### Converters
| Tool | Description |
|---|---|
| IP to Decimal | Convert between IP formats |
| CIDR Calculator | Subnet and broadcast address calculator |
| Base64 Encode/Decode | Standard and URL-safe Base64 |
| Unix Timestamp | Convert epoch to human-readable and back |
| JSON Formatter | Format, validate, and minify JSON |
| Markdown Preview | Live Markdown renderer |

---

## Stack

- **Web server:** Nginx
- **Backend:** PHP 8.3-FPM
- **DNS resolver:** Private Unbound (all DNS/RBL queries go through a local resolver — no public resolver leakage)
- **Database:** SQLite (query logging)
- **CDN/proxy:** Cloudflare (Full Strict mode)
- **Hosting:** Contabo VPS, Germany

---

## Languages

The interface is available in:
- 🇬🇧 English
- 🇷🇺 Russian
- 🇹🇷 Turkish

Language is detected via `Accept-Language` header with a cookie-based override.

---

## Design Philosophy

- **No captchas** — tools should be frictionless
- **No broken results** — resolvers are tested; dead/unreliable upstreams are removed
- **Always fast** — queries go to private infrastructure, not third-party APIs where avoidable
- **Workbench, not a homepage** — all tools are visible immediately, no marketing fluff

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## License

The codebase is proprietary. Tool suggestions, bug reports, and feedback are welcome via [GitHub Issues](../../issues).
