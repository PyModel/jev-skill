# Contributing

Corrections and new field lessons are welcome.

## Fix a fact

Jev changes fast. If a fact in the skill is wrong, open an issue or a pull request with a link to the source: a page on docs.typesafe.ai, an SDK changelog, or a live API response. Do not paste an API key into an issue.

## Add a field lesson

Add the lesson to the shape file that matches how the system works, not what domain it serves. `skills/jev/prior-art/INDEX.md` lists the shapes. Each entry needs:

- one line on how the system uses Jev (which primitives, which loop),
- any measured number, written so it stands without a source link,
- no links and no third-party names. The shape files carry lessons, not catalogs.

A shape that tried Jev and found it a bad fit is just as useful. Add it to "Known bad fits" in `INDEX.md`.

## Before you open a pull request

```bash
python3 scripts/check_configs.py
python3 -m unittest discover -s tests -v
```

The hero card at `.github/assets/hero.png` is a designed asset. Edit it outside the repo and commit the PNG. Nothing in this repo regenerates it.

## Screenshots of the API key flow

`.github/assets/api-key/step-*.png` come from `scripts/annotate_screens.py`. The raw captures show a live key and account details, so they never go in the repo. To refresh them, capture the four console screens at 1512x807, keep the raw files outside the repo, and run `python3 scripts/annotate_screens.py /path/to/raw-dir`. Check every output image for an unmasked key or name before you commit, then revoke the key you created for the capture.
