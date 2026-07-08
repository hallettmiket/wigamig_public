# Join a wigamig institution

**wigamig** is shared AI research infrastructure used by universities and
research centres. **How you join depends on who you are** — a *member* joining a
lab or core that already exists, or a *PI* starting a new one.

> This page is a **directory**, and it collects **nothing** — no form, no issues.
> A join request is **encrypted to your institution's registrar** and emailed to
> them; only they can read it, and nothing about you is ever posted publicly.

## Joining a lab or core that already exists? (most people)

**You don't contact anyone here — talk to your PI** (your lab or core leader).
They add you to the group and issue you a **signed membership card**. You install
wigamig ([the same command PIs use](#1-install-wigamig-first)) and import the card
with one command (`wigamig import-card`); your dashboard then recognises your role.
The mayor and this directory are **not** involved for members.

*(Curious how the card works? See
[`docs/identity.md`](https://github.com/hallettmiket/wigamig/blob/main/docs/identity.md).)*

## Starting a new lab or core? (you're the PI)

Only **PIs** contact the mayor — and only to stand up a new lab or core. Two
steps, in order:

### 1. Install wigamig first

The code is public; installing just gets your computer ready (you only need `git`).

```sh
curl -fsSL -O https://raw.githubusercontent.com/hallettmiket/wigamig_public/main/install-wigamig.sh
sh install-wigamig.sh
```

It downloads wigamig to `~/repos/wigamig`, installs the `wigamig` command, and
wires up the shared agents, rules, and tools (installing the `uv` helper for you
if you don't already have it). The code lives at
[github.com/hallettmiket/wigamig](https://github.com/hallettmiket/wigamig).

### 2. Send the mayor an encrypted join request

Run the join script. It asks a few questions, **encrypts** your request to your
institution's registrar key, and opens your email app with it ready to send.

```sh
curl -fsSL -O https://raw.githubusercontent.com/hallettmiket/wigamig_public/main/join/wigamig-join.sh
sh wigamig-join.sh
```

Press **Send**. Your request is encrypted so only your registrar can read it, and
nothing is posted publicly. *(Prefer to do it by hand?
[`join/join-form.txt`](join/join-form.txt) is the plain form, and the directory
below has each registrar's email + encryption key.)*

**After you send it**, watch for a reply from the **Mayor**: an email, a Slack
invite to your `wigamig-<centre>` workspace, and your signed **PI card** to
import. If a few days pass with no reply, nudge them by replying to your own sent
email.

## Institutions using wigamig

One institution may run more than one installation (a centre, a department, a
named group), so match on the institution *and* the description. Each row's
**age key** is the public key the join script encrypts to.

| Institution | Installation | Email to join | age key (encrypt to this) |
|---|---|---|---|
| Western University | Western QA Centre | tbrowne5@uwo.ca | age1pa3tqu0xlcm0tqmgr5j63nh50k2xhvxd2yfcxd760dxyhuzat9nqqmexah |

**Don't see your institution?** It may not run wigamig yet — ask your PI or lab
manager. (Registrars add their row here when they go live.)
