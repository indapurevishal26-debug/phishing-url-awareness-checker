<<<<<<< HEAD
# Python Phishing URL Awareness Checker

## Project Overview

The **Python Phishing URL Awareness Checker** is a simple educational tool that checks a URL for selected warning signs commonly associated with suspicious links.

It is designed to support phishing awareness. It does **not** confirm whether a website is safe or malicious.

## Features

The checker looks for these warning signs:

1. The URL contains an `@` symbol.
2. The URL is longer than 100 characters.
3. The hostname appears to be an IPv4 address.
4. The hostname contains five or more dot-separated parts.
5. The hostname contains `xn--`, which can appear in internationalized domain names.
6. The URL uses HTTP instead of HTTPS.

The program also supports checking multiple URLs in one session, handles malformed URL input, and displays a review message when warning signs are found.

## Requirements

- Python 3.10 or later
- No additional Python packages are required; the project uses Python's standard library.

## Project Structure

```text
phishing-url-awareness/
├── phishing_checker.py
├── requirements.txt
├── README.md
├── tests/
│   └── test_samples.md
└── screenshots/
    ├── sample_run.png
    └── test_results.png
```

## How to Run

1. Open a terminal in the project folder.
2. Run:

   ```bash
   python phishing_checker.py
   ```

3. Enter a URL when prompted.
4. Enter another URL to check another link.
5. Enter `q`, `quit`, or `exit` to stop the program.

## Sample Test Cases

| Input | Expected result |
|---|---|
| `https://www.example.com/login` | No listed warning signs |
| `http://192.0.2.10/account` | IP-address and HTTP warnings |
| `http://example.com@sample.invalid/login` | `@` and HTTP warnings |
| `https://a.b.c.d.e.example.invalid/path` | Many hostname segments warning |
| `https://xn--example.invalid/` | Punycode warning |

Record the actual output from your program in `tests/test_samples.md`.

## Screenshots

### Sample Run

![Sample run](screenshots/sample_run.png)

### Test Results

![Test results](screenshots/test_results.png)

## Limitations

- The checker uses a small set of URL patterns and may miss phishing links.
- A warning does not prove that a URL is malicious.
- A URL with no listed warning signs is not guaranteed to be safe.
- The program does not visit websites, check domain reputation, or verify website content.

## Ethical Use

Use this tool for learning and awareness. Do not use it to access, disrupt, or test websites without authorization.

## Author

Name: Vishal Indapure
=======
# phishing-url-awareness-checker
A beginner-friendly Python tool that checks URLs for common phishing warning signs and provides awareness-focused guidance.
>>>>>>> 2a3ca4c3280ce974214f9726ae3c029ab35f0229
