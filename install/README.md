# CMSC 205 - Data-Scientific Programming

## Software

1. Install the following software. If you already have R and RStudio installed, please re-install both to make sure that you have the most up-to-date versions.

- [R](https://cran.r-project.org/) programming language and software environment for statistical computing and graphics
- [RStudio](https://www.rstudio.com/products/rstudio/download3/) integrated development environment (IDE) for R.
    + On Macs, when prompted to install command line developer tools, select "Install"
    + On Windows, you should get a similar prompt.

- LaTeX:
    + [MacTeX](https://tug.org/mactex/downloading.html) for Mac (2.5GB)
    + [MiKTeX](https://miktex.org/download) for Windows (176MB)

- [Git](https://git-scm.com/) open source distributed version control system

2. Ensure you can login to RStudio Server from your browser at [rstudio.lawrence.edu](https://rstudio.lawrence.edu). You must be on campus to login to the server.


#### R markdown

1. Open RStudio and starting in the menu bar, go to File -> New File -> R Markdown…
2. If prompted to install any packages, say yes.
3. Give it an arbitrary title and select the PDF output format.
4. A document Untitled1 should pop-up. In that panel, click on Knit.
5. Give the file a name and save

A PDF document should pop-up. Then

1. Click on the downward point black arrow next to the Knit button and select Knit to HTML

The same analysis as the PDF above should appear on a webpage.

#### Installing Packages

Next, we need to install R packages, or extensions to R, from the [CRAN repository of packages](https://cran.r-project.org/web/packages/available_packages_by_name.html).

- In one of the panels in RStudio, there is a tab *Packages*.
- Click Install and in the Packages field type `tidyverse` to install the package.
- If prompted to restart R, say yes.
- In another panel, there is a tab Console. Type `library(tidyverse)` and ensure the resulting messages does not contain any error messages.

#### Github

GitHub is a web-based Git repository hosting system.

- Go to [GitHub](https://github.com/), create an account using your `@lawrence.edu` account, and verify your email.
- Edit your profile:
    + Change your profile picture to a cropped picture of you (this will help me learn your names faster)
    + Add your name
    + (Optional) Add your personal email
- Go to [GitHub Education](https://education.github.com/discount_requests/new)
    + Request an "Individual Account" discount
    + For "How do you plan to use GitHub?" type in: For my Lawrence University CMSC 205 Data-Scientific Programming course https://github.com/cmsc205

