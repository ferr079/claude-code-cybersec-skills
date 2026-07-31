# Claude Code Cybersecurity Skills

31 cybersecurity slash commands for [Claude Code](https://claude.com/product/claude-code) — covering offensive security (CTF/pentest) and defensive operations (blue team/hardening).

Based on [Anthropic-Cybersecurity-Skills](https://github.com/mukul975/Anthropic-Cybersecurity-Skills) by mukul975, reformatted as Claude Code slash commands with MITRE ATT&CK references.

## Installation

Copy the `commands/cybersec/` directory to your Claude Code commands folder:

```bash
cp -r commands/cybersec/ ~/.claude/commands/cybersec/
```

The skills will be available globally as `/cybersec:<name>` in any Claude Code session.

## Tier 1 — Offensive / CTF / Pentest (17 skills)

| Command | Description |
|---|---|
| `/cybersec:nmap-advanced` | Network scanning with advanced Nmap techniques |
| `/cybersec:privesc-linux` | Linux privilege escalation |
| `/cybersec:sqli-sqlmap` | SQL injection exploitation with sqlmap |
| `/cybersec:xss-testing` | XSS vulnerability testing |
| `/cybersec:ssrf` | Server-Side Request Forgery exploitation |
| `/cybersec:deserialization` | Insecure deserialization exploitation |
| `/cybersec:ssti` | Server-Side Template Injection |
| `/cybersec:web-pentest` | Full web application penetration test |
| `/cybersec:hashcat` | Hash cracking with Hashcat |
| `/cybersec:dns-enum` | DNS enumeration and zone transfer |
| `/cybersec:subdomain-enum` | Subdomain enumeration with Subfinder |
| `/cybersec:jwt-attack` | JWT algorithm confusion attack |
| `/cybersec:bloodhound` | Active Directory BloodHound analysis |
| `/cybersec:kerberoasting` | Kerberoasting with Impacket |
| `/cybersec:internal-pentest` | Internal network penetration test |
| `/cybersec:binary-exploit` | Binary exploitation analysis |
| `/cybersec:race-condition` | Race condition exploitation |

## Tier 2 — Blue Team / Defensive (14 skills)

| Command | Description |
|---|---|
| `/cybersec:cis-linux-hardening` | CIS Benchmark Linux hardening |
| `/cybersec:docker-hardening` | Docker container hardening |
| `/cybersec:wazuh-detection` | Endpoint detection with Wazuh |
| `/cybersec:linux-audit-logs` | Linux audit log analysis |
| `/cybersec:dns-exfil-analysis` | DNS exfiltration log analysis |
| `/cybersec:dns-exfil-detect` | DNS exfiltration detection |
| `/cybersec:suricata-config` | Suricata IDS configuration |
| `/cybersec:aide-fim` | File integrity monitoring with AIDE |
| `/cybersec:wireshark-analysis` | Network traffic analysis with Wireshark |
| `/cybersec:lateral-movement-detect` | Lateral movement detection |
| `/cybersec:syslog-central` | Syslog centralization with Rsyslog |
| `/cybersec:security-headers` | HTTP security headers audit |
| `/cybersec:credential-dump-detect` | Credential dumping detection |
| `/cybersec:docker-forensics` | Docker container forensics |

## Usage

Each skill provides a structured runbook that Claude Code follows interactively:

```
> /cybersec:nmap-advanced

Target: 10.10.10.x
Starting reconnaissance...
```

The skills guide Claude through the complete workflow — from reconnaissance to exploitation or from detection to remediation — with concrete commands and MITRE ATT&CK references.

## License

MIT

## Credits

Original skills by [mukul975/Anthropic-Cybersecurity-Skills](https://github.com/mukul975/Anthropic-Cybersecurity-Skills) (~27k stars). Reformatted for Claude Code slash command format.
