# ton-connect-auto-sync

## start
```
cd src && node app.js
```

## process description

1. get the latest npm version to compare

2. if inconsistent, select the latest tag with version number to compare and get the patch file
  a. get all tags
  b. select the tags to compare
  c. get the patch file

3. parse patch and compare tonconnect react update content

4. if only package.json version and tonconnect ui version have changed

5. pull our package file and update these fields
  a. pull the latest code
  b. update package.json

6. create a new branch and commit the changes

7. merge the branch into main

8. trigger github action to automatically update log and publish to npm

9. after successful merge, remove the created branch

10. if the patch contains more than just version updates, create an issue to be notified
  a. if the patch contains other significant changes, create an issue on github to be notified about the updates

11. if any request fails after step 3, create an issue, making sure there is only one issue per problem