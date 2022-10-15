# Deploy-Qt-application-for-Windows-using-mxe-on-Linux

**Step 1:** Get MXE
```bash
git clone https://github.com/mxe/mxe.git
```
**Step 2:** Install dependencies

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

**Step 2:** Build Qt for Windows

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

If u want a 64-bit executable application, build Qt with
```bash
make MXE_TARGETS=x86_64-w64-mingw32.static qtbase
```

Unfortunately, I could not build qt6, but with qt5 the application was able to deploy, despite the fact that I used qt6. If u lucky, u can build qt6)

**Step 3:** Prepare environment

```bash
export PATH=<directory of mxe folder>/usr/bin:$PATH  
```

**Step 4:** Get to the directory of your app(WHERE SOURCES, NOT BUILD), and run the Qt Makefile generator tool:

```bash
<directory of mxe folder>/usr/bin/i686-w64-mingw32.static-qmake-qt5
```

**Step 5:** Build your project

```bash
make
```
You should find the binary in the ./release directory


***HAPPY END FOR RAIK199X***
