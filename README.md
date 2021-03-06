# uPyCraft_src
#### uPyCraft is an IDE designed for micropython that supports Windows 7, Windows 8, Windows 10, Linux, MAC OSX 10.11, and above.To make it easier for users to use, uPyCraft is released in green in all systems, no need to install.

# Windows
## Installation
This requires you to have python3.4, pyqt4, py2exe, qsci, pyserial and pyflakes installed.

1. python3.4:<br>

    download address:https://www.python.org/downloads/windows/ <br>
        add python to the windows environment variable when installed.<br> 

    update pip： python -m pip install -U pip 
        add pip to the windows environment variable, such as C:/Python34/Scripts 
        
    pyserial:pip install pyserial 
    
    py2exe  :pip install py2exe
        Python34/Lib/site-packages/py2exe/icons.py Modify lines89:if iconheader.idCount>10 -> if iconheader.idCount>20
        
    pyflakes:pip install pyflakes 
        find api.py and replace with pyflakesChange/api.py 
    
2. pyqt4:<br>

    sip：<br>
        download address:https://www.riverbankcomputing.com/software/sip/download <br>
        
        unpack the directory and open
        exec:
            python configure.py
        
        enter Visual Studio command prompt, changedir to sip installed path
            nmake
            nmake install
        
    PyQt4:<br>
        download address:https://sourceforge.net/projects/pyqt/files/PyQt4/PyQt-4.11.4/ <br>
        follow "next" to install. <br>

## Running
Open uPyCraft.py with python3.4 IDE, click the run module button/F5 to run.

## Package uPyCraft
uPyCraft.exe will be created in directory dist/ .



# Linux
## Environment
ubuntu16.04 LTS     Python3.5   PyQt4
## Install
### SIP<br>
Download SIP from https://riverbankcomputing.com/software/sip/download <br>

    tar zxvf sip-4.19.tar.gz -C /home/PyQt
    sudo python configure.py
    sudo make install
### QT support library<br>

    sudo apt-get install qt4-dev-tools qt4-doc qt4-qtconfig qt4-demos qt4-designer
    sudo apt-get install libqwt5-qt4 libqwt5-qt4-dev
### PyQt4<br>
Download PyQt4_gpl_x11-4.12 from https://sourceforge.net/projects/pyqt/files/PyQt4/ <br>

    tar zxvf PyQt4_gpl_x11-4.12.tar.gz -C /home/PyQt
    cd /home/PyQt/PyQt4_gpl_x11-4.12
    sudo python configure.py
    sudo make
    sudo make install
### Package uPyCraft<br>
    pip install pyinstaller
    pyinstaller -F uPycraft.py
