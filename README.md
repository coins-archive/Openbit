

### Coin Specs
<table>
<tr><td>Coin name</td><td>Openbit Coin</td></tr>
<tr><td>Symbol</td><td>OPN</td></tr>
<tr><td>Algo</td><td>Quark Zerocoin</td></tr>
<tr><td>Type</td><td>PoS/MN</td></tr>
<tr><td>Rewards</td><td>MN 75% / POS 25%</td></tr>
<tr><td>Maturity</td><td>120 blocks</td></tr>
<tr><td>Max Coin Supply</td><td>25,000,000</td></tr>
<tr><td>Premine</td><td>1.99% (500000)</td></tr>
<tr><td>Block maturity</td><td>120 blocks</td></tr>
<tr><td>Block Time</td><td>60 Seconds</td></tr>
<tr><td>Min Staking age</td><td>3 hours</td></tr>
<tr><td>Masternode collateral</td><td>2000 OPN</td></tr>
<tr><td>P2P port:</td><td>7091 </td></tr>
<tr><td>RPC port: </td><td>7090 </td></tr>

</table>

### PoS Rewards Table

<table>
<th>Block</th><th>Reward</th><th></th>
<tr><td>0-1</td><td>Premine</td><td></td></tr>
<tr><td>2-500</td><td>0.1 POW</td><td></td></tr>
<tr><td>501-1000</td><td>0.5</td><td>PoS - 0.1 OPN, MN - 0.4 OPN</td></tr>
<tr><td>1001-25000</td><td>1</td><td>PoS - 0.25 OPN, MN - 0.75 OPN</td></tr>
<tr><td>25001-50000</td><td>2</td><td>PoS - 0.50 OPN, MN - 1.5 OPN</td></tr>
<tr><td>50001-75000</td><td>3</td><td>PoS - 0.75 OPN, MN - 2.25 OPN</td></tr>
<tr><td>75001-125000</td><td>2</td><td>PoS - 0.5 OPN, MN - 1.5 OPN</td></tr>
<tr><td>125001-INF</td><td>4</td><td>PoS - 1 OPN, MN - 3 OPN</td></tr>
</table>




Quick installation of the Openbit daemon under linux. See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/openbit/Openbit.git
    cd Openbit
    chmod +x autogen.sh
    cd Openbit/share
    chmod +x genbuild.sh
    cd Openbit/src/leveldb
    chmod +x build_detect_platform
    cd .. / cd ..
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip Openbitd
    sudo strip Openbit-cli
    sudo strip Openbit-tx
    cd ..

Running the daemon:

    Openbitd 

Stopping the daemon:

    Openbit-cli stop

Demon status:

    Openbit-cli getinfo
    Openbit-cli mnsync status

All binaries for different operating systems, you can download in the releases repository:

https://github.com/openbit/Openbit/releases

***

It is recommended [use the shell script](https://openbit.online/masternode.sh) to install a Openbit Coin Masternode on a Linux server running Ubuntu 14.04 or 16.04

***

-
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.
