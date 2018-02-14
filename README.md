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
