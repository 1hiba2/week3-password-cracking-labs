# What I Learned

Working through these labs helped me understand the difference between extracting a password hash and recovering the original password. The hash extraction step prepared the PDF for testing, while the wordlist attack tried candidate passwords.

I used both the John the Ripper command-line utilities and the Johnny graphical interface. I also fixed a Windows setup problem: Perl was not recognized at first, but after installing Strawberry Perl and opening a new Command Prompt, `pdf2john.pl` worked.

The two labs showed different approaches to the same kind of task: a local workflow with John the Ripper and a browser-based workflow with Networkwalks tools. I verified both results by opening the training PDFs and viewing their flag pages.
