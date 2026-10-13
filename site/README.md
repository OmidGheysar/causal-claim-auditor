# Front end

Put `causal-auditor.html` here, renamed to `index.html`.

Caddy serves this folder at the site root. The page calls the n8n webhook at `/webhook/...` on the same domain, so no API keys or server addresses need to be in the HTML.
