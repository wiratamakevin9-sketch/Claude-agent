# Claude Agents

Kumpulan subagent Claude Code dengan peran tim software lengkap.

| Agent | Peran |
|---|---|
| `pm` | Product Manager: PRD, user story, acceptance criteria, prioritas |
| `architect` | Software Architect: desain sistem, kontrak API, ADR |
| `designer` | UI/UX Designer: user flow, wireframe, design token, aksesibilitas |
| `mobile` | Mobile Engineer: Flutter / React Native / native |
| `backend` | Backend Engineer: API, business logic, auth |
| `database` | Database Engineer: skema, ERD, migrasi, optimasi query |
| `qa` | QA Engineer: test plan, test otomatis, laporan bug |
| `security` | Security Engineer: threat modeling, review OWASP, audit dependensi |
| `devops` | DevOps Engineer: Docker, CI/CD, IaC, monitoring |
| `tech-lead` | Tech Lead: pembagian tugas, code review, Definition of Done |

## Cara pasang

Untuk satu proyek, salin folder `.claude/agents/` ke root proyek:

```bash
cp -r .claude/agents /path/ke/proyek/.claude/
```

Untuk semua proyek di komputermu, salin ke folder user:

```bash
mkdir -p ~/.claude/agents && cp .claude/agents/*.md ~/.claude/agents/
```

Mulai sesi Claude Code baru agar agent terbaca.

## Cara pakai

```
@agent-pm buatkan PRD untuk aplikasi kasir
@agent-security review folder src/auth
```

Alur yang disarankan: `pm` → `architect` → `designer` + `database` → `backend` + `mobile` → `qa` + `security` → `devops` → `tech-lead`.

Subagent tidak bisa memanggil subagent lain; `tech-lead` menyusun rencana langkah demi langkah dan sesi utama yang memanggil tiap agent.
