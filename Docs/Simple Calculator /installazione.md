# Aggiorniamo il sistema operativo
sudo apt update

sudo apt upgrade -y

# Installiamo le dipendenze necessarie per Swift e lo sviluppo con KDE
sudo apt install -y \
  binutils \
  git \
  gnupg2 \
  libc6-dev \
  libcurl4-openssl-dev \
  libedit2 \
  libgcc-13-dev \
  libpython3.12 \
  libsqlite3-0 \
  libstdc++-13-dev \
  libxml2-dev \
  libz3-dev \
  pkg-config \
  tzdata \
  unzip \
  zlib1g-dev \
  qt6-base-dev \
  qt6-declarative-dev \
  cmake \
  extra-cmake-modules

# Scarichiamo Swift 6.0.3
wget https://download.swift.org/swift-6.0.3-release/ubuntu2404/swift-6.0.3-RELEASE/swift-6.0.3-RELEASE-ubuntu24.04.tar.gz

# Estraiamo l'archivio e installiamo Swift
tar xzf swift-6.0.3-RELEASE-ubuntu24.04.tar.gz

sudo mv swift-6.0.3-RELEASE-ubuntu24.04 /usr/share/swift

# Aggiungiamo Swift al PATH
echo 'export PATH=/usr/share/swift/usr/bin:$PATH' >> ~/.bashrc
source ~/.bashrc

# Verifichiamo l'installazione di Swift
swift --version

# Installiamo Visual Studio Code
sudo snap install code --classic

# Installiamo le estensioni per Swift in VS Code
code --install-extension swiftlang.swift-vscode

code --install-extension vadimcn.vscode-lldb
