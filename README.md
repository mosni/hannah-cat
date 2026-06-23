# hannah.cat

Static personal site — animated spinning cat with follow-the-cursor eyes.

- kind: `static` (served by host nginx; see nginx.conf). Repo is **public**.
- favicon hotlinked from `mosni.dev/images/icon.png` (same owner — fine).
- Cat image hotlinked from `i.imgur.com` — external dependency; could be inlined if needed.

## Notable

- Hardcoded `https://mosni.dev` link and favicon reference — intentional cross-domain links, not a problem.
- No build step; deploy as-is.

## Local test

    docker run --rm -d -p 8089:80 -v "$PWD:/usr/share/nginx/html:ro" --name hannah-test nginx:alpine
    curl -s localhost:8089 | head            # then: docker rm -f hannah-test
