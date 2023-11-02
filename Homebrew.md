Install Homebrew on your linux distribution:   
"The Homebrew package manager may be used on Linux and Windows Subsystem for Linux (WSL) 2.
 Homebrew was formerly referred to as Linuxbrew when running on Linux or WSL. 
 Homebrew does not use any libraries provided by your host system, except glibc and gcc if they are new enough. 
 Homebrew can install its own current versions of glibc and gcc for older distributions of Linux"   @ https://docs.brew.sh/Homebrew-on-Linux

1. Install group developments tools for linux:  
**`# sudo dnf groupinstall 'Development Tools' `**

2. Install other necesssary tools:  
**`# sudo dnf install procps-ng curl file git `**

3. Install Homebrew (you have not to be root)  
**`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" `**
