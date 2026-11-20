# Week 3 — PDF Password Recovery Labs

Hands-on cybersecurity labs completed on Windows 10 using John the Ripper, Johnny GUI, and Networkwalks password-recovery tools.

## What I worked on

| Lab | Tools | Result |
| --- | --- | --- |
| Module 1 — Password Cracking with JTR | John the Ripper, Johnny, `pdf2john.pl`, Strawberry Perl | Recovered the PDF password and captured the flag |
| Module 2 — Password Cracking with Networkwalks Tools | Networkwalks Hash Calculator and Password Cracker | Unlocked the lab PDF and captured the flag |

## Module 1 — John the Ripper

I set up John the Ripper and Johnny on Windows, configured Johnny to use `john.exe`, and installed Strawberry Perl to run `pdf2john.pl`. I extracted the hash from `My Locked PDF1.pdf` and loaded the resulting text file into Johnny. I used the bundled `password.lst` wordlist to test the hash.

Commands I used from John the Ripper's `run` folder:

```cmd
perl -v
perl pdf2john.pl "..\..\My Locked PDF1.pdf" > pdf1_hash.txt
type pdf1_hash.txt
```

Johnny identified the hash format as **PDF** and showed **100% complete — 1 of 1 cracked**.

- Recovered password: `good-luck`
- Captured flag: `nw{cybersecurity_flag_captured_2608}`

See [my Module 1 notes](docs/module1-jtr.md).

## Module 2 — Networkwalks Tools

I used the Networkwalks Hash Calculator to extract the hash from the separate lab PDF, then used the Networkwalks Password Cracker to recover its password. After opening the PDF, I reached the flag page.

- Captured flag: `nw{networkwalks_flag1_jtr_270521_1}`

See [my Module 2 notes](docs/module2-networkwalks.md).

## Project files

```text
week3-password-cracking-labs/
├── README.md
├── .gitignore
├── docs/
│   ├── module1-jtr.md
│   ├── module2-networkwalks.md
│   └── what-i-learned.md
└── screenshots/
    ├── module1-jtr/
    └── module2-networkwalks/
```

## What I learned

I practiced extracting a PDF password hash, using a wordlist with John the Ripper, working with both command-line and graphical tools, and verifying a recovered password by opening the PDF. I also learned how to troubleshoot a missing Perl installation on Windows.

These exercises were performed using the training files supplied for the labs.
