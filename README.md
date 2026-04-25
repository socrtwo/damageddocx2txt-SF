# Corrupt DOCX Salvager

<!--PAGES_LINK_BANNER-->
> 🌐 **Live page:** [https://socrtwo.github.io/damageddocx2txt-SF/](https://socrtwo.github.io/damageddocx2txt-SF/)  
> 📦 **Releases:** [github.com/socrtwo/damageddocx2txt-SF/releases](https://github.com/socrtwo/damageddocx2txt-SF/releases)
<!--/PAGES_LINK_BANNER-->

Salvages readable text from damaged DOCX (Word 2007+) files by directly parsing the XML inside the zip archive, bypassing Word's file validation.

**Language:** Perl  
**License:** MIT

## Features

- Extracts text from corrupt DOCX files
- Parses document.xml directly inside the zip archive
- Bypasses Word's strict file validation
- Command-line interface for scripting and batch use
- Outputs clean plain text

## System Requirements

- Perl 5.10 or later
- Linux, macOS, or Windows (with Strawberry Perl or WSL)

## Installation & Usage

### Running

```bash
# Install Perl (if not already installed)
# Linux/macOS: usually pre-installed
# Windows: download Strawberry Perl from https://strawberryperl.com/

# Run the script
perl <script_name>.pl [arguments]
```

### Dependencies

If the script uses CPAN modules, install them with:
```bash
cpan install Module::Name
```

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