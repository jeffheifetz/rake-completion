# Rake Completion

Bash completion support for Rake, Ruby Make.

     $ rake st<Tab>
     $ rake stats

     $ rake test<Tab><Tab>
     test              test:integration  test:recent       
     test:benchmark    test:plugins      test:uncommitted  
     test:functionals  test:profile      test:units

It cache tasks to `.rake_tasks~` and update it if it will be outdated.
So it’s more faster, that default completion from Ubuntu rake.

## Install

### Ubuntu

1. Add Ubuntu on Rails PPA:
   
        $ sudo add-apt-repository ppa:ubuntu-on-rails/ppa
   
2. Install `rake-completion` package:
   
        $ sudo apt-get install rake-completion

### Other UNIX-like

#### System
Copy `rake` script to `/etc/bash_completion.d/`.

#### User
Copy `rake` script (for example, to `~/scripts/`) and add to your `.bashrc`:

    . ~/scripts/rake

## Cache

Tasks cache in `.rake_tasks~` will be update on changes in Rakefile or any
`*.rake` files.

To remove tasks cache (and another backup files) from Git repository add to
`.gitignore`: `*~`.
