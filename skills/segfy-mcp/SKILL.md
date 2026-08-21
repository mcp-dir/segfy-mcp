---
name: segfy-mcp
description: Skill da REST API do Segfy na MCP.AI: 1 endpoint em /api/segfy. Segfy, plataforma de multicálculo e gestão para corretoras de seguros. Conecte a sua conta com o e-mail e a senha do seu login do Segfy para trazer a sua corretora para o assistente. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Segfy — REST API skill

Você tem acesso à **Segfy** REST API na MCP.AI.

> Segfy, plataforma de multicálculo e gestão para corretoras de seguros. Conecte a sua conta com o e-mail e a senha do seu login do Segfy para trazer a sua corretora para o assistente.

## Base URL

```
https://api.mcp.ai/api/segfy
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/segfy/list/accounts \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/segfy/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `segfy_list_accounts`

Conta Segfy conectada: e-mail e identificador do corretor. _(POST /api/segfy/list/accounts)_

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_segfy` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
