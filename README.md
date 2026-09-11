# Skill de BiefCMS para tu IA

**BiefCMS** es el CMS headless de [BIEF Team](https://biefteam.store). Cada organización tiene su
propio servidor MCP, y esta *Agent Skill* es lo que tu IA necesita saber **antes** de llamarlo:
qué es una tipología frente a un registro, que escribir nunca publica, cómo se conecta, y qué
cosas sigue haciendo una persona desde el panel.

## Instalar

```bash
npx skills add renep16/biefcms-skill
```

Funciona con Claude Code, Cursor, Gemini CLI, VS Code y Codex. Con `-g` se instala para todos tus
proyectos; sin `-g`, solo para el proyecto actual.

## Conectar tu organización

La Skill sola no lee tu contenido: hace falta conectar el servidor MCP de tu organización.

1. En tu panel, **Desarrolladores → Claves API → Nueva clave**. Si no ves esa entrada, tu
   organización no es autogestionada y la clave te la da BIEF.
2. Elige el alcance mínimo que necesites. `read:publicado` para leer, `write:contenido` para que
   tu IA escriba contenido, `write:estructura` para que además defina tipologías.
3. Junto al valor de la clave sale **Conectar una IA** con la línea ya montada y un botón de
   copiar. El valor se ve **una sola vez**.
4. Pega esa línea en tu terminal o en tu archivo de configuración, y reinicia tu cliente.

## Lo que tu IA no podrá hacer, a propósito

Borrar una tipología, crear o revocar claves, tocar webhooks, sincronizaciones, ajustes, equipo o
dominios, ni exportar tu organización. Eso sigue siendo de una persona con sesión abierta. Lo que
sí hace es decirte quién puede y en qué pantalla, en vez de dejarte a medias o inventarse un atajo.

Y nunca necesita que le pegues una clave o una contraseña en el chat. Si alguna vez te la pide,
no se la des.

---

Publicado por BIEF Team. El contenido de esta Skill describe el producto BiefCMS y se actualiza
con él.
