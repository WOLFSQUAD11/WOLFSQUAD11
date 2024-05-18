SERVER _HACKR, [5/17/2024 11:09 PM]
miray_xala_bakr

SERVER _HACKR, [5/17/2024 11:09 PM]
gchvvi@hi2.in

SERVER _HACKR, [5/18/2024 2:17 AM]
termux-change-repo

SERVER _HACKR, [5/18/2024 2:17 AM]
pkg update
pkg upgrade -y

SERVER _HACKR, [5/18/2024 2:17 AM]
pkg install -y \
  build-essential \
  binutils \
  pkg-config \
  python3 \
  nodejs-lts
npm config set python python3
node -v

SERVER _HACKR, [5/18/2024 2:17 AM]
installing with npm

SERVER _HACKR, [5/18/2024 2:17 AM]
code-server --auth none

SERVER _HACKR, [5/18/2024 2:17 AM]
npm update --global code-server

SERVER _HACKR, [5/18/2024 2:18 AM]
rm -rf ~/.local/lib/code-server-*

SERVER _HACKR, [5/18/2024 2:18 AM]
curl -fsSL https://code-server.dev/install.sh | sh

SERVER _HACKR, [5/18/2024 2:18 AM]
Using git in the /sdcard directory will fail during cloning/commit/staging/etc...

SERVER _HACKR, [5/18/2024 2:18 AM]
None

SERVER _HACKR, [5/18/2024 2:18 AM]
/sdcard

SERVER _HACKR, [5/18/2024 2:19 AM]
(preferred)

SERVER _HACKR, [5/18/2024 2:19 AM]
// android-as-linux.js
Object.defineProperty(process, "platform", {
  get() {
    return "linux"
  },
})

SERVER _HACKR, [5/18/2024 2:19 AM]
NODE_OPTIONS="--require /path/to/android-as-linux.js" code-server

SERVER _HACKR, [5/18/2024 2:19 AM]
{
  "keyboard.dispatch": "keyCode"
}

SERVER _HACKR, [5/18/2024 2:19 AM]
From https://golang.org/doc/installFrom https://golang.org/doc/install

SERVER _HACKR, [5/18/2024 2:20 AM]
wget download_link

SERVER _HACKR, [5/18/2024 2:20 AM]
rm -rf /usr/local/go && tar -C /usr/local -xzf archive_name

SERVER _HACKR, [5/18/2024 2:20 AM]
Run these commands as root

SERVER _HACKR, [5/18/2024 2:20 AM]
sudo apt-get update
sudo apt-get install make build-essential libssl-dev zlib1g-dev \
  libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
  libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
sudo apt-get update
sudo apt-get install make build-essential libssl-dev zlib1g-dev \
  libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
  libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev

SERVER _HACKR, [5/18/2024 2:20 AM]
curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash

SERVER _HACKR, [5/18/2024 2:20 AM]
export PYENV_ROOT="/root/.pyenv"
export PATH="/root/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv virtualenv-init -)"

SERVER _HACKR, [5/18/2024 2:21 AM]
Android
✅✅✅✅✅✅

SERVER _HACKR, [5/18/2024 2:21 AM]
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash

SERVER _HACKR, [5/18/2024 2:21 AM]
nvm install 18
nvm use 18

SERVER _HACKR, [5/18/2024 2:22 AM]
curl -fsSL https://code-server.dev/install.sh | sh -s -- --dry-run

SERVER _HACKR, [5/18/2024 2:22 AM]
curl -fsSL https://code-server.dev/install.sh | sh

SERVER _HACKR, [5/18/2024 2:22 AM]
mkdir -p ~/.local/lib ~/.local/bin
curl -fL https://github.com/coder/code-server/releases/download/v$VERSION/code-server-$VERSION-linux-amd64.tar.gz \
  | tar -C ~/.local/lib -xz
mv ~/.local/lib/code-server-$VERSION-linux-amd64 ~/.local/lib/code-server-$VERSION
ln -s ~/.local/lib/code-server-$VERSION/bin/code-server ~/.local/bin/code-server
PATH="~/.local/bin:$PATH"
code-server
# Now visit http://127.0.0.1:8080. Your password is in ~/.config/code-server/config.yaml

SERVER _HACKR, [5/18/2024 2:22 AM]
curl -fOL https://github.com/coder/code-server/releases/download/v$VERSION/code-server_${VERSION}_amd64.deb
sudo dpkg -i code-server_${VERSION}_amd64.deb
sudo systemctl enable --now code-server@$USER
# Now visit http://127.0.0.1:8080. Your password is in ~/.config/code-server/config.yaml

SERVER _HACKR, [5/18/2024 2:22 AM]
curl -fOL https://github.com/coder/code-server/releases/download/v$VERSION/code-server-$VERSION-amd64.rpm
sudo rpm -i code-server-$VERSION-amd64.rpm
sudo systemctl enable --now code-server@$USER
# Now visit http://127.0.0.1:8080. Your password is in ~/.config/code-server/config.yaml

SERVER _HACKR, [5/18/2024 2:22 AM]
# Install code-server from the AUR using yay.
yay -S code-server
sudo systemctl enable --now code-server@$USER
# Now visit http://127.0.0.1:8080. Your password is in ~/.config/code-server/config.yaml

SERVER _HACKR, [5/18/2024 2:22 AM]
# Install code-server from the AUR with plain makepkg.
git clone https://aur.archlinux.org/code-server.git
cd code-server
makepkg -si
sudo systemctl enable --now code-server@$USER
# Now visit http://127.0.0.1:8080. Your password is in ~/.config/code-server/config.yaml

SERVER _HACKR, [5/18/2024 2:22 AM]
# Install code-server from the AUR
git clone https://aur.archlinux.org/code-server.git
cd code-server
makepkg -si

SERVER _HACKR, [5/18/2024 2:23 AM]
#!/sbin/openrc-run
name=$RC_SVCNAME
description="$name - VS Code on a remote server"
user="" # your username here
homedir="/home/$user"
command="$(which code-server)"
# Just because you can do this does not mean you should. Use ~/.config/code-server/config.yaml instead
#command_args="--extensions-dir $homedir/.local/share/$name/extensions --user-data-dir $homedir/.local/share/$name --disable-telemetry"
command_user="$user:$user"
pidfile="/run/$name/$name.pid"
command_background="yes"
extra_commands="report"

depend() {
  use logger dns
  need net
}

start_pre() {
  checkpath --directory --owner $command_user --mode 0755 /run/$name /var/log/$name
}

start() {
  default_start
  report
}

stop() {
  default_stop
}

status() {
  default_status
  report
}

report() {
  # Report to the user
  einfo "Reading configuration from ~/.config/code-server/config.yaml"
}

SERVER _HACKR, [5/18/2024 2:23 AM]
rc-update add code-server default

SERVER _HACKR, [5/18/2024 2:23 AM]
rc-service code-server start

SERVER _HACKR, [5/18/2024 2:23 AM]
brew install code-server
brew services start code-server
# Now visit http://127.0.0.1:8080. Your password is in ~/.config/code-server/config.yaml

SERVER _HACKR, [5/18/2024 2:23 AM]
# This will start a code-server container and expose it at http://127.0.0.1:8080.
# It will also mount your current directory into the container as /home/coder/project
# and forward your UID/GID so that all file system operations occur as your user outside
# the container.
#
# Your $HOME/.config is mounted at $HOME/.config within the container to ensure you can
# easily access/modify your code-server config in $HOME/.config/code-server/config.json
# outside the container.
mkdir -p ~/.config
docker run -it --name code-server -p 127.0.0.1:8080:8080 \
  -v "$HOME/.local:/home/coder/.local" \
  -v "$HOME/.config:/home/coder/.config" \
  -v "$PWD:/home/coder/project" \
  -u "$(id -u):$(id -g)" \
  -e "DOCKER_USER=$USER" \
  codercom/code-server:latest

SERVER _HACKR, [5/18/2024 2:23 AM]
rm -rf ~/.local/share/code-server ~/.config/code-server

SERVER _HACKR, [5/18/2024 2:23 AM]
rm -rf ~/.local/lib/code-server-*

SERVER _HACKR, [5/18/2024 2:23 AM]
brew remove code-server

# Alternatively
brew uninstall code-server

SERVER _HACKR, [5/18/2024 2:25 AM]
npm uninstall --global code-server

SERVER _HACKR, [5/18/2024 2:25 AM]
sudo apt remove code-server
