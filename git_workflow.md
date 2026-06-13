GIT WORKFLOW

1. Get latest code

git checkout develop
git pull origin develop

2. Create feature branch

git checkout -b feature/JIRA-101-login

3. Work on code

git add .
git commit -m "JIRA-101 Add login validation"

4. Push branch
First Push
After creating the feature branch and making your changes:
git push -u origin feature/JIRA-101-login
This creates the branch on GitHub so others can see it and you can create a PR later.

5. Sync with latest develop before PR
Second Push
Later, before creating the PR, you sync with the latest develop:

git checkout develop
git pull origin develop

git checkout feature/JIRA-101-login
git merge develop
This creates a new merge commit (or updates your branch).

If nobody changed develop
Then you don't need the second push.

6. Push updated branch

git push origin feature/JIRA-101-login

7. Create Pull Request

feature/JIRA-101-login -> develop

8. After merge, delete feature branch

git branch -d feature/JIRA-101-login
git push origin --delete feature/JIRA-101-login