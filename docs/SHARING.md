# Sharing Guide

> Language: English | 中文：[`SHARING.zh-CN.md`](SHARING.zh-CN.md)

## What you can share (no NDA)
Simplest:
- Send this single file (English, default): `docs/nonconfidential/Eco-Cat-Food_Technical_Package_NONCONFIDENTIAL_SINGLE_v0.9_2026-02-10.en-US.md`
- Optional Chinese version: `docs/nonconfidential/Eco-Cat-Food_Technical_Package_NONCONFIDENTIAL_SINGLE_v0.9_2026-02-10.zh-CN.md`

Or (if you prefer a folder/zip):
- Share only: `docs/nonconfidential/` (exclude any `archive/` local drafts)

Do **not** share:
- `docs/_confidential_DO_NOT_SHARE/`
- any `references/` content
- any PDFs, screenshots, or extracted figures

## Quick packaging (Windows PowerShell)
To create a zip that contains only the shareable package files (excluding any local drafts):

```powershell
$root = Resolve-Path .
$src = Join-Path $root "docs\nonconfidential"
$dst = Join-Path $root "Eco-Cat-Food_NonConfidential_Package.zip"
if (Test-Path $dst) { Remove-Item $dst -Force }
$paths = @(
  Join-Path $src "00-PACKAGE_INDEX.NC.md",
  Join-Path $src "00-PACKAGE_INDEX.NC.zh-CN.md",
  Join-Path $src "04-References.NC.tsv",
  Join-Path $src "04-References.NC.csv",
  Join-Path $src "05-DOI-Verification.NC.tsv",
  Join-Path $src "05-DOI-Verification.NC.csv",
  Join-Path $src "Eco-Cat-Food_Technical_Package_NONCONFIDENTIAL_SINGLE_v0.9_2026-02-10.en-US.md",
  Join-Path $src "Eco-Cat-Food_Technical_Package_NONCONFIDENTIAL_SINGLE_v0.9_2026-02-10.zh-CN.md"
)
Compress-Archive -Path $paths -DestinationPath $dst
```

## Notes
See `docs/nonconfidential/00-PACKAGE_INDEX.NC.md` for what is included/excluded in the non‑confidential package.
