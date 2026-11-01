
# Test Results

Python version used: Python 3.12.0
Operating system: Windows
Date: 28/10/2026

 # | Input | Expected result | Actual result | Pass/Fail |

 1  https://www.example.com/login | No listed warning signs | No listed warning signs found | PASS |
 2  http://192.0.2.10/account | IP address + HTTP | IP address warning + HTTP warning | PASS |
 3 http://example.com@sample.invalid/login | @ symbol + HTTP | @ symbol warning + HTTP warning | PASS |
 4  https://a.b.c.d.e.example.invalid/path | Many hostname segments | Many hostname segments/subdomains warning | PASS | 5  https://xn--example.invalid/ | Punycode-style hostname | Punycode-style hostname warning | PASS |

## Notes

The program successfully detected the five sample URL cases.
I learned how URL text can contain warning signs such as an @ symbol,
an IP address, multiple hostname segments, and a punycode marker.
No warning signs found does not prove that a URL is safe.
