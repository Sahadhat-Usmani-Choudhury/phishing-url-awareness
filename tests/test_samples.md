# Test Results

Python version used: 3.15.2
Operating system: Windows
Date: 28 October 2026

| # | Input | Expected result | Actual result | Pass/Fail |
|---|-------|-----------------|---------------|-----------|
| 1 | https://www.example.com/login | No listed warning signs; not proof of safety | No listed warning signs found. This does not prove safety. | PASS |
| 2 | http://192.0.2.10/account | IP address + HTTP | IP address + HTTP | PASS |
| 3 | http://example.com@sample.invalid/login | @ symbol + HTTP | @ symbol + HTTP | PASS |
| 4 | https://a.b.c.d.e.example.invalid/path | Many hostname segments | Many hostname segments |PASS |
| 5 | https://xn--example.invalid/ | Punycode-style hostname | Punycode-style hostname | PASS |

## Notes

## Notes

From this testing, I learned how to compare the expected result with the actual output of my program and decide whether a test passed or failed. I also learned that one URL can contain more than one warning sign. What surprised me most was that a URL could show no listed warning signs without being guaranteed safe. This helped me understand that my program checks only a few selected clues and cannot give a final decision about a URL’s safety.