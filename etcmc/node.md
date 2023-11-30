ETCMC digital node operator guide

Donate

If this guide was helpful for you and you want to say thank you you can tip me to
ETC/ETCPOW address 0xAf8AD530a794cc06c111917640FC3f2948D3c4b4

Preparations

This guide created for specific mini PC Firebat AK2 plus but will work with most similar mini PCs.

Hardware list:
- mini PC with minimal system requirements: 4 cores, 4 threads, 8 Gb RAM, 256 Gb SSD/NVMe
- display emulator to prevent Windows issues related to no monitor attached (if you don't plan to run your node with connected monitor)
- your router should support UPnP(check in Google instructions how to check it) otherwise you will need to do port forwarding manually(use Google for particular router instructions)
- (OPTIONAL) wired ethernet connection stuff like cables/switches/etc, it is recommended to run nodes via wired connection but Wi-Fi will work as well


Software list:
- windows 10/11
- ccleaner

Money:
each ETCMC node requires digital license (249$ at the moment), you can buy it only with ETCPOW, also you will need self-custodial wallet with ETC blockchain support, all licenses and payouts will be tied to your wallet, so money-related list is
- money itself(USDT/ETC or any coin you will exchange to get ETCPOW)
- self-custodial web3 wallet


Assuming you have everything in place and ready to get started let's move to setup section

Setup
1. Plug in display emulator into your mini PC
2. Connect any display(TV/monitor/etc), ethernet cable(if you are plan to run it on wired connection), keyboard and mice to be able to interact with system
3. Start mini PC
4. Go through initial windows setup, I don't recommend you to connect your Microsoft account. Instead of it use some unique username for system user you will create during setup. Also I recommend to write this username somwhere on mini PC. Later you will use this username to get your license(in case you will run multiple nodes each node will require separated license with unique username). Username will be required on each ETCPOW claim from node.
5. Once you are done with initial Windows setup you are ready to go to some system tweaks before we will start with ETCMC software.
6. Ensure your mini PC already connected to internet and go to Settings -> Windows Update, check for the updates and install any updates you willbe proposed. If you are seeing "You're up to date" - pause the updates for longest time is available.
7. Go to Settings -> Power -> Screen and sleep and set everything to Never
8. Go to Settings -> Accounts -> Sign-in options. Disable dynamic lock and set If you've been away, when should Windows require you to sign in again? to Never
9. Go to Control Panel -> System and Security -> Windows defender firewall -> Turn Windows Defender Firewall on or off and seclect Turn off everywhere and press Ok
10. Install Ccleaner
11. (OPTIONAL IF YOUR NODES WILL LIVE IN YOUR HOME NETWORK AND YOU WANT TO ACCESS THEM FROM HOME)Go to Settings -> System -> Remote desktop and turn on Remote desktop
12. (IF YOUR NODE WILL LIVE IN DIFFERENT NETWORK OR YOU WANT TO ACCESS THEM FROM OUTSIDE YOUR HOME) You can use Teamviewer/Radmin/Anydesk/etc for remote access to your nodes but I recommend you to use Google's Remote Desktop https://remotedesktop.google.com/
13. (OPTIONAL, for convinient way to find your node in network) Go to Settings -> System -> About -> Rename this PC and set the same as username you created previously.

ETCMC part
Assuming you are done with system setup and you have 249$ on your self-custodial wallet or even ETCPOW you can ready to start with this section.
1. Turn off your mini PC, disconnect display/keyboard/mice and any other connected accessories except display emulator.
2. Put your mini PC to place where it will live, connect ethernet cable(if you will run with wired connection), connect power and turn it on.
3. Go to your main computer, further setup you will do remotely.
