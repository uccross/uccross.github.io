# OSRE Project Ideas

How to update project ideas:

  1. Create a new branch
  2. Edit `projects.md`:
      - Try to adhere to the same format as the other projects
      - Do not edit the table of contents, it is generated automatically (and your edits will be overwritten)
      - Your research projects are on section level 2 (titles start with `## `)
      - Your project ideas are on section level 3 (titles start with `### `)
      - Make sure that mentor names include `mailto:` links
  3. Create a pull request in this repository (not your forked one) and ask for a review on cross-info@ucsc.edu

# CROSS Software Portal

How to update the data:

  1. Edit the `explore/input_lists.json` to add/remove/modify the 
     repos or organizations that get queried.

  2. Rerun the `MASTER.sh` script by doing:

     ```bash
     cd explore/scripts/
     GITHUB_API_TOKEN=<yourtoken> ./MASTER.sh
     ```

  3. Commit the changes
