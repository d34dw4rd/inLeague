# inLeague

#TODO
1. Design Requirements
2. Tools Selection
3. Development Ways of Working

Continuous Integration Ways of Working

1. Clone Repository
    git clone https://review.gerrithub.io/d34dw4rd/inLeague && (cd inLeague && curl -kLo `git rev-parse --git-dir`/hooks/commit-msg https://review.gerrithub.io/tools/hooks/commit-msg; chmod +x `git rev-parse --git-dir`/hooks/commit-msg)

2. Make changes

3. Add changes to be Tracked
    git status
    git add

4. Commit changes
    git commit

    a. If you want to commit new patch set to same code review do
    git commit --amend (instead)

5. Push Changes
    git push origin HEAD:refs/for/master

6. Login to GerritHub 
    Website URL: https://review.gerrithub.io
    a. Go to My / Changes to see code reivew
    b .Add code reviewers


