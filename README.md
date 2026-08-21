# Segfy

### Segfy para Claude, ChatGPT e agentes de IA

Segfy, plataforma de multicálculo e gestão para corretoras de seguros. Conecte a sua conta com o e-mail e a senha do seu login do Segfy para trazer a sua corretora para o assistente.

- 📊 **1 ferramenta**
- 🔒 **Somente leitura**
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Login via magic-link (sem senha)**

[English version](README.en.md) · [Documentação completa](docs/) · [Skill pra agentes](skills/)

---

## Instalar em 1 clique

### Claude (Web e Desktop)

A Anthropic unificou a instalação de MCPs em `claude.ai/customize/connectors`. **O mesmo link serve pra Claude Web e Claude Desktop** (basta estar logado):

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

**Manual** (se o deeplink não abrir): [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → cole **Nome** `Segfy` e **URL** `https://api.mcp.ai/p_segfy`.

### Cursor

[➕ Instalar Segfy no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=segfy&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9zZWdmeSJ9)

### VS Code (Copilot Chat)

[➕ Instalar Segfy no VS Code](vscode:mcp/install?name=segfy&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_segfy%22%7D)

### ChatGPT, Manus, OpenClaw e mais 40+ clientes

Funciona em qualquer cliente MCP que suporte **MCP over HTTP**. A URL do servidor é sempre:

```
https://api.mcp.ai/p_segfy
```

Detalhes por cliente: [INSTALL.md](INSTALL.md).

---

## Exemplos de uso

```
Qual conta do Segfy está conectada?
```

---

## 1 ferramenta disponível

| Tool | Descrição |
|---|---|
| `segfy_list_accounts` | Conta Segfy conectada: e-mail e identificador do corretor. |

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)

---

## Preços

Grátis.

---

## Privacidade & LGPD

- **Somente leitura**, nenhuma ferramenta altera dados na origem.
- **Sub-processadores**: Segfy, Google Firebase (Identity Platform), o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills — tudo MIT.

**Posso usar com agente próprio (não Claude/Cursor)?**
Sim — qualquer cliente que suporte MCP over HTTP. URL: `https://api.mcp.ai/p_segfy`.


---

## Suporte

- 📧 [segfy@mcp.ai](mailto:segfy@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/segfy-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_segfy` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
