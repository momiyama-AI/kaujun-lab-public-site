# NitakuBar question data

`catalog.json` contains the reviewed, production-signed NitakuBar question-data envelope. It contains question data only and is not application code.

Planned production URL:

`https://momiyama-ai.github.io/kaujun-lab-public-site/nitakubar/catalog.json`

Current artifact: revision **1**, **397 questions**, **72,101 bytes**.

- Catalog canonical SHA-256: `f122c1d0afd71b22cd002cfec3037bce65b67f03633377f58ec2512554150b01`
- Envelope SHA-256: `c027cf410b90c7f6df8743fdf8a4b4332b5f81acca1b60bae4a182a4d65c92da`
- Signing public-key fingerprint: `008269309e51245e85d314b3e786bdf52811f07385c3eeaf0dc318d84bda9aea`

Before publishing a replacement, verify its signature with the dedicated public key, require increasing revision, and preserve all previous question IDs, text and tags. Record its revision, count, byte length and digest. Keep prior signed artifacts outside the active public file path. Never place private keys, device histories, favorites or test-signed artifacts here.

Only this dedicated directory is added to the existing site. Its homepage, design, other pages, workflow, domain and access settings are unchanged. The existing `.nojekyll` file is retained, so the JSON is a static asset rather than a rendered page. Native-app behavior and the actual HTTPS JSON response must still be verified separately.

After publication, request the exact URL without redirects or authentication, require HTTP 200 and JSON MIME type, and verify the downloaded signature, revision, question count and digest.

Replacing this file with a lower revision or deleting it does not withdraw valid data already cached on devices. Site-source rollback and the app's last-good-cache fallback are separate mechanisms. The current app supports additional questions; server-directed removal or editing of already published questions is not supported.
