# rch ai

GitHub organisation for the RCH AI team — source control, CI/CD, and management of our applications.

All repositories here are **private**. Access is limited to RCH staff and approved collaborators.

---

## What lives here

This org holds the code, pipelines, and operational config for rch ai products: deployable applications built and validated in hospital environments before they are offered more broadly.

Individual repos come and go as products evolve. Each repository has its own README with setup, deployment, and environment details — start there for the app you are working on.

---

## Working in this org

1. **Access** — Ask an org admin to add you to `rch-ai` on GitHub.
2. **Clone** — You need org membership to see private repositories.
3. **CI/CD** — Pipelines and deployment workflows live in each repo (typically under `.github/workflows`). Check the repo README and any `DEPLOYMENT.md` before pushing to shared branches.
4. **Conventions** — Shared infrastructure, services, environments, and coding standards are documented in [**rch-ai-mcp**](https://github.com/rch-ai/rch-ai-mcp) (`knowledge-base.json`). If you use Cursor, register the MCP server so agents pick up RCH-specific context — see that repo's README for setup.
5. **Secrets** — Never commit credentials. Use Key Vault or environment variables; reference secret *names* in code and docs, not values.

---

## Environments & governance

- **Azure** — Most apps run on Azure (App Service, Static Web Apps, SQL, Blob Storage, AI Foundry). Region is typically Australia East unless a repo says otherwise.
- **Auth** — User-facing apps use Microsoft Entra ID (MSAL) where required. Service-to-service auth varies by app (API keys, managed identity, SQL auth — see the repo).
- **Clinical data** — Follow RCH information governance. Use synthetic data in dev unless the repo explicitly allows otherwise. Production data only in approved environments.
- **Human review** — Where AI output affects clinical, legal, or operational decisions, products include review steps before action. Do not bypass these in code or config.

---

## Contact

Questions about access, a specific repo, or deployment — contact the repo owner or your team lead.

**RCH AI** — AI, Automation & Innovation division, The Royal Children's Hospital Melbourne.
