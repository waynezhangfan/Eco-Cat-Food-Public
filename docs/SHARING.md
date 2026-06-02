# Sharing Guide

> Language: English | 中文：[`SHARING.zh-CN.md`](SHARING.zh-CN.md)

## What you can share (no NDA)
Current recommended public materials:
- [README](../README.md)
- [Current public status](STATUS_UPDATE_2026-05-30.md)
- [Public disclosure scope](PUBLIC_SCOPE.md)
- [Roadmap](ROADMAP.md)

The v0.9 non-confidential technical package dated 2026-02-10 is now a superseded historical package. Do not share it as the current project technical package.

Do **not** share:
- `docs/_confidential_DO_NOT_SHARE/`
- any `references/` content
- any PDFs, screenshots, or extracted figures

## Quick packaging (Windows PowerShell)
If you need to package historical materials for audit, label the zip as historical/superseded and include the current status update:

```powershell
$root = Resolve-Path .
$src = Join-Path $root "docs\nonconfidential"
$dst = Join-Path $root "Eco-Cat-Food_Public_Status_And_Historical_Package.zip"
if (Test-Path $dst) { Remove-Item $dst -Force }
$paths = @(
  Join-Path $root "README.md",
  Join-Path $root "docs\STATUS_UPDATE_2026-05-30.md",
  Join-Path $root "docs\PUBLIC_SCOPE.md",
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
Use historical materials only when an explicit audit or historical-review context is needed. See the [historical package index](nonconfidential/00-PACKAGE_INDEX.NC.md) for the historical package status and exclusions.
