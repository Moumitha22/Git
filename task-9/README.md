# Task 9 **Working with Remote Repositories and Collaboration**
    
## **Objective:**
- Simulate a collaborative workflow with remote repositories.

## **Requirements:**
- Create a local repository and push it to a remote service (e.g., GitHub or GitLab).
- Create a feature branch, make commits, and push the branch to the remote.
- Open a Pull Request (or Merge Request) and perform a code review process.
- Merge the feature branch into the main branch on the remote and then pull the changes locally.

## **Steps:**

#### **1. Initialize a Local Git Repository:**
- Initialize the local project folder as a Git repository. 
- This sets up Git to start version control.

```sh
git init
```

![init](./init.png)

#### **2. Link Remote Repository (GitHub):**
- Connect the local repository to a GitHub remote repository.

```sh
git remote add origin https://github.com/your-name/your-repo-name.git
```
![add-remote](./add-remote.png)

- Verify the connection to the remote:

```sh
git remote -v
```
![remote-version](./remote-v.png)

#### **3. Rename Default Branch:**
- Rename the default branch from master to main (as followed by modern Git standards).

```sh
git branch -M main
```

![rename-branch-to-main](./branch-main.png)

#### **4. Create and Commit the First File:**
- Create an index.html file to represent the homepage.

```sh
touch file_name
```
![create-index-page](./create-index.png)

- Add content to the file.
![index-page](./index-page.png)

- Stage and commit the file to Git.

```sh
git add file_name
git commit -m "Commit message"
```

![commit](./commit.png)

#### **5. Push main Branch to GitHub:**
Push the local main branch to the remote GitHub repository.

```sh
git push -u origin main
```

![push](./push.png)

#### **6. Create a New Feature Branch:**
- Create and switch to a new branch for the about page feature.

```sh
git checkout -b feature-about-page
```
![about-branch](./feature-branch.png)

#### **7. Add and Commit New Feature File:**
- Create an about.html file and commit it to the feature branch.

```sh
touch file_name
git add file_name
git commit -m "Commit message"
```

![commit-about](./commit-about.png)

#### **8. Push Feature Branch to Remote:**
- Push the feature branch to the remote GitHub repository.

```sh
git push -u origin feature-about-page
```

![push-feature-branch](./push-feature-branch.png)

#### **9. Create Pull Request on GitHub:**
- Go to GitHub, click Compare & Pull Request

![pull-request](./pull-request.png)

- Add a title and description, then click Create Pull Request.

![title&desc](./title&desc.png)


#### **10. Merge Pull Request:**
- Click "Merge Pull Request" to merge the feature-about-page branch into the main branch.

![merge-pr](./merge-pr.png)

- Confirm the merge operation on GitHub by clicking "Confirm Merge".

![confirm-merge](./confirm-merge.png)

- GitHub shows a success message after the merge is completed.

![merge-success](./merge-success.png)

- The main branch now includes the merged changes from feature-about-page.

![after-merge](./after-merge.png)

#### **11. Pull Changes to Local Main:**
- Switch to  your local main branch and pull the latest changes from GitHub.

```sh
git checkout main
git pull origin main
```

![pull-in-local](./pull-in-local.png)