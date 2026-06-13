| Term          | Meaning                   |
| ------------- | ------------------------- |
| `HEAD`        | Your current local branch |
| `origin`      | Remote GitHub repository  |
| `origin/main` | Main branch on GitHub     |
| `origin/HEAD` | Default branch on GitHub  |

Local Repository
----------------
HEAD
  |
  v
main

Remote Repository (GitHub)
--------------------------
origin/HEAD
     |
     v
origin/main

Switch to SSH:
git remote set-url origin git@github.com:bhanuonline/test.git

added name/email:
git config --global user.name "Bhanu Pratap"
git config --global user.email "your-github-email@example.com"

See the commit that hasn't been pushed:
git log --oneline origin/main..HEAD

Cleanup ACtivity:
Since the feature branch has already been merged, you can delete it:
git branch -d feature/daily-workflow
git push origin --delete feature/daily-workflow
