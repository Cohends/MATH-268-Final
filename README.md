# MATH 268 Final Project — Team 6

This repository contains our group’s project proposal, data, analysis code,
and reports for Math 268: Data Analysis and Visualization.

## Team Members

- Dylan Cohen
- Parash Khanal
- Livia Leneweaver
- Max Tyree

## Project Topic

[Add our selected topic and a brief description.]

### Main Question

[Add the main research question.]

## Project Files

- `README.md`: Project overview and collaboration instructions.
- `.qmd` file: Main Quarto document containing our writing, R code,
  visualizations, and analysis.
- `project_templet.scss`: Required stylesheet used when rendering the report.
- `data/`: Original data files used in the analysis.
- Rendered `.html` file: Report generated from the Quarto document.
- `.Rproj` file, if included: Opens the project in RStudio.

Keep the Quarto document and `project_templet.scss` together.
Keep original data unchanged and perform cleaning in R code.

Edit the `.qmd` source, not the generated HTML report.

## Required Software

Each team member needs:

1. R.
2. RStudio Desktop.
3. Git installed on their computer.
4. A GitHub account with access to this repository.

The current project template uses these R packages:

```r
install.packages(c("tidyverse", "here"))
```

Run the installation command once in the RStudio Console.
The project document loads the packages when it runs.

## First-Time Git and RStudio Setup

### 1. Get access to the repository

Send your GitHub username to the repository owner so they can invite you
as a collaborator. Accept the invitation before trying to push changes.

Everyone should use their own GitHub account.

### 2. Check that RStudio detects Git

In RStudio:

1. Open Tools → Global Options → Git/SVN.
2. Make sure Git version control is enabled.
3. Check that the Git executable field points to your Git installation.
4. Restart RStudio after installing Git or changing its configuration.

### 3. Set your Git name and email

Open the Terminal tab in RStudio, not the R Console, and run:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-github-email@example.com"
```

Replace the examples with your own information.
Use an email associated with your GitHub account, or your GitHub
provided no-reply email.

### 4. Download the repository into RStudio

You only need to clone the repository once per computer.

1. Open this repository on GitHub.
2. Click the green Code button.
3. Copy the HTTPS repository URL.
4. In RStudio, select File → New Project → Version Control → Git.
5. Paste the URL into Repository URL.
6. Choose where to save the project on your computer.
7. Click Create Project.

RStudio will download the repository and open it as a project.

For future work, reopen this project instead of cloning it again.

### 5. Authenticate with GitHub

When Git asks you to authenticate, complete the sign-in process offered
by your computer’s Git credential manager.

GitHub does not accept your normal account password for HTTPS Git
operations. If a password prompt requires a token, use a personal access
token with access to this repository.

Never put a password or access token in the README, project code,
or any committed file.

## Everyday Workflow in RStudio

GitHub is not live editing like Google Docs.
Each person works on a local copy and shares saved changes through Git.

### Before editing

1. Open the correct RStudio project.
2. Check the Git tab for any unfinished local changes.
3. If your working copy is clean, click Pull to download the latest changes.
4. Tell the group which section or file you will work on.

If you already have local changes, finish and commit them before pulling.
Do not discard changes just to make Pull work.

### After editing

1. Save the files you changed.
2. If you changed the report or analysis, render the `.qmd` and check it.
3. Open the Git tab.
4. Click Diff or Commit to review your changes.
5. Check the Staged box for the files you want to include.
6. Write a short, specific commit message.
7. Click Commit.
8. Click Pull to incorporate any updates made while you were working.
9. Resolve any conflicts if necessary.
10. Click Push to upload your commits to GitHub.

If Git requests a merge commit after pulling, complete that commit
before pushing.

### What the Git buttons mean

- Pull: Download and integrate changes from GitHub.
- Diff: Review what changed in a file.
- Stage: Select changes to include in the next commit.
- Commit: Record the staged changes locally.
- Push: Upload local commits to GitHub.

Saving is not the same as committing.
Committing is not the same as pushing.

### Example commit messages

- Add data source and variable descriptions
- Write introduction and main question
- Add missing-value checks
- Revise follow-up questions and evidence plan
- Fix chart labels and rendering errors

## Avoiding Conflicts

For this project, coordinate before editing shared files.

- Work on different sections or files when possible.
- Announce when you are editing the main `.qmd`.
- Pull before starting and push when you finish.
- Make small commits with clear messages.
- Do not rename or move shared files without telling the group.
- Do not overwrite someone else’s work to fix a conflict.
- Do not force-push to the shared branch.

Working on different sections reduces conflicts, but does not eliminate
them when multiple people edit the same file.

## If a Merge Conflict Happens

A conflict means Git needs help combining overlapping changes.

1. Read the conflict message and identify the affected file.
2. Open the file and find the conflict markers:

```text
<<<<<<< HEAD
One version of the text
=======
The other version of the text
>>>>>>> other-commit
```

3. Check with the teammate who edited that section.
4. Keep or combine the correct content.
5. Remove the conflict marker lines.
6. Save the file.
7. Render the report if the conflict affected the `.qmd`.
8. Stage and commit the resolved file.
9. Push the completed changes.

Do not delete the file or choose a version without reviewing both sides.

## Running and Rendering the Report

1. Open the project in RStudio.
2. Open the main `.qmd` file.
3. Confirm that the required data files are present.
4. Confirm that `project_templet.scss` is next to the `.qmd`.
5. Click Render.
6. Review the generated HTML report.

Check that:

- The document renders successfully.
- Charts and tables display correctly.
- Data paths work on other team members’ computers.
- Reported analysis numbers come from code.
- The final output does not contain unwanted messages, warnings,
  or raw printed datasets.

Use project-relative paths instead of personal paths such as
`C:/Users/YourName/Downloads/...`.

The template’s example uses:

```r
here("project", "data", "your_file.csv")
```

That example assumes the project root is the folder above `project/`.
If our repository root is the folder containing the `.qmd` and `data/`,
use this layout instead:

```r
here("data", "your_file.csv")
```

Agree on one folder structure and use it consistently.

## Proposal Checklist

### Introduction

- Include a concrete number explaining why the topic matters.
- Cite the source of that number.
- Link one or two existing analyses.
- Explain specifically how our project differs.

### Research Questions

- State the main question in the report title.
- Make the main question clear, focused, arguable, and not yes/no.
- Include four to six connected follow-up questions.
- Give each follow-up question a job:
  establishes, stress-tests, questions, or extends.
- Make every question about the real world and answerable with our data.

### Planned Evidence

- Match every question with suitable evidence.
- Name the variables used, not just the chart type.
- Include at least two of these course topics:
  relationships, time, and clusters.

### Data Description and Quality

- Cite the dataset source and date accessed.
- Explain who collected the data, when, and how.
- Explain what one row represents.
- Report the dataset size.
- Include a variable description table.
- If using multiple datasets, explain which questions each supports.
- Check missing values, including who or which groups are missing.
- Check unknown codes and outliers.
- Include numerical findings and one or two data-check charts.
- Discuss missing populations, possible bias, and what the data cannot show.

### Submission

- Use the required project template and stylesheet.
- Confirm the report renders as submitted.
- Describe each member’s specific contributions.
- Include an accurate AI use statement.
- Check the course instructions for the deadline and required files.

The rubric specifies a 10% deduction for submitting without the required
project template and `project_templet.scss`. Late submissions are not accepted.

## Member Contributions

Update this section at each milestone to reflect work actually completed.

- Dylan Cohen: [Specific contribution]
- Parash Khanal: [Specific contribution]
- Livia Leneweaver: [Specific contribution]
- Max Tyree: [Specific contribution]

Also update the Member Contributions section in the submitted report.

## AI Use

[Describe any AI assistance actually used, including its purpose and
how the team checked the result. If none was used, write “None.”]

Also update the AI Use Statement in the submitted report.
