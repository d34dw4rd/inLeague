# inLeague

#TODO
1. Design Requirements
2. Tools Selection
3. Development Ways of Working

#Continuous Integration Ways of Working

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
    a. Go to My / Changes to see coM#de reivew
    b .Add code reviewers

#On SSH Keys

Gerrithub requires sshkey access inorder to push commandline for a code review. In order to set this up please do the following.
1. ssh-kegen -t rsa
2. cat /.ssh/id_rsa.pub
    a. copy the entire key
    b. it should look something like this:
    ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAx7HLtm09Ihf25vxBjCR66o4ESgwHQS54BIU0kR1JvpOZ15dR6gG8IZcjfliNJLcA4qvYerCLxQCL3C37N2LnqrMe+icy+gyOMu2k9lk0ykedLaUZWMuGFgkW07DyjjUFWOueWAcjVPCtAKDXwts4dp/fTdwlmDMpJ/hBjUWMHeBQ8bvFxPmFoYGxPwBZjHlOWAgxPWJ2j4lW2QNukQQgwiHepac8pckePE8Lv+UutcOkcF/PvOZL2ZhpOnUPZiAveOYl9c/2YUyUSUsa0tbvnKtO2CCfEDvMQ0+TBEwVPysXWhTO/c9pIpngHa3rTO83sbZXwkt+L8lsYvmuabUANQ== eedwalo@eussjlx7047.sj.us.am.ericsson.se
    c. paste it into gerrithub -> settings -> ssh public keys -> add key
3. test your access 
    a. "ssh -p 29481 <username>@https://review.gerrithub.io"


#NOTE: When pushing to a code review, make sure to use your http password which is generated in gerrithub. GOTO: Settings -> HTTP Password -> Generate Password -> Copy and Paste Password when pushing


