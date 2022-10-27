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

## Add in package json file
````
"release-it":{
    "git": {
        ""commitMessage": "chore: release v${version}"
    },
    "github": {
        "release": true
    },
    "npm":{
        "publish": false
    },
    "plugins":{
        "@release-it/conventional-changelog": {
            "infile": "CHANGELOG.md",
            "preset": {
                "name": "conventionalcommits",
                "types": [
                    {
                        "type": "feat",
                        "section": "Features"
                    },
                    {
                        "type": "fix",
                        "section": "Bug Fixes"

                    }
                ]
            }
        }
    }
}

````
### Install husky on dev

````
npm install husky --include=dev

./node_modules/husky/lib/bin.js install

touch .husky/commit-msg && chmod a+x .husky/commit-msg

 git commit -a

 npm run release

````

$ npm i @commitlint/cli @commitlint/config-conventional

# from original comment
$ echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js

# sample commit message from original comment
$ echo 'refactor: remove old files, add dev files' | npx commitlint -V
⧗   input: refactor: remove old files, add dev files
✔   found 0 problems, 0 warnings

$ npx commitlint --version
@commitlint/cli@16.0.2
