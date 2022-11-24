# graphite-test

npm install -g @withgraphite/graphite-cli

to init a repo for tracking with graphite
gt repo init

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
