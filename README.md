## 🔁 GitHub Actions CI/CD Workflow

This project uses GitHub Actions to implement a CI/CD pipeline with the following stages:

### Workflow Triggers
- **Push to `staging`** → Deploys to the staging server
- **Push to `main`** → Runs tests and build
- **Release published** → Deploys to production

### Workflow Jobs
1. **Install Dependencies** – Installs required Python packages using `pip`
2. **Run Tests** – Runs the test suite with `pytest`
3. **Build** – Prepares the application for deployment
4. **Deploy to Staging** – On push to `staging` branch
5. **Deploy to Production** – On GitHub release

### 🔐 Configuring Secrets
Set the following secrets under:
`Settings → Secrets and variables → Actions → New repository secret`

| Secret Name         | Description                          |
|---------------------|--------------------------------------|
| `SSH_PRIVATE_KEY`   | SSH private key for deployment       |
| `STAGING_HOST`      | IP/Domain of the staging server      |
| `STAGING_USER`      | Username for SSH to staging          |
| `PROD_HOST`         | IP/Domain of the production server   |
| `PROD_USER`         | Username for SSH to production       |

---

## 📦 Running Locally

```bash
# Install dependencies
pip install -r requirements.txt

# Run tests
pytest
# CI-CD flask-application

---

### 📸 3. **Screenshots of Workflow Runs**

Take screenshots of:
- Successful run for push to `staging` showing:
  - Dependency installation
  - Test execution
  - Build step
  - Deploy to staging step
- Successful release triggering production deployment

#### Tips:
- Go to the **Actions** tab of your GitHub repo
- Click on a run → Expand each step and take screenshots
- Save as `ci-run-staging.png`, `ci-run-release.png`, etc.

---

### 📤 4. **Submit**

- ✅ GitHub repo URL with:
  - Workflow file
  - Working Flask app
  - Updated `README.md`

- ✅ Upload screenshots or include them in your submission folder.

---

If you’d like, share your GitHub repo link and I can review your `README.md`, workflow file, and setup for any missing parts.
pytest
Usage: flask [OPTIONS] COMMAND [ARGS]...

  A general utility script for Flask applications.

  An application to load must be given with the '--app' option, 'FLASK_APP'
  environment variable, or with a 'wsgi.py' or 'app.py' file in the current
  directory.

Options:
  -e, --env-file FILE   Load environment variables from this file. python-
                        dotenv must be installed.
  -A, --app IMPORT      The Flask application or factory function to load, in
                        the form 'module:name'. Module can be a dotted import
                        or file path. Name is not required if it is 'app',
                        'application', 'create_app', or 'make_app', and can be
                        'name(args)' to pass arguments.
  --debug / --no-debug  Set debug mode.
  --version             Show the Flask version.
  --help                Show this message and exit.

Commands:
  routes  Show the routes for the app.
  run     Run a development server.
  shell   Run a shell in the app context.
Command 'pytest' not found, but can be installed with:
sudo apt install python3-pytest
Microsoft Windows [Version 10.0.26100.3775]
(c) Microsoft Corporation. All rights reserved.

C:\Windows\System32>wsl
Welcome to Ubuntu 24.04.2 LTS (GNU/Linux 5.15.167.4-microsoft-standard-WSL2 x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Thu May 15 05:15:24 UTC 2025

  System load:  0.4                 Processes:             57
  Usage of /:   0.3% of 1006.85GB   Users logged in:       0
  Memory usage: 6%                  IPv4 address for eth0: 172.24.99.238
  Swap usage:   0%


This message is shown once a day. To disable it please create the
/home/suva/.hushlogin file.
suva@BWULPT931:/mnt/c/Windows/System32$ ls /mnt/d
'$RECYCLE.BIN'             IVF                   SUVA
 BANK                      KYC                  'Staff Notice 2023_06_16_006 No Smoking inside the Campus.pdf'
 BRAINWARE                 PAYSLIP              'System Volume Information'
 CAST_HIGHERARCHY         'PHD NIT'              TCS
 CESC                      PHOTO                 TOYOTA
 COMPLAIN                  PIU                  'TRADING FX ROAD'
 EXPERIENCE_CV            'SAKTIBRATA GUHARAY'   TRANCSEND
'FLIGHT BOOKING'           SCREENSHOT            TRANSCEND
 HACKATHON                 SIGNATURE            'TRAVELS@JAYDEB BISWAS'
'HERO VIRED'               SKFGI                'VOTER LIST'
'INTERNET OF TECHNOLOGY'   SOFTWARE
suva@BWULPT931:/mnt/c/Windows/System32$ cd /mnt/d
suva@BWULPT931:/mnt/d$ cd AWS
-bash: cd: AWS: No such file or directory
suva@BWULPT931:/mnt/d$ cd TCS/AWS
suva@BWULPT931:/mnt/d/TCS/AWS$ # Clone your forked repo
git clone https://github.com/suvaatnbu/flask-app.git
cd flask-app

# Create and push staging branch
git checkout -b staging
git push -u origin staging
Cloning into 'flask-app'...
remote: Enumerating objects: 10, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 10 (delta 0), reused 4 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (10/10), done.
Switched to a new branch 'staging'
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'staging' on GitHub by visiting:
remote:      https://github.com/suvaatnbu/flask-app/pull/new/staging
remote:
To https://github.com/suvaatnbu/flask-app.git
 * [new branch]      staging -> staging
branch 'staging' set up to track 'origin/staging'.
suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ nano testapp.py
suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ git add .
git commit -m "Setup CI/CD pipeline"
git push origin main
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: empty ident name (for <suva@BWULPT931.>) not allowed
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
To https://github.com/suvaatnbu/flask-app.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/suvaatnbu/flask-app.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ git pull origin main --rebase
git push origin main
error: cannot pull with rebase: Your index contains uncommitted changes.
error: Please commit or stash them.
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
To https://github.com/suvaatnbu/flask-app.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/suvaatnbu/flask-app.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ git status
On branch staging
Your branch is up to date with 'origin/staging'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   testapp.py

suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ git add .
git commit -m "WIP: saving changes before pull"
git pull origin main --rebase
git push origin main
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: empty ident name (for <suva@BWULPT931.>) not allowed
error: cannot pull with rebase: Your index contains uncommitted changes.
error: Please commit or stash them.
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
remote: invalid credentials
fatal: Authentication failed for 'https://github.com/suvaatnbu/flask-app.git/'
suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ sudo cp /mnt/d/TCS/AWS/babu_suva.pem /home/suva/
sudo chown suva:suva /home/suva/babu_suva.pem
chmod 400 /home/suva/babu_suva.pem
[sudo] password for suva:suva
[sudo] password for suva:
[sudo]: command not found
suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ ssh -i /home/suva/babu_suva.pem ubuntu@13.203.102.78
Welcome to Ubuntu 24.04.2 LTS (GNU/Linux 6.8.0-1024-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Thu May 15 05:43:47 UTC 2025

  System load:  0.08              Processes:             117
  Usage of /:   43.6% of 6.71GB   Users logged in:       1
  Memory usage: 39%               IPv4 address for enX0: 172.31.10.209
  Swap usage:   0%

 * Ubuntu Pro delivers the most comprehensive open source security and
   compliance features.

   https://ubuntu.com/aws/pro

Expanded Security Maintenance for Applications is not enabled.

1 update can be applied immediately.
1 of these updates is a standard security update.
To see these additional updates run: apt list --upgradable

1 additional security update can be applied with ESM Apps.
Learn more about enabling ESM Apps service at https://ubuntu.com/esm


*** System restart required ***
Last login: Thu May 15 05:13:30 2025 from 13.233.177.4
ubuntu@ip-172-31-10-209:~$ git add .
git commit -m "WIP: saving changes before pull"
git pull origin main --rebase
git push origin main
fatal: not a git repository (or any of the parent directories): .git
fatal: not a git repository (or any of the parent directories): .git
fatal: not a git repository (or any of the parent directories): .git
fatal: not a git repository (or any of the parent directories): .git
ubuntu@ip-172-31-10-209:~$ git add
fatal: not a git repository (or any of the parent directories): .git
ubuntu@ip-172-31-10-209:~$ ls
flaskapp  venv
ubuntu@ip-172-31-10-209:~$ cd flask-app  # Replace `flask-app` with the actual folder name
-bash: cd: flask-app: No such file or directory
ubuntu@ip-172-31-10-209:~$ cd flaskapp  venv
-bash: cd: too many arguments
ubuntu@ip-172-31-10-209:~$ ls
flaskapp  venv
ubuntu@ip-172-31-10-209:~$ cd flask-app
-bash: cd: flask-app: No such file or directory
ubuntu@ip-172-31-10-209:~$ cd flaskapp
ubuntu@ip-172-31-10-209:~/flaskapp$ cd flaskapp
-bash: cd: flaskapp: No such file or directory
ubuntu@ip-172-31-10-209:~/flaskapp$ git status
fatal: not a git repository (or any of the parent directories): .git
ubuntu@ip-172-31-10-209:~/flaskapp$ git clone https://github.com/suvaatnbu/flask-app.git
Cloning into 'flask-app'...
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (13/13), done.
remote: Total 16 (delta 2), reused 4 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (16/16), 4.65 KiB | 1.16 MiB/s, done.
Resolving deltas: 100% (2/2), done.
ubuntu@ip-172-31-10-209:~/flaskapp$ cd flask-app
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git add
Nothing specified, nothing added.
hint: Maybe you wanted to say 'git add .'?
hint: Turn this message off by running
hint: "git config advice.addEmptyPathspec false"
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git add .
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git commit -m "your message"
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git pull origin main --rebase
From https://github.com/suvaatnbu/flask-app
 * branch            main       -> FETCH_HEAD
Already up to date.
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git pull origin main --rebase
From https://github.com/suvaatnbu/flask-app
 * branch            main       -> FETCH_HEAD
Already up to date.
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git push origin main
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
remote: invalid credentials
fatal: Authentication failed for 'https://github.com/suvaatnbu/flask-app.git/'
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git push origin main
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/suvaatnbu/flask-app.git/'
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git push origin main
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
Everything up-to-date
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ mkdir -p .github/workflows
touch .github/workflows/ci-cd.yml
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ Flask
pytest
Command 'Flask' not found, did you mean:
  command 'flask' from deb python3-flask (2.2.5-1ubuntu1)
Try: sudo apt install <deb name>
Command 'pytest' not found, but can be installed with:
sudo apt install python3-pytest
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ flask
pytest
Usage: flask [OPTIONS] COMMAND [ARGS]...

  A general utility script for Flask applications.

  An application to load must be given with the '--app' option, 'FLASK_APP'
  environment variable, or with a 'wsgi.py' or 'app.py' file in the current
  directory.

Options:
  -e, --env-file FILE   Load environment variables from this file. python-
                        dotenv must be installed.
  -A, --app IMPORT      The Flask application or factory function to load, in
                        the form 'module:name'. Module can be a dotted import
                        or file path. Name is not required if it is 'app',
                        'application', 'create_app', or 'make_app', and can be
                        'name(args)' to pass arguments.
  --debug / --no-debug  Set debug mode.
  --version             Show the Flask version.
  --help                Show this message and exit.

Commands:
  routes  Show the routes for the app.
  run     Run a development server.
  shell   Run a shell in the app context.
Command 'pytest' not found, but can be installed with:
sudo apt install python3-pytest
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ ^[[2~

Microsoft Windows [Version 10.0.26100.3775]
(c) Microsoft Corporation. All rights reserved.

C:\Windows\System32>wsl
Welcome to Ubuntu 24.04.2 LTS (GNU/Linux 5.15.167.4-microsoft-standard-WSL2 x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Thu May 15 05:15:24 UTC 2025

  System load:  0.4                 Processes:             57
  Usage of /:   0.3% of 1006.85GB   Users logged in:       0
  Memory usage: 6%                  IPv4 address for eth0: 172.24.99.238
  Swap usage:   0%


This message is shown once a day. To disable it please create the
/home/suva/.hushlogin file.
suva@BWULPT931:/mnt/c/Windows/System32$ ls /mnt/d
'$RECYCLE.BIN'             IVF                   SUVA
 BANK                      KYC                  'Staff Notice 2023_06_16_006 No Smoking inside the Campus.pdf'
 BRAINWARE                 PAYSLIP              'System Volume Information'
 CAST_HIGHERARCHY         'PHD NIT'              TCS
 CESC                      PHOTO                 TOYOTA
 COMPLAIN                  PIU                  'TRADING FX ROAD'
 EXPERIENCE_CV            'SAKTIBRATA GUHARAY'   TRANCSEND
'FLIGHT BOOKING'           SCREENSHOT            TRANSCEND
 HACKATHON                 SIGNATURE            'TRAVELS@JAYDEB BISWAS'
'HERO VIRED'               SKFGI                'VOTER LIST'
'INTERNET OF TECHNOLOGY'   SOFTWARE
suva@BWULPT931:/mnt/c/Windows/System32$ cd /mnt/d
suva@BWULPT931:/mnt/d$ cd AWS
-bash: cd: AWS: No such file or directory
suva@BWULPT931:/mnt/d$ cd TCS/AWS
suva@BWULPT931:/mnt/d/TCS/AWS$ # Clone your forked repo
git clone https://github.com/suvaatnbu/flask-app.git
cd flask-app

# Create and push staging branch
git checkout -b staging
git push -u origin staging
Cloning into 'flask-app'...
remote: Enumerating objects: 10, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 10 (delta 0), reused 4 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (10/10), done.
Switched to a new branch 'staging'
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'staging' on GitHub by visiting:
remote:      https://github.com/suvaatnbu/flask-app/pull/new/staging
remote:
To https://github.com/suvaatnbu/flask-app.git
 * [new branch]      staging -> staging
branch 'staging' set up to track 'origin/staging'.
suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ nano testapp.py
suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ git add .
git commit -m "Setup CI/CD pipeline"
git push origin main
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: empty ident name (for <suva@BWULPT931.>) not allowed
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
To https://github.com/suvaatnbu/flask-app.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/suvaatnbu/flask-app.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ git pull origin main --rebase
git push origin main
error: cannot pull with rebase: Your index contains uncommitted changes.
error: Please commit or stash them.
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
To https://github.com/suvaatnbu/flask-app.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/suvaatnbu/flask-app.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ git status
On branch staging
Your branch is up to date with 'origin/staging'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   testapp.py

suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ git add .
git commit -m "WIP: saving changes before pull"
git pull origin main --rebase
git push origin main
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: empty ident name (for <suva@BWULPT931.>) not allowed
error: cannot pull with rebase: Your index contains uncommitted changes.
error: Please commit or stash them.
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
remote: invalid credentials
fatal: Authentication failed for 'https://github.com/suvaatnbu/flask-app.git/'
suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ sudo cp /mnt/d/TCS/AWS/babu_suva.pem /home/suva/
sudo chown suva:suva /home/suva/babu_suva.pem
chmod 400 /home/suva/babu_suva.pem
[sudo] password for suva:suva
[sudo] password for suva:
[sudo]: command not found
suva@BWULPT931:/mnt/d/TCS/AWS/flask-app$ ssh -i /home/suva/babu_suva.pem ubuntu@13.203.102.78
Welcome to Ubuntu 24.04.2 LTS (GNU/Linux 6.8.0-1024-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Thu May 15 05:43:47 UTC 2025

  System load:  0.08              Processes:             117
  Usage of /:   43.6% of 6.71GB   Users logged in:       1
  Memory usage: 39%               IPv4 address for enX0: 172.31.10.209
  Swap usage:   0%

 * Ubuntu Pro delivers the most comprehensive open source security and
   compliance features.

   https://ubuntu.com/aws/pro

Expanded Security Maintenance for Applications is not enabled.

1 update can be applied immediately.
1 of these updates is a standard security update.
To see these additional updates run: apt list --upgradable

1 additional security update can be applied with ESM Apps.
Learn more about enabling ESM Apps service at https://ubuntu.com/esm


*** System restart required ***
Last login: Thu May 15 05:13:30 2025 from 13.233.177.4
ubuntu@ip-172-31-10-209:~$ git add .
git commit -m "WIP: saving changes before pull"
git pull origin main --rebase
git push origin main
fatal: not a git repository (or any of the parent directories): .git
fatal: not a git repository (or any of the parent directories): .git
fatal: not a git repository (or any of the parent directories): .git
fatal: not a git repository (or any of the parent directories): .git
ubuntu@ip-172-31-10-209:~$ git add
fatal: not a git repository (or any of the parent directories): .git
ubuntu@ip-172-31-10-209:~$ ls
flaskapp  venv
ubuntu@ip-172-31-10-209:~$ cd flask-app  # Replace `flask-app` with the actual folder name
-bash: cd: flask-app: No such file or directory
ubuntu@ip-172-31-10-209:~$ cd flaskapp  venv
-bash: cd: too many arguments
ubuntu@ip-172-31-10-209:~$ ls
flaskapp  venv
ubuntu@ip-172-31-10-209:~$ cd flask-app
-bash: cd: flask-app: No such file or directory
ubuntu@ip-172-31-10-209:~$ cd flaskapp
ubuntu@ip-172-31-10-209:~/flaskapp$ cd flaskapp
-bash: cd: flaskapp: No such file or directory
ubuntu@ip-172-31-10-209:~/flaskapp$ git status
fatal: not a git repository (or any of the parent directories): .git
ubuntu@ip-172-31-10-209:~/flaskapp$ git clone https://github.com/suvaatnbu/flask-app.git
Cloning into 'flask-app'...
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (13/13), done.
remote: Total 16 (delta 2), reused 4 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (16/16), 4.65 KiB | 1.16 MiB/s, done.
Resolving deltas: 100% (2/2), done.
ubuntu@ip-172-31-10-209:~/flaskapp$ cd flask-app
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git add
Nothing specified, nothing added.
hint: Maybe you wanted to say 'git add .'?
hint: Turn this message off by running
hint: "git config advice.addEmptyPathspec false"
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git add .
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git commit -m "your message"
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git pull origin main --rebase
From https://github.com/suvaatnbu/flask-app
 * branch            main       -> FETCH_HEAD
Already up to date.
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git pull origin main --rebase
From https://github.com/suvaatnbu/flask-app
 * branch            main       -> FETCH_HEAD
Already up to date.
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git push origin main
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
remote: invalid credentials
fatal: Authentication failed for 'https://github.com/suvaatnbu/flask-app.git/'
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git push origin main
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/suvaatnbu/flask-app.git/'
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ git push origin main
Username for 'https://github.com': suvaatnbu
Password for 'https://suvaatnbu@github.com':
Everything up-to-date
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ mkdir -p .github/workflows
touch .github/workflows/ci-cd.yml
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ Flask
pytest
Command 'Flask' not found, did you mean:
  command 'flask' from deb python3-flask (2.2.5-1ubuntu1)
Try: sudo apt install <deb name>
Command 'pytest' not found, but can be installed with:
sudo apt install python3-pytest
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$ flask
pytest
Usage: flask [OPTIONS] COMMAND [ARGS]...

  A general utility script for Flask applications.

  An application to load must be given with the '--app' option, 'FLASK_APP'
  environment variable, or with a 'wsgi.py' or 'app.py' file in the current
  directory.

Options:
  -e, --env-file FILE   Load environment variables from this file. python-
                        dotenv must be installed.
  -A, --app IMPORT      The Flask application or factory function to load, in
                        the form 'module:name'. Module can be a dotted import
                        or file path. Name is not required if it is 'app',
                        'application', 'create_app', or 'make_app', and can be
                        'name(args)' to pass arguments.
  --debug / --no-debug  Set debug mode.
  --version             Show the Flask version.
  --help                Show this message and exit.

Commands:
  routes  Show the routes for the app.
  run     Run a development server.
  shell   Run a shell in the app context.
Command 'pytest' not found, but can be installed with:
sudo apt install python3-pytest
ubuntu@ip-172-31-10-209:~/flaskapp/flask-app$
