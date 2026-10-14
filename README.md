# Tiago Costa · TN Costa Tecnologia

**Engenheiro de Software e DevOps** · back-end Python · PostgreSQL · Linux e Docker · Macapá (AP), trabalho remoto

Quatorze anos em sistemas corporativos e PostgreSQL. Desde 2025 respondo de ponta a ponta (arquitetura, código,
banco de dados, CI/CD, infraestrutura Linux, segurança e resposta a incidentes) por sistemas em produção de um grupo
educacional de ensino superior e saúde e por produtos próprios: o [Escolia](https://escolia.com.br), SaaS
multi-tenant de gestão escolar; agentes de IA em n8n; e uma [loja de automações n8n](https://www.tncostatecnologia.com.br/automacoes/)
com pagamentos integrados. Comecei no no-code (Bubble, Make, n8n) e levei para código próprio o que precisou crescer.

Disponível para oportunidades remotas (CLT ou PJ) em back-end Python, DevOps e bancos de dados.

## Projetos públicos

| Repositório | O que é | O que mostra |
|---|---|---|
| [nfse-nacional-kit](https://github.com/tncostatec/nfse-nacional-kit) | Emissão, consulta e cancelamento de NFS-e no padrão Nacional (SEFIN/gov.br) em Python: XML da DPS, assinatura XMLDSig com certificado A1, cliente mTLS. Extraído de um ERP que emite notas reais. MIT. | Integração com órgão público medida contra o validador real; as decisões "que parecem erradas" documentadas com a data da medição (`docs/ARMADILHAS.md`); CI com autoteste sem certificado. |
| [n8n-automacoes-whatsapp](https://github.com/tncostatec/n8n-automacoes-whatsapp) | Vitrine da linha de templates n8n para WhatsApp (Evolution API / Cloud API) para clínicas e serviços: núcleo compartilhado, Data Tables, sandbox com serviços simulados. | Desenho de produto em n8n com modo teste de fábrica, opt-out, janela de envio e entrega carimbada por comprador; a própria loja roda em n8n. |

Os sistemas de clientes e o código dos produtos são privados. O que está aqui é o que pode ser público sem expor
negócio nem dado de terceiros.

## Como trabalho

- **Critério de aceite antes, testes durante, verificação em produção depois.** Portão de CI com ruff, pytest com
  cobertura, testes contra a API rodando (RBAC, antifraude, corrida de saque duplo), build e Trivy antes de qualquer deploy.
- **Backups que restauram.** `pg_dump` consistente com restauração de verificação, restore por tenant e cópia off-site
  (Backblaze B2). Backup sem teste de restore não conta.
- **Observabilidade sem dado pessoal.** Sentry por tenant e request id, Uptime Kuma, registro das rotinas cron,
  vigia de CPU, steal e OOM com alerta por e-mail.
- **Incidentes viram postmortem.** Contenção, causa raiz, correção provada e lições escritas; dois deles (um
  vazamento de processos que derrubou uma VPS e um minerador via RCE em Next.js) estão descritos no meu currículo e
  serão publicados aqui, anonimizados.
- **Segurança como padrão de infra.** Contêineres com rootfs somente leitura, tmpfs `noexec`, `cap_drop: ALL`,
  `no-new-privileges`, teto de CPU e PIDs; UFW, fail2ban, SSH só por chave; segredos cifrados em repouso; MFA TOTP.
- **Uso IA com disciplina de engenharia.** Claude Code com subagentes em git worktrees e servidores MCP, sempre com
  critério de sucesso definido antes e verificação depois.

## Stack em produção

- **Back-end:** Python 3.11+, FastAPI, Pydantic, SQLAlchemy 2 (async), asyncpg, Alembic, Celery e Redis, APScheduler, httpx; REST com OpenAPI, webhooks, JWT, OAuth2, mTLS com certificado A1.
- **Dados:** PostgreSQL (9.3 a 16: multi-tenant por schema, índices parciais, tuning, migração e unificação de bases), SQL Server (T-SQL, pyodbc), MySQL, Redis, MinIO; ETL com Pentaho Kettle; JasperReports.
- **Infra e DevOps:** Ubuntu, Docker e Docker Compose, Nginx, Traefik, Easypanel, Cloudflare (DNS, Pages, Turnstile), Let's Encrypt, GitHub Actions, cron e systemd; Sentry, Uptime Kuma, Trivy, Dependabot, Semgrep.
- **Integrações:** Asaas, Santander Cobrança, InfinitePay, NFS-e Nacional, SERPRO, DropSigner, Evolution API e WhatsApp Cloud API, Google Calendar, Brevo, Backblaze B2, Hostinger API, Anthropic e Groq.
- **Front-end e testes:** Next.js, React, Tailwind CSS, TanStack Query; pytest, Vitest, Playwright.
- **Automação:** n8n self-hosted (workflows, agentes de IA, Code nodes), Make, Bubble.

## Onde me encontrar

[LinkedIn](https://www.linkedin.com/in/tiago-costa-7470587a) · [tncostatecnologia.com.br](https://www.tncostatecnologia.com.br/) · [Página da TN Costa no LinkedIn](https://www.linkedin.com/company/tn-costa-tecnologia/) · [Contato](https://www.tncostatecnologia.com.br/contato/)
