# crdb-dialect

<!-- phasetwo:banner:start - managed by p2-inc/shared-github-actions, edit there -->
[![docs](https://img.shields.io/badge/docs-phasetwo.io-blue)](https://phasetwo.io/docs/introduction/)

📚 [Documentation](https://phasetwo.io/docs/introduction/) • 🚀 [Hosted Keycloak](https://dash.phasetwo.io/?utm_source=github&utm_medium=readme&utm_campaign=crdb-dialect) • 🤖 [Keycloak Skills](https://github.com/p2-inc/keycloak-skills) • 💬 [Support](mailto:support@phasetwo.io)

> [!TIP]
> **Run this in our cloud, no setup needed.** Phase Two hosts Keycloak with all of our extensions built in. [Try it free with your own cluster →](https://dash.phasetwo.io/?utm_source=github&utm_medium=readme&utm_campaign=crdb-dialect)
>
> **Using a coding agent?** Add the Phase Two Keycloak skills ([launch post](https://phasetwo.io/blog/keycloak-skills-mcp-launch)) to Claude Code, Cursor or Codex so your agent can set up passwordless login, SSO, organizations and clusters for you:
>
> ```sh
> # Install the skills (connects to our hosted MCP server)
> claude plugin marketplace add p2-inc/keycloak-skills
> claude plugin install phasetwo@keycloak-skills
> # Or connect to the MCP server directly
> claude mcp add --transport http keycloak https://mcp.phasetwo.io/mcp
> ```
<!-- phasetwo:banner:end -->

A Hibernate (6) dialect for CRDB that removes **all** `escape '...'` clauses in SQL LIKE/ESCAPE

## notes

- https://www.cockroachlabs.com/docs/stable/known-limitations#using-like-escape-in-where-and-having-constraints
- https://github.com/steveperkins/hibernate6-h2-like-fix
- https://docs.jboss.org/hibernate/orm/6.2/javadocs/org/hibernate/dialect/CockroachSqlAstTranslator.html
- https://github.com/hibernate/hibernate-orm/blob/6.2/hibernate-core/src/main/java/org/hibernate/dialect/CockroachSqlAstTranslator.java#L131
- https://discourse.hibernate.org/t/why-does-hibernate-6-automatically-escape-backslashes-when-rendering-like-predicates/7420
- https://discourse.hibernate.org/t/erroneous-escape-being-added-to-generated-sql-with-a-jparepository-findall-example/9353
- https://discourse.hibernate.org/t/it-is-necessary-to-write-redundant-escape-after-every-like-expression/9079/5
- https://discourse.hibernate.org/t/incorrect-escape-added-to-sql-for-h2-in-oracle-mode/8372/10



