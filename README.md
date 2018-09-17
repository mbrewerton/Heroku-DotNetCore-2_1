# .Net Core 2.1.1 Basic MVC
This repo provides a .NET Core 2.1.1 basic MVC/Bootstrap project ready for deployment to Heroku. Once pulled the repo, make sure it builds and runs locally, then to get it running on Heroku you need to:

**Note:** this is using the Heroku CLI. If you are **totally** unaware of how to use the Heroku CLI, I recommend spending 10 minutes here: [https://devcenter.heroku.com/categories/command-line]()

#### Create the App
1. Open a command prompt in the project directory (eg: `C:\Projects\Heroku-DotNetcore-2_1`)
2. Create the Heroku App: `heroku apps:create my-dotnet-core`
3. Add the .NET Core Buildpack for this version (2.1.300): `heroku buildpacks:add https://github.com/jincod/dotnetcore-buildpack#v2.1.300`

#### Setup the Remote
1. Add the remote to the git repo: `git remote add heroku https://git.heroku.com/<your-app-name>.git`
2. Stage the files in git: `git add .`
3. Commit all files: `git commmit -m "Commit for Deployment"`.

    **Note:** If you get the error `fatal: The current branch master has no upstream branch.` then run the command `git push --set-upstream origin master`
4. Push to the Heroku remote: `git push heroku`.

    **Note:** that if you're not on a master branch locally, you'll need to run the command like: `git push heroku local-branch:master` to deploy