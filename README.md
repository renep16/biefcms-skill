# Skill de BiefCMS para tu IA

**BiefCMS** es el CMS headless de [BIEF Team](https://biefteam.store). Cada organización tiene su
propio servidor MCP, y esta *Agent Skill* es lo que tu IA necesita saber **antes** de llamarlo:
qué es una tipología frente a un registro, que guardar nunca publica, cómo se sube una imagen, y
qué cosas sigue haciendo una persona desde el panel.

Son dos pasos, y los dos hacen falta: la Skill le enseña a tu IA cómo funciona el CMS, y el
servidor MCP le da acceso a **tu** organización.

## 1. Instalar la Skill

```bash
npx skills add renep16/biefcms-skill
```

Funciona con Claude Code, Cursor, Gemini CLI, VS Code y Codex: si te pregunta en qué herramientas
instalarla, elige las que uses. Con `-g` se instala para todos tus proyectos; sin `-g`, solo para el
proyecto actual.

## 2. Conectar tu organización

La Skill sola no lee tu contenido.

1. En tu panel, **Desarrolladores → Claves API → Nueva clave**. Si no ves esa entrada, es una de
   dos: o tu organización no es autogestionada, y entonces la clave te la da BIEF, o tu rol no tiene
   permiso sobre *Desarrolladores*, y entonces pídesela a quien administre tu organización.
2. Elige solo los alcances que necesite tu IA. Cada uno dice en el formulario qué permite y qué
   no. Para leer basta **Leer publicado**; para que escriba contenido, **Escribir contenido**;
   para que suba y ordene imágenes, **Gestionar la biblioteca**.
3. Al crearla, junto al valor de la clave sale **Conectar una IA**: eliges tu herramienta y copias
   el bloque, que ya lleva la clave dentro. El valor se ve **una sola vez**.
4. Pégalo en tu terminal o en tu archivo de configuración, reinicia tu cliente y pídele a tu IA
   que liste las herramientas del servidor `bief-{tu-organización}`.

## Lo que tu IA no podrá hacer, a propósito

Borrar nada que no se pueda recuperar: una tipología, un medio, un formulario, un webhook. Tampoco
crear o revocar claves, regenerar secretos, cambiar ajustes, equipo o dominios, ni exportar tu
organización. Eso sigue siendo de una persona con sesión abierta. Lo que sí hace es decirte quién
puede y en qué pantalla, en vez de dejarte a medias o inventarse un atajo.

Y nunca necesita que le pegues una clave o una contraseña en el chat. Si alguna vez te la pide,
no se la des.

---

Publicado por BIEF Team. El contenido de esta Skill describe el producto BiefCMS y se actualiza
con él.
