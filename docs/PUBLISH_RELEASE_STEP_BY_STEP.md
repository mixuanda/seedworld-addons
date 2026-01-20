# Publish a Release (Step by Step)

## 1) Prepare the release in GitHub

1. Go to the repository on GitHub.
2. Click **Releases** in the right sidebar, then **Draft a new release**.
3. Choose a **Tag** (create a new tag if needed).
4. Enter a **Release title** and **Description**.
5. Upload release assets (ZIPs, binaries, or models) in the **Attach binaries** section.
6. Click **Publish release**.

## 2) Update manifest URLs to use release assets

1. Copy the asset URLs from the release page.
2. Replace mirror URLs in the relevant `manifests/*/manifest.json` entries with the release asset URLs.
3. Commit and push the updated manifests to `main`.

## 3) Optional checksums (recommended hardening)

Checksums are optional but recommended for integrity verification.

### Windows (PowerShell)

```
Get-FileHash -Algorithm SHA256 .\path\to\file.zip
```

### macOS

```
shasum -a 256 /path/to/file.zip
```
