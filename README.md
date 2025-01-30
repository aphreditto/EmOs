# EmOs

## compile python and create virtual environment with it

`sudo apt-get update`

`sudo apt-get install build-essential gdb lcov libbz2-dev libffi-dev libgdbm-dev liblzma-dev liblzma-dev libncurses5-dev libreadline6-dev libsqlite3-dev libssl-dev lzma-dev tk-dev uuid-dev zlib1g-dev`

# download latest non-beta python release https://www.python.org/downloads/
`wget https://www.python.org/ftp/python/3.13.1/Python-3.13.1.tgz`

# uncompress file
`tar zxvf Python-3.13.1.tgz`

# delete the tar file
`rm Python-3.13.1.tgz`

# config
`cd Python-3.13.1/`

`./configure --enable-optimizations`

# fully saturate all cores
`htop`

`make -j 4`

# final step, put python executable into a useable place
`sudo make altinstall`

# use our Python-3.13
`cd ..`

`/usr/local/bin/python3.13`

# make Python-3.13 the default
`vim ~/.bashrc`

`#new python\nalias python="/usr/local/bin/python3.13"`

`source ~/.bashrc`

`python`

# create python virtual environment
`python -m venv ~/.venv`

`vim ~/.bashrc`

`#source venv\nsource ~/.venv/bin/activate`

`source ~/.bashrc`

# set up template for python project
`touch requirements.txt`

# create make file
`touch MakeFile`

# commit

`rm -rf Python-3.13`

`git status`

`git add README.md`

`git add *`

`git commit -m "adding skeleton"`

`git push`
