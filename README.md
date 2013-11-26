HyDive-DevEnv
=============

Shortest easy path to diving into development on OS X 10.8.5

# Sync Dropbox




# In Terminal . . .  
defaults write com.apple.Finder AppleShowAllFiles YES
# . . . Then hold alt and right-click Finder icon, select: "Relaunch"




# Get the Mountain Lion developer tools (for gcc-without-Xcode) . . .  
# http://osxdaily.com/2012/07/06/install-gcc-without-xcode-in-mac-os-x/
https://developer.apple.com/downloads/index.action#




# Get wget from: http://ftp.gnu.org/gnu/wget/
gunzip < wget-1.14.tar.gz | tar -xv
cd wget-1.14
./configure --with-ssl=openssl
make
sudo make install
which wget

[see:http://thomashunter.name/blog/install-wget-on-os-x-lion/]




# Optionally add this line to the ~/.gemrc file to prevent rdoc spam:
gem: --no-rdoc --no-ri




# Download and install the Heroku Toolbelt and then . . .  
git config --global user.name "DrStephenRacunas"
git config --global user.email Stephen.A.Racunas@gmail.com




# Download Mongo . . .  
curl -O http://downloads.mongodb.org/osx/mongodb-osx-x86_64-2.4.8.tgz
tar -zxvf mongodb-osx-x86_64-2.4.8.tgz




# From https://github.com/sstephenson/rbenv . . .  
git clone https://github.com/sstephenson/rbenv.git ~/.rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
# in .bash_profile, alias b=‘bundle exec’ (optional)

git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build
rbenv install -list
rbenv install 2.0.0-p247
rbenv rehash
# rehash after each new ruby version or global gem!

rbenv shell 2.0.0-p247 
gem install bundler
rbenv rehash

# Optionally, make rbenv bundler-aware (saves typing bundle exec, etc.) . . .  
git clone git://github.com/carsomyr/rbenv-bundler.git ~/.rbenv/plugins/bundler




# chruby and ruby-install are perhaps a better choice . . . 
[see: https://github.com/postmodern/chruby]

wget -O ruby-install-0.3.2.tar.gz https://github.com/postmodern/ruby-install/archive/v0.3.2.tar.gz
tar -xzvf ruby-install-0.3.2.tar.gz
cd ruby-install-0.3.2/
sudo make install

wget -O chruby-0.3.7.tar.gz https://github.com/postmodern/chruby/archive/v0.3.7.tar.gz
tar -xzvf chruby-0.3.7.tar.gz
cd chruby-0.3.7/
sudo make install

# Edit .bashrc . . .  
# (bashrc is only used by chruby so far) . . .

# baseline: need this for chruby to function:
source /usr/local/share/chruby/chruby.sh

# let chruby auto-swap vers to .ruby_version in current dir or parent
source /usr/local/share/chruby/auto.sh

# tell chruby where to find the rbenv-installed rubies . . .
RUBIES=(
        ~/.rbenv/versions/*
        /opt/rubies/*
)

sudo ruby-install -i /opt/rubies/2.0.0-p353 ruby 2.0.0-p353

# Comment out the lines in .bash_profile dealing with rbenv

chruby





# Helpful Sources . . .  
http://dan.carley.co/blog/2012/02/07/rbenv-and-bundler/



