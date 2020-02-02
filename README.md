# Git training guide:

## What you need to do ONE TIME:
- **Fork this repo**: so that you will have a "thing" to push code to and pull request to me or compare code in different branches.
- **Pull YOUR forked repo to your machine**: to have a local repo.
- In your local repo, check if you have 2 branches: **master and dev** by using ```git checkout dev``` then ```git branch```. Then create another branch to work in (dev_yourname).
- Create **upstream** remote so that you can fetch new code **FROM OUR REPO**:
```sh
$ git remote add upstream https://github.com/phuongminh2303/Git_training.git
```

## What you need to do WHEN YOU WANT TO GET THE LASTEST CODE:
- If you're working with some code, you need to "stash" or "commit" that code, I prefer "stash"
```sh
$ git stash # save your code that you're working to a bucket.
```
- Fetch the latest code from our repo:
```sh
$ git checkout dev  # I am not sure if we need this :))
$ git fetch upstream # Now, the latest code is in your local machine but you need to merge it into dev branch
$ git merge upstream/dev
```
- Then move to branch dev_yourname and merge the code using ```git merge dev```.
- Now, put your code that you saved in step 1 out of the bucket:
```sh
$ git stash
```
- Sometimes you will have a conflict, simply resolve the conflict using the technique that I've teached you!

## What you need to do AFTER YOU ADDED NEW THINGS:
- Commit your code in your dev_name branch.
- Checkout to dev branch and merge dev_name to it (using ```git checkout dev``` and ``git merge dev_yourname```).
- Push ```dev``` to your forked repo on Github.
- Make a pull request in Github page (REMEMBER TO CHECK THE BRANCHES IS CORRECT OR NOT), tell me to review.
