# Murmurent Centre directory

This page lists implementations of **Murmurent** at different institutions.
You only need this repository if you're a **PI** registering a lab or core, or a **mayor**
listing a centre.

Anyone interested in obtaining Murmurent, install this first:
  [github.com/hallettmiket/murmurent](https://github.com/hallettmiket/murmurent).

> This repository only facilitates **encrypted join requests** to your institution's Mayor
> via email.

## PIs — register a lab or core

Find your institution in the directory below, then run the join script.
It asks a few questions, encrypts your request to that centre's key, and opens your email
app ready to send:

```sh
curl -fsSL -O https://raw.githubusercontent.com/hallettmiket/murmurent_public/main/join/murmurent-join.sh
sh murmurent-join.sh
```

Press **Send**. Once the mayor approves, they email you back your signed **PI ID** —
import it with:

```sh
murmurent import-card <file> --trust-root <the centre's published signing recipient>
```

Confirm the trust root's fingerprint with the mayor out-of-band (e.g. on a call) the
first time — it's what makes the chain of trust actually trustworthy.

## Mayors — list your centre

From your centre, run `murmurent centre-hub-publish` — it writes your directory row
here plus your signing key + revocation list (so members can verify IDs) and
prints a `git push` for you to run. See the mayor setup in the
[code repo](https://github.com/hallettmiket/murmurent).

## Institutions using murmurent

| Institution | Installation | Email to join | age key (encrypt to this) |
|---|---|---|---|
| Western University | Western Test Centre | tbrowne5@uwo.ca | age1y43uxhv7dp50mw8qnrqwh4wvamp7adz4alxezpxang4wn9usuumqmneuat |

