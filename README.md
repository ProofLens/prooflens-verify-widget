\# ProofLens Verify Widget (Caption-mode, No Overlay)



\*\*Add a tiny verified credit-line — click to see creator \& verify file integrity. No on-image badges.\*\*



\[Demo](https://prooflens.netlify.app/demo-embed.html) · \[Verify tool](https://prooflens.netlify.app/verify.html) · \[Main repo](https://github.com/ProofLens/prooflens)



!\[ci](https://github.com/ProofLens/prooflens-verify-widget/actions/workflows/ci.yml/badge.svg)



\## Quickstart (self-host)

```html

<script src="/dist/prooflens-verify.min.js"></script>

<figure>

&nbsp; <img src="/images/photo.jpg" data-manifest-url="/images/photo.jpg.manifest.json" alt="">

&nbsp; <figcaption class="credit">Photo: Your Name</figcaption>

</figure>

Or use the hosted lite build (no overlay):

<script src="https://prooflens.netlify.app/assets/prooflens-verify-lite.js"></script>


How it works

We compute SHA-256 of the exact image in the browser (WebCrypto).

Compare to *.manifest.json (contains sha256, creator, created_at).

Match ⇒ appends a small ✓ verified to the caption/credit. No overlay.

Events / API

Global: window.addEventListener('ProofLensVerified', (e) => { /* e.detail = {img, pass} */ })

Manual attach: window.ProofLensLite.attach(imgElement)

Files

dist/prooflens-verify.min.js — production bundle

docs/api.md — API & events

Roadmap

WordPress Auto-CR plugin integration (header once, auto-inject)

Header-only mode via Link: rel="content-credentials"





