# Common Username Generator
This project contains a web-based application that generates lists of statistically common usernames based on patterns observed in public data and security research. Users can generate lists of varying sizes and export them in different formats.

##### This repository provides two ways to use the generator:

* A live web application hosted via GitHub Pages.
* A GitHub Action that automatically generates the username lists and saves them as downloadable artifacts.

## Live Application (GitHub Pages Website)
You can access the live version of the username generator, hosted directly from this repository using GitHub Pages.

### Features

**Generate Username Lists:** 
Create lists of three different sizes:
- **Small** (~1,000 usernames)
- **Medium** (~10,000 usernames)
- **Large** (~100,000 usernames)

**Pattern-Based Generation:** 
Usernames are generated based on a combination of common patterns, including:
- **Personal names** (e.g., john.smith, jessica89)
- **Lexical themes** (e.g., shadowmaster, coolgamer)
- **Numerical sequences** (e.g., 123456)
- **System and role-based names** (e.g., admin, support)

**Export Functionality:** 
Download the generated list in the following formats:
* .txt
* .pdf
* .doc

## Automated Generation (GitHub Actions)
This repository is configured with a GitHub Action that runs every time code is pushed to the main branch. This action performs the following steps:

- Sets up a Node.js environment.
- Runs a script to generate three usernames.txt files (small, medium, large).
- Uploads these files as build artifacts.

You can find the generated lists in the "Actions" tab of this repository. After a successful run, you will see an "Artifacts" section on the summary page for that run, where you can download a zip file containing the username lists.

### How to Use the GitHub Action

- Navigate to the Actions tab in this repository.
- Click on the latest workflow run.
- Under the Artifacts section, you will find a file named username-lists.
- Download the zip file and extract it to access the .txt files.

## How It Works
The generation logic is contained within the <script> tag in the index.html file. It uses several arrays of common names, words, and adjectives as data sources. When the "Generate" button is clicked, it randomly combines these elements based on weighted probabilities to create a list of unique usernames.
