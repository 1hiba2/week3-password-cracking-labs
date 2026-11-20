# Module 1 — Password Cracking with JTR

## Objective

Recover the password for the lab file `My Locked PDF1.pdf` using John the Ripper and Johnny on Windows.

## Tools

- Windows 10
- John the Ripper Jumbo 1.9.0 (Windows 64-bit)
- Johnny GUI
- Strawberry Perl 5.42.3
- `pdf2john.pl`
- John the Ripper `password.lst` wordlist

## Steps I followed

1. Downloaded and extracted John the Ripper.
2. Installed Johnny and selected `john.exe` from the `run` folder in Johnny's settings.
3. Found `pdf2john.pl` in the `run` folder.
4. Installed Strawberry Perl after `perl -v` initially returned a command-not-recognized error.
5. Opened a new Command Prompt and confirmed that `perl -v` displayed the installed Perl version.
6. Extracted the PDF hash into `pdf1_hash.txt`.
7. Opened the hash file in Johnny and confirmed it recognized the PDF format.
8. Selected the bundled `password.lst` wordlist and ran the attack.
9. Opened the PDF using the recovered password and viewed the flag page.

## Commands

Run from the `run` directory, with the lab PDF in the `module1-JTR` directory:

```cmd
perl -v
perl pdf2john.pl "..\..\My Locked PDF1.pdf" > pdf1_hash.txt
type pdf1_hash.txt
```

## Result

- Hash format: PDF
- Johnny result: 100%, 1/1 cracked
- Password: `good-luck`
- Flag: `nw{cybersecurity_flag_captured_2608}`

## Evidence

Screenshots of Johnny's recovered password and the unlocked PDF can be placed in `screenshots/module1-jtr/`.
