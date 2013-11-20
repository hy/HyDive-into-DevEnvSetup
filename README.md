HyDive-DevEnv
=============

Shortest easy path to diving into development on OS X 10.8.5

# Sync Dropbox



# In Terminal . . .  
defaults write com.apple.Finder AppleShowAllFiles YES

# . . . Then hold alt and right-click Finder icon, select: "Relaunch"



# Download and install the Heroku Toolbelt and then . . .  
git config --global user.name "DrStephenRacunas"
git config --global user.email Stephen.A.Racunas@gmail.com



# Downloaded Mongo . . .  
curl http://downloads.mongodb.org/osx/mongodb-osx-x86_64-2.4.6.tgz > mongodb.tgz



# From https://github.com/sstephenson/rbenv . . .  
git clone https://github.com/sstephenson/rbenv.git ~/.rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
echo 'eval "$(rbenv init -)"' >> ~/.bash_profile

# alias b=‘bundle exec’ (optional)



# Get the Mountain Lion developer tools (for gcc-without-Xcode) . . .  
# http://osxdaily.com/2012/07/06/install-gcc-without-xcode-in-mac-os-x/

https://developer.apple.com/downloads/index.action#



git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build

rbenv install -list
rbenv install 2.0.0-p247
rbenv rehash

# rehash after each new ruby version or global gem!



# Optionally add this line to the ~/.gemrc file to prevent rdoc spam:
gem: --no-rdoc --no-ri



rbenv shell 2.0.0-p247 
gem install bundler
rbenv rehash


# Optionally, make rbenv bundler-aware (saves typing bundle exec, etc.) . . .  
git clone git://github.com/carsomyr/rbenv-bundler.git ~/.rbenv/plugins/bundler


# Get wget from: http://ftp.gnu.org/gnu/wget/
gunzip < wget-1.14.tar.gz | tar -xv
cd wget-1.14
./configure --with-ssl=openssl
make
sudo make install
which wget

[see:http://thomashunter.name/blog/install-wget-on-os-x-lion/]







# Helpful Sources . . .  
http://dan.carley.co/blog/2012/02/07/rbenv-and-bundler/



