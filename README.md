# CityConnect

This project is undertaken as part of the TQS course, with the goal of developing a MVP product while applying software enterprise architecture patterns, specifying and enforcing a Software Quality Assurance (SQA) strategy and applying Continuous Testing, Continuous Integration and Continuous Delivery practices. The chosen theme was a bus service, like the ones you found in common transportation terminals. This is a digital service which includes a customer portal, tools for staff to edit bus and trips information and a digital signage system.

Our project aligns with these goals by focusing on the development of a user-centered online system for a public bus service, with the advantage of unifying these digital services into one.

## Keep repo and submodules up-to-date
Do these commands every time you start working:
```bash
git pull
git submodule foreach git pull
```

If everything works right, all submodules will hopefully be updated.

There is no need to commit submodule changes to this repo, since GitHub Actions does it by itself.

### Full fetch & pull
In the case where a full pull is needed, do the following:

```bash
git pull --recurse-submodules
git submodule foreach git checkout main
```

**WARNING: All local changes will be discarded!**

## Git tips
### Check current branch
Run this code to get the current branch of all submodules:

```bash
git submodule foreach git rev-parse --abbrev-ref HEAD
```

### Cherry-picking commits
If you need to cherry-pick commits from another branch or repo, do the following:

```bash
# Add other repo, if applicable
git remote add cherry git@github.com:CityConnect-TQS/client-portal.git
git fetch cherry

# Cherry-pick one commit
git cherry-pick commit_hash

# Cherry-pick several commits
git cherry-pick <commit_hash1>^..<commit_hash2>

# Remove other repo, if applicable
git remote remove cherry
```

## Project Bookmarks

- [Project Backlog](https://cityconnect-tqs.atlassian.net/jira/software/projects/CC/boards/1/backlog)
- [API Documentation](http://api.localhost/api/docs/swagger-ui/index.html)
- [Static Analysis](https://sonarcloud.io/project/overview?id=CityConnect-TQS_backend)

- CI/CD enviroment: Check the [backend](https://github.com/CityConnect-TQS/backend) submodule on how CI/CD is used for testing and Sonar analysis

## Project Team

| Member                  | Role             |
|-------------------------|------------------|
| Bárbara Galiza (105937) | Product owner    |
| Diana Miranda (107457)  | QA Engineer      |
| Diogo Falcão (108712)   | Team Coordinator |
| Rúben Garrido (107927)  | DevOps master    |
