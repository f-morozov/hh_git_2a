git clone https://github.com/hhru/frontik hh_git_2a

cd hh_git_2a

git subtree split -P frontik/testing/ -b testing

cd ..

mkdir hh_git_2b

git init

cd hh_git_2b

git init

git pull ../hh_git_2a/ testing

cd ../hh_git_2a

git filter-branch --prune-empty --tree-filter 'rm -rf frontik/testing' HEAD
