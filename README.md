<!--MODERNIZED:v1-->
# Damageddocx2txt

> Migrated from SourceForge via SF2GH Migrator

[![Live page](https://img.shields.io/badge/live-page-ff2e93?style=for-the-badge)](https://socrtwo.github.io/damageddocx2txt-SF/)
[![Releases](https://img.shields.io/github/v/release/socrtwo/damageddocx2txt-SF?style=for-the-badge&color=7c3aed)](https://github.com/socrtwo/damageddocx2txt-SF/releases)
[![License](https://img.shields.io/github/license/socrtwo/damageddocx2txt-SF?style=for-the-badge&color=22d3ee)](https://github.com/socrtwo/damageddocx2txt-SF/blob/main/LICENSE)
[![Last commit](https://img.shields.io/github/last-commit/socrtwo/damageddocx2txt-SF?style=for-the-badge&color=34d399)](https://github.com/socrtwo/damageddocx2txt-SF/commits)

🌐 **Live:** https://socrtwo.github.io/damageddocx2txt-SF/  
📦 **Downloads:** [Releases](https://github.com/socrtwo/damageddocx2txt-SF/releases)  
📂 **Source:** [socrtwo/damageddocx2txt-SF](https://github.com/socrtwo/damageddocx2txt-SF)

---

Salvage readable text from damaged Microsoft Word **`.docx`** (Word 2007+) files
when Word itself refuses to open them — by parsing the XML inside the zip
package directly and bypassing Word's strict validation. Originally a
Windows/Perl command-line tool migrated from SourceForge; now a fully offline,
cross-platform **web / PWA** app that runs entirely in your browser. Your file
never leaves your device.

**Language:** JavaScript (zero dependencies) · **License:** MIT

## Features

- **Three-stage recovery**, all client-side:
  1. **Standard ZIP read** — opens the archive and validates each entry.
  2. **Low-level byte scan** — when the central directory is destroyed, scans the
     raw bytes for ZIP local-file headers and rebuilds entries one by one.
  3. **XML repair & text rescue** — fixes truncated/malformed XML, then pulls the
     text of every paragraph from `word/document.xml` (plus headers, footers and
     notes), bypassing Word's strict validation.
- **Primary output: clean `.txt`** — one line per paragraph, tabs and line
  breaks preserved. A best-effort repaired `.docx` is also offered.
- **100% offline** — installable as a PWA; works with no network after first load.
- **No upload, no server** — recovery happens locally via the browser's native
  `DecompressionStream`/`CompressionStream`.

## Install & run

**Easiest — use the hosted app (and install it):**
Open <https://socrtwo.github.io/damageddocx2txt-SF/> and click the browser's
install icon (Chrome/Edge) or *Share → Add to Home Screen* (iOS Safari) to get
an offline desktop/home-screen app.

**Or download a platform bundle from [Releases](https://github.com/socrtwo/damageddocx2txt-SF/releases):**

| Platform | Bundle | How to run |
| --- | --- | --- |
| Windows  | `damageddocx2txt-<ver>-windows.zip`   | Unzip, double-click `DamagedDocx2Txt.bat` |
| macOS    | `damageddocx2txt-<ver>-macos.zip`     | Unzip, double-click `DamagedDocx2Txt.command` |
| Linux    | `damageddocx2txt-<ver>-linux.tar.gz`  | Extract, run `./damageddocx2txt.sh` |
| ChromeOS | `damageddocx2txt-<ver>-chromeos.zip`  | Install the PWA, or open `web/index.html` in Chrome |
| Android  | `damageddocx2txt-<ver>-android.zip`   | Install the PWA from Chrome |
| iOS      | `damageddocx2txt-<ver>-ios.zip`       | Add to Home Screen from Safari |
| Web      | `damageddocx2txt-<ver>-web.zip`       | Drop `web/` on any static host |

Each bundle contains the full offline app plus a per-platform launcher and
install instructions (`README.txt`). Verify downloads against `SHA256SUMS`.

## Build releases yourself

```bash
bash scripts/build-releases.sh v1.0.0   # writes bundles to dist/
node scripts/test-recovery.mjs          # run the recovery smoke tests
```

Or trigger the **Build & publish multi-platform releases** GitHub Action and
enter a version tag — it tests, builds all bundles, and attaches them to a
fresh GitHub Release.

## Origin

This project was originally hosted on SourceForge and has been migrated to GitHub for easier access and collaboration.

- **SourceForge:** [damageddocx2txt](https://sourceforge.net/projects/damageddocx2txt/)
- **Migrated with:** [SF2GH Migrator](https://github.com/socrtwo/sf-to-github)

## Contributing

Contributions are welcome! Feel free to:

1. Fork this repository
2. Create a feature branch (`git checkout -b my-feature`)
3. Commit your changes (`git commit -m "Add my feature"`)
4. Push to the branch (`git push origin my-feature`)
5. Open a Pull Request

## License

MIT License — see [LICENSE](LICENSE) for details.

---

## 📜 SourceForge heritage

This project originated on **SourceForge** before being migrated to GitHub. The legacy SourceForge entry, if still available, can be searched at:

🔗 https://sourceforge.net/projects/damageddocx2txt/

The repository here at `socrtwo/damageddocx2txt-SF` is the canonical, actively-maintained home. All future updates, issue tracking, and releases happen on GitHub.

## 🛠️ Contributing

Issues and pull requests are welcome at [https://github.com/socrtwo/damageddocx2txt-SF/issues](https://github.com/socrtwo/damageddocx2txt-SF/issues).

## 📝 License

See the [LICENSE](https://github.com/socrtwo/damageddocx2txt-SF/blob/main/LICENSE) file in this repository. If no license file is present, the project is shared as-is for reference and personal use; please contact the maintainer for other use cases.

---

*Maintained by [@socrtwo](https://github.com/socrtwo)*