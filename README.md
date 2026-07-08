# Download Wigamig

**wigamig** is shared AI research infrastructure for universities and research
centres. To use it, install it on your computer — the code is public and this one
command does everything (you only need `git`):

```sh
curl -fsSL -O https://raw.githubusercontent.com/hallettmiket/wigamig_public/main/install-wigamig.sh
sh install-wigamig.sh
```

It downloads wigamig to `~/repos/wigamig`, installs the `wigamig` command, and
wires up the shared agents, rules, and tools. The source lives at
[github.com/hallettmiket/wigamig](https://github.com/hallettmiket/wigamig).

Then find your situation below.

---

## I'm a member of a lab that already uses wigamig

Just ask your **PI** for a **membership certificate**. They issue it to you; you
run the one `wigamig import-card` command they give you, and your dashboard
recognises your role. That's it — you don't email the mayor or touch this
directory.

## I'm a PI of a lab or core

Install wigamig (above), then **accept members by issuing them certificates**. A
member requests one with `wigamig enroll`; you sign and return it with:

```sh
wigamig issue-member-card <their-request> --group <your-lab>
```

Full walkthrough:
[`docs/identity.md`](https://github.com/hallettmiket/wigamig/blob/main/docs/identity.md).

## My institution runs wigamig and I want to start a lab or core

You need the **mayor** to register your group. Send them an encrypted request —
one script asks a few questions, encrypts it to your institution's key, and opens
your email ready to send:

```sh
curl -fsSL -O https://raw.githubusercontent.com/hallettmiket/wigamig_public/main/join/wigamig-join.sh
sh wigamig-join.sh
```

Nothing about you is posted publicly — the request is encrypted so only your
institution's registrar can read it. Find your institution in the directory
below. Once the mayor approves, they send you back your **PI certificate** to
import.

## I want to run wigamig at my institution

You'll bootstrap a new **centre** and become its *mayor*. Install wigamig (above),
then follow the mayor setup in the code repo:
[github.com/hallettmiket/wigamig](https://github.com/hallettmiket/wigamig) →
**"Install wigamig at your institution."**

## Institutions using wigamig

One institution may run more than one installation (a centre, a department, a
named group), so match on the institution *and* the description. The **age key**
is the public key the join script encrypts to.

| Institution | Installation | Email to join | age key (encrypt to this) |
|---|---|---|---|
| Western University | Western QA Centre | tbrowne5@uwo.ca | age1pa3tqu0xlcm0tqmgr5j63nh50k2xhvxd2yfcxd760dxyhuzat9nqqmexah |

**Don't see your institution?** It may not run wigamig yet — ask your PI or lab
manager. (Registrars add their row here when they go live.)
