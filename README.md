# Deploy-Qt-application-for-Windows-using-mxe-on-Linux

**Step 1:** Getting MXE
```bash
git clone https://github.com/mxe/mxe.git
```
**Step 2:** Installing build [dependencies](https://mxe.cc/#requirements)

Debian
```bash
apt-get install \
    autoconf \
    automake \
    autopoint \
    bash \
    bison \
    bzip2 \
    flex \
    g++ \
    g++-multilib \
    gettext \
    git \
    gperf \
    intltool \
    libc6-dev-i386 \
    libgdk-pixbuf2.0-dev \
    libltdl-dev \
    libssl-dev \
    libtool-bin \
    libxml-parser-perl \
    lzip \
    make \
    openssl \
    p7zip-full \
    patch \
    perl \
    python3 \
    python3-mako \
    ruby \
    sed \
    unzip \
    wget \
    xz-utils
```
For other destr [here](https://mxe.cc/#requirements)

**Step 2:** Building Qt for Windows

```bash
cd mxe
```
For base functionality build qtbase
```bash
make qtbase
```
if u use extra functionality build qt5 or qt6, depending on the version of Qt
```bash
make qt5
```
```bash
make qt6
```
