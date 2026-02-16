# DevOpsDemo

These hands-on exercises will teach you Continuous Integration (CI) using GitHub Actions.
Each lab builds on previous concepts, helping you understand how CI automates testing,
building, and validating code changes.


  Checkpoint 1
  
Q1: What is the "Trigger" in this workflow? (What makes the script start?)
  
A1: Commiting a change the repository

Q2: Where is the computer located that actually runs the echo command?
   
A2:

    ```
    Hosted Compute Agent
    Version: 20260123.484
    Commit: 6bd6555ca37d84114959e1c76d2c01448ff61c5d
    Build Date: 2026-01-23T19:41:17Z
    Worker ID: {75e1c7c9-df8e-440d-9d76-a3d3f80375f0}
    Azure Region: westus3
   
Q3: If you create a new file called test.txt and push it, will this Action run again?
Why?

A3: Auto Runs at commit

  Checkpoint 2
Q1: When the test failed, what color icon appeared in GitHub?

A1: Red
   
<img width="657" height="232" alt="image" src="https://github.com/user-attachments/assets/9e79464a-7c3d-4d76-b1c3-75791187ad20" />

Q2: Why do we need the actions/checkout@v4 step? What happens to the code if we
delete that line?

A3: Sync with Latest of Repository and Testing, If we delete, it wont update to latest commit

Q3: In a real job, why is it better for the CI to find this error than a customer?

A3: Small Errors That cause in Real Development may break code, so better to use tools like actions to do testing and running of code.

Checkpoint 3

Q1: Why did we use a "Secret" instead of just typing the API Key into the app.js file?

A1:  It is an Environment Variable which contains sensitive data and not to be shared publicly

Q2: What is the benefit of testing on two different Node.js versions (Matrix)?

A2: Compatibiliity for all users and No dependency Problems

Q3: What is a "Build Artifact" and how would a eployment team use it?

A3:Files produced as a result of build process, used for software development, team can use this because includes documents and executables

Checkpoint 4
Make a test fail intentionally and observe the CI failure [x]
  
Add a new function and test to the calculator [x]
  
Fix the failing test and see CI pass [x]

Checkpoint 5

Q1: Do the jobs run in parallel or sequentially?

A1: Parallel by default. In GitHub Actions, separate jobs in the same workflow run in parallel unless you add dependencies with `needs`.

Q2: What happens if the Python tests pass but JavaScript tests fail?

A2: The workflow is marked as failed because at least one job failed, even if the Python job passed.


Q3: How would you make JavaScript tests depend on Python tests passing?

A3: Add `needs: test` to the JavaScript job so it only starts after the Python `test` job succeeds (or rename jobs and reference the Python job name).

Checkpoint 6

- How many total jobs will run?

A1: 15 total jobs.
- Calculate: Python jobs + Node jobs

A2: Python jobs = 3 OS * 4 Python versions = 12. Node jobs = 3 Node versions = 3. Total = 12 + 3 = 15.

- Observe which combinations might fail
A3: Python on Windows/macOS can fail if dependencies or path assumptions are Linux-only; specific Python versions could fail if a package lacks wheels. Node 18/20/21 can fail if dependencies require a different Node version.

https://drive.google.com/drive/folders/1oIS0SKJeJqzX6iGqdTH-7cYXKhMZkCtv

Create a file with name_USN.doc
Upload the All Checkpoint answers(1-6):
https://forms.gle/yZ3orxrGxaAk77aWA