# 📧 EmailFinder

![License](https://img.shields.io/badge/license-GPLv3-blue)
![Python](https://img.shields.io/badge/python-3.x-green)

> A powerful email extraction tool that crawls websites to discover email addresses efficiently.

<p align="center">
  <img src="demo.gif" alt="EmailFinder Demo" width="700">
</p>

## ✨ Features

- 🔍 **Automatic Crawling**: Traverses all page routes within the same domain
- 📋 **Batch Processing**: Process multiple URLs from a text file
- 🧠 **Smart Detection**: Uses advanced regex patterns to identify valid emails
- 🚀 **Multithreaded**: Efficiently processes multiple websites concurrently
- 💻 **User-Friendly**: Simple command-line interface with progress indication

## 📋 Prerequisites

- Python 3.x
- Virtual environment (recommended)

## 🚀 Installation

```bash
# Clone the repository
git clone https://github.com/AyraStelmaszewski/emailFinder.git

# Navigate to the project directory
cd emailFinder

# Set up a virtual environment
python3 -m venv venv

# Activate the virtual environment
# On Linux/macOS:
source venv/bin/activate
# On Windows:
# venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## 💻 Usage

### Processing a single URL

```bash
python emailFinder.py example.com
```

### Processing multiple URLs from a file

```bash
python emailFinder.py urls.txt
```

### Example file format (urls.txt)

```
example.com
another-website.com
third-example.net
```

## 🔍 How It Works

1. The tool parses the input (single URL or file with URLs)
2. For each URL, it discovers all internal links within the same domain
3. It crawls each discovered page, searching for email patterns
4. Valid emails are extracted, filtered, and displayed in the terminal

## 📊 Output Example

```
==============================================
 - Took 1m45s to find 24 emails from urls.txt
 - All collected emails:
==============================================
contact@example.com
support@website.com
info@company.org
sales@business.net
...
```

## ⚙️ Configuration

The tool uses sensible defaults, but you can modify these variables in the code:

- `emailReg`: The primary regex pattern for email detection
- `secondReg`: The secondary filter regex to avoid invalid matches
- Thread pool settings for performance tuning

## ⚠️ Legal Disclaimer

**Important:** Email scraping may be subject to legal restrictions:

- This tool is provided for educational purposes only
- Business email addresses associated with individuals (e.g., john.doe@company.com) may be considered personal data under privacy laws like GDPR
- Always ensure you have proper authorization before scraping websites
- The authors assume no liability for misuse of this tool

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the GNU General Public License v3.0 - see the LICENSE file for details.

## 🔗 Links

- [Project Repository](https://github.com/AyraStelmaszewski/emailFinder)
- [Report Issues](https://github.com/AyraStelmaszewski/emailFinder/issues)

