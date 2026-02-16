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

Q3: What is a "Build Artifact" and how would a Deployment team use it?

A3:Files produced as a result of build process, used for software development, team can use this because includes documents and executables
