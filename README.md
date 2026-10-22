# cirite-invernomics

Página de CIRITE / CIRBE que se abre dentro de las negociaciones de Bitrix24 (Cloudflare Pages).

## Seguridad

- La página **no lleva ninguna clave**. Cada llamada al servidor (`itw-invernomics`) envía el token de la sesión de Bitrix24 que da `BX24.getAuth()` (`Authorization: Bearer …` y `X-B24-Domain`), y el servidor lo valida contra Bitrix24.
- Por eso el envío al Banco de España y la descarga de CIRBE **solo funcionan dentro de Bitrix24**. En modo "standalone" (fuera de Bitrix) la página avisa y no llama al servidor.
- La clave que llevaba antes la página sigue en el historial público de este repo: debe considerarse comprometida y rotarse (`API_KEY` en Railway).
