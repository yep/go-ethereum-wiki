Ethereum(Go) Requires QML 5.1+

## Mac OS X

`brew tap homebrew/versions`

`brew install qt5`

The following commands assume Qt 5.2.0. Please check your current Qt version

    export QT5VERSION=5.2.0
    export PKG_CONFIG_PATH=`brew --prefix qt5`/lib/pkgconfig

    # For "private/qmetaobject_p.h" inclusion
    export CGO_CPPFLAGS=-I`brew --prefix qt5`/include/QtCore/$QT5VERSION/QtCore
    go get github.com/niemeyer/qml

## Linux

    sudo add-apt-repository ppa:ubuntu-sdk-team/ppa
    sudo apt-get update
    sudo apt-get install ubuntu-sdk qtbase5-private-dev qtdeclarative5-private-dev libqt5opengl5-dev