# Submit Cookiefy to the Google Tag Manager Community Template Gallery

The gallery is **GitHub-based**. You do **not** submit only from inside the GTM template editor.

## Before you start

1. In GTM → **Templates** → your Cookiefy tag template → **Info** tab: check **Agree to the Community Template Gallery Terms of Service** (after reading the [Gallery ToS](https://developers.google.com/tag-platform/tag-manager/templates/gallery-tos)).
2. If you **export** from GTM, Windows may save `template (2).tpl`. **Rename** the file to **`template.tpl`** and replace the file in **this repo root**, or copy its contents over the existing `template.tpl`, then commit. The canonical copy for the gallery is the **`template.tpl` at the root of this repository**.

## Files that must exist at the repo root

| File | Notes |
|------|--------|
| `template.tpl` | Exported template; must include `___TERMS_OF_SERVICE___` and `categories` in `___INFO___` |
| `metadata.yaml` | `homepage`, `documentation`, `versions` with Git **full** commit SHAs |
| `LICENSE` | **Apache 2.0**, filename exactly **`LICENSE`** (all caps) |

`README.md` is optional but recommended.

Official reference: [Submit a template to the Community Template Gallery](https://developers.google.com/tag-platform/tag-manager/templates/gallery).

## Update `metadata.yaml` after changing `template.tpl`

Each gallery **version** points at one **commit** whose tree contains the `template.tpl` you want users to get.

1. Commit and push `template.tpl` (and any other changes) to **`main`**.
2. Copy the **full** SHA of that commit (GitHub commit page → copy SHA, or `git rev-parse HEAD` right after that commit).
3. Add a **new** entry at the **top** of `versions` in `metadata.yaml` with that `sha` and `changeNotes`. Keep older entries below (newest first).
4. Commit and push `metadata.yaml`.

If you change `template.tpl` again later, repeat: new commit → new top `versions` entry with the **new** commit SHA.

## Submit the template to Google

1. Sign in to **GitHub** with an account that can read this repository.
2. Open **[tagmanager.google.com/gallery](https://tagmanager.google.com/gallery)**.
3. Click **Submit template** (or the gallery’s equivalent control).
4. Enter this repository URL:

   **`https://github.com/SUNROS-AB/cookiefy-gtm-template`**

   (Adjust if the repo is under another org or name.)

5. Submit and wait for review (often on the order of days to a couple of weeks).

## After approval

- Keep **GitHub Issues** enabled on the repo so users can report problems.
- For updates: commit `template.tpl`, then add a new `sha` + `changeNotes` at the top of `metadata.yaml`; gallery updates usually appear within about **2–3 days** per Google’s docs.

## Sample layout

Google’s example repo: [gtm-vendor-templates/example-community-template](https://github.com/gtm-vendor-templates/example-community-template)
