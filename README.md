# Version and Changelog your projects automatically to GitHub using Release It

````
npm init

npm install release-it @release-it/conventional-changelog @commitlint/config-conventional @commitlint/cli --include=dev

````
### or create a new repository on the command line
````
echo "# Automate-Version-Changelog-GitHub-Release-It" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/hamza-webdev/Automate-Version-Changelog-GitHub-Release-It.git
git push -u origin main
````

### …or push an existing repository from the command line
````
git remote add origin https://github.com/hamza-webdev/Automate-Version-Changelog-GitHub-Release-It.git
git branch -M main
git push -u origin main
````
