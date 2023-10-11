# Terminal, Rails and Git commands

---

## Terminal Commands

| Command | Variations       | What it means                | What it does                                                                                          |
| ------- | ---------------- | ---------------------------- | ----------------------------------------------------------------------------------------------------- |
| `pwd`   |                  | Present Working Directory    | Shows the path of your current directory (where you are in the folder structure)                      |
| `ls`    |                  | LiSt                         | Lists visible files and directories in current directory                                              |
|         | `ls -al`         | List All as vertical List    | Lists all files (including invisible “.” files) in a vertical list with access information, file size |
| `cd`    |                  | Change Directory             |                                                                                                       |
|         | `cd ..`          | Change Directory up a level  | Takes your terminal to the parent folder                                                              |
|         | `cd some_dir`    | Change to specific directory | Takes your terminal to the named folder within current directory                                      |
|         | `cd ~`           | Change to home directory     | Takes your terminal to your home directory                                                            |
|         | `cd /root`       | Change to root directory     | Takes your terminal to the root directory                                                             |
|         | `cd ../some_dir` | Change to sibling directory  | Takes your terminal up a level and into other directory                                               |
| `whoami`  |                  | Which user am I now          | Prints name of current user                                                                           |
|         |                  |                              |                                                                                                       |

## Rails Commands 

| Command    | Variations                                            | What it means                                                                | What it does                                                                                                                                                                  |
| ---------- | ----------------------------------------------------- | ---------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `rvm`      |                                                       | Ruby Version Manager                                                         | Manages the versions of Ruby installed [RVM: Ruby Version Manager](https://rvm.io/)                                                                                           |
|            | `rvm list known`                                      | Lists versions of known Ruby                                                 | Prints lists of Ruby packages available since last update (`q` to exit)                                                                                                       |
|            | `rvm get head`                                        | Get newest head of RVM                                                       | Updates RVM                                                                                                                                                                   |
|            | `rvm list`                                            | List Ruby versions installed                                                 |                                                                                                                                                                               |
|            | `rvm list gemsets`                                    | List names of created gemsets                                                | Lists created gemsets with arrow pointing to current gemset in use                                                                                                            |
|            | `rvm use ruby-3.2.2@gemset --create`                  | Create the name gemset                                                       | Creates a gemset named `ruby-3.2.2@rails` (Ruby version named must be installed)                                                                                              |
|            | `rvm use ruby-3.2.2@gemset`                           | Use the named gemset                                                         |                                                                                                                                                                               |
|            | `echo ruby-3.2.2@gemset > .ruby-gemset`               | Create .ruby-gemset file in project                                          | Creates a config file so the terminal knows which gemset to use for this project [RVM: Ruby Version Manager - Typical RVM Project Workflow](https://rvm.io/workflow/projects) |
| `ruby -v`  |                                                       | Ruby version                                                                 | Prints version of ruby in use [Ruby Programming Language](https://www.ruby-lang.org/en/)                                                                                      |
| `rails -v` |                                                       | Ruby on Rails version                                                        | Prints version of Rails in use [Ruby on Rails Guides](https://guides.rubyonrails.org/)                                                                                        |
|            | `rails new new_app`                                   | Create new Rails app called new_app                                          | Creates a new Rails app in a directory called new_app                                                                                                                         |
|            | `rails s`                                             | Start Rails server                                                           | (`rails s` == `rails server`)                                                                                                                                                 |
|            | `rails g controller controller_name action_name`      | Generate controller and view for named controller and action                 | (`rails g` == `rails generate`) Creates a named controller file with the named actions methods plus corresponding views plus route                                            |
|            | `rails g model ModelName attribute_name:data_type`    | Generate a ModelName model (object) with named attributes of named datatypes | Creates a named model file, and a migration file to generate the database table as defined`                                                                                   |
|            | `rails g scaffold ModelName attribute_name:data_type` | Generate the full stack of files needed for CRUD                             | Creates model_name.rb (model file), model_names.rb (controller file), views/model_names (views directory plus view files), routes resource, migration file                    |
|            | `rails db:create`                                     | Create database                                                              | Creates database according to `config/database.yml`                                                                                                                           |
|            | `rails db:migrate`                                    | Run database migration                                                       | Runs **all** migration files that have not already been run                                                                                                                   |
|            | `rails db:rollback`                                   | Rollback database migration                                                  | Rolls back the most recent migration                                                                                                                                          |
|            | `rails c`                                             | Open Rails console                                                           | (`rails c` == `rails console`) Ruby code to access project                                                                                                                    |
|            |                                                       |                                                                              |                                                                                                                                                                               |
|            |                                                       |                                                                              |                                                                                                                                                                               |
## Git commands 

| Command                          | Variations                      | Meaning                                 | Description                                                               |
| -------------------------------- | ------------------------------- | --------------------------------------- | ------------------------------------------------------------------------- |
| `git init`                       |                                 | Initiate git repository                 | Generates a git repo in current directory                                 |
| `git status`                     |                                 | Status git repo                         | Prints out current branch and uncommitted changes                         |
| `git add --all`                  |                                 | Adds all unstaged and untracked changes | Prepares all new and modified files to be committed                       |
| `git commit -m 'commit message'` |                                 | Create a commit with required message   | Creates a 'commit' (can rollback here easily) - message must be given     |
| `git push origin main`           |                                 | Push main to origin                     | Push latest commit in the branch named *main* to remote named *origin* (usually Github)                                                                          |
| `git remote -v`                  |                                 | Show git remote locations               | Prints list of any remote repos                                           |
|                                  | `git remote remove remote_name` | Remove the named remote connection      | Removes the connection to a remote repo - does not delete the remote repo |
|                                  |                                 |                                         |                                                                           |


