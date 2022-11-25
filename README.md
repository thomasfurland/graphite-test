# graphite-test

npm install -g @withgraphite/graphite-cli

to init a repo for tracking with graphite
gt repo init

mega conflict withgraphite
and with all the code
right here I think

## Create a branch with a commit and opens up a draft pr

function gb
  if test (count $argv) -lt 2
    echo "Must be in format: gb BRANCHNAME THIS IS THE TITLE"
  else
    gt branch create "$argv[1]" -a -m "$argv[2..-1]" --no-interactive && \
    gt branch submit --no-interactive
  end
end

## Moving up and down the stack

use gt branch up 
can use gt branch up 2 to move up 2

use gt branch down
can also use with numbers to move multiple branches

these commands only work if the code is uncommited. Don't commit any code. Run this only at the beginning

## Make changes to the exisiting commit

function app
  git add . && git commit --amend --no-edit && git push --force-with-lease $argv; 
end

Use this rather than creating a new commit. This is to keep graphite from breaking.

## checking logs for graphite

use gt log to check your stacks for a project

## Merging Branches

function gs
  gt repo sync --force && \
  gt stack restack && \
  gt stack submit --no-interactive $argv; 
end


