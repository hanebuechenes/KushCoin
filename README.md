Kushcoin
========

Installation from source
------------------------

Recommended linux environment, Ubuntu XENIAL (16.04).

Install dependencies:

    sudo apt-get install git build-essential libtool autotools-dev automake pkg-config libssl-dev \
        libevent-dev bsdmainutils libboost-all-dev libqrencode-dev qt4-qmake libqt4-dev \
        libprotobuf-dev protobuf-compiler software-properties-common
     
    sudo add-apt-repository ppa:bitcoin/bitcoin
    sudo apt-get update
    sudo apt-get install libdb4.8-dev libdb4.8++-dev

Get the source:

    git clone https://github.com/hanebuechenes/KushCoin.git

To compile `kushcoind` under linux:

    cd KushCoin/src/
    make -f makefile.unix USE_O3=1 USE_ASM=1 USE_LEVELDB=1

Run the binary:

    cd KushCoin
    ./bin/amd64/kushcoind


To compile `kushcoin-qt` under linux

    cd kushcoin
    qmake USE_O3=1 USE_ASM=1 USE_LEVELDB=1
    make

See docs/

RPC Port: 31543
Network Port: 31544


=========================================================================================================
actual situation:

KushCoin will run under ubuntu 16 only. There is a big development hole, what has to be filled, to make it running 
on actual systems also..

The encluded .bin file is compiled for running on Ubuntu 16.04.

