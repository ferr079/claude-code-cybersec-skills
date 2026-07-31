# Claude Code Cybersecurity Skills

31 cybersecurity runbooks packaged as a [Claude Code](https://claude.com/product/claude-code) plugin — 17 offensive (CTF, pentest) and 14 defensive (blue team, hardening), each with MITRE ATT&CK references.

Every skill is a structured runbook Claude follows interactively: concrete commands, expected output, and what to do with it. Nothing runs on its own — you stay in the loop at each step.

Based on [Anthropic-Cybersecurity-Skills](https://github.com/mukul975/Anthropic-Cybersecurity-Skills) by mukul975 (~27k stars), reformatted for Claude Code.

## Install

```
/plugin marketplace add ferr079/claude-code-cybersec-skills
/plugin install cybersec@ferr079-cybersec
/reload-plugins
```

Then invoke a runbook by name:

```
/cybersec:nmap-advanced
/cybersec:wazuh-detection
```

Claude also pulls a skill on its own when the task calls for it — each one carries a `description` stating when it applies.

<details>
<summary>Other ways to install</summary>

**Try it without installing** — load the plugin for a single session:

```bash
git clone https://github.com/ferr079/claude-code-cybersec-skills
claude --plugin-dir ./claude-code-cybersec-skills
```

**Pick individual skills** — each `skills/<name>/SKILL.md` is self-contained; copy the folders you want into `~/.claude/skills/`. They then answer to `/<name>` instead of `/cybersec:<name>`.

</details>

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

> Offensive skills are written for **authorized engagements and CTF targets**. Each one states its authorization prerequisite, and several open with an explicit "do not use" section. Read it.

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

```
> /cybersec:nmap-advanced

Target: 10.10.10.x
Starting reconnaissance...
```

Each skill walks the complete workflow — reconnaissance to exploitation, or detection to remediation — with concrete commands and MITRE ATT&CK mappings.

## Repository layout

```
.claude-plugin/
  plugin.json        plugin manifest (namespace: cybersec)
  marketplace.json   catalog, so the repo installs directly
skills/
  <name>/SKILL.md    one runbook per skill: frontmatter + body
```

These runbooks previously shipped as flat `commands/cybersec/*.md` files. Slash commands and skills are now the same mechanism in Claude Code, and the skill layout adds what flat files could not carry: a `description` that lets Claude pull the right runbook on its own, and a folder per skill for supporting files. Invocation names are unchanged.

## Credits

Original skills by [mukul975/Anthropic-Cybersecurity-Skills](https://github.com/mukul975/Anthropic-Cybersecurity-Skills). Repackaged as a Claude Code plugin, with MITRE ATT&CK references.

## License

MIT
