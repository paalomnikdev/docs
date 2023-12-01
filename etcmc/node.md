# ETCMC digital node operator guide

## Terminology 📓
**Node** - A mini PC where you will run the ETCMC software.

**Workstation** - A PC, Mac, laptop, or tablet used for managing your wallet and from which you will connect to your nodes.

## Preparations ✅

This guide is created specifically for the Firebat AK2 Plus mini PC but will work with most similar mini PCs.

## Hardware list 🖥

 Mini PC with minimal system requirements: 4 cores, 4 threads, 8 GB RAM, 256 GB SSD/NVMe.
- Display emulator to prevent Windows issues related to having no monitor attached (if you don't plan to run your node with a connected monitor).
- Your router should support UPnP (check Google for instructions on how to verify this); otherwise, you will need to do port forwarding manually (use Google for instructions specific to your router).
- (**OPTIONAL**) Wired Ethernet connection equipment like cables and switches is recommended for running nodes, but Wi-Fi will also work.


## Software list for node 📀
- windows 10/11
- ccleaner

## Money 💳
Each ETCMC node requires a digital license (currently priced at $249). You can only purchase it using ETCPOW. Additionally, you will need a self-custodial wallet that supports the ETC blockchain. All licenses and payouts will be tied to your wallet. Therefore, the money-related list includes:
- Funds (USDT/ETC or any cryptocurrency that you will exchange to acquire ETCPOW).
- A self-custodial Web3 wallet.


Assuming you have everything in place and are ready to get started, let's move to the setup section.

## Setup 🛠

1. Plug the display emulator into your node.
2. Connect a display (TV/monitor/etc.), an ethernet cable (if you plan to run it on a wired connection), a keyboard, and a mouse to interact with the system.
3. Start the node.
4. Go through the initial Windows setup. I don't recommend connecting your Microsoft account. Instead, use a unique username for the system user you will create during setup. I recommend writing this username somewhere on the node. Later, you will use this username to get your license (if you run multiple nodes, each will require a separate license with a unique username). The username will be required for each ETCPOW claim from the node.
5. Once done with the initial Windows setup, you are ready for some system tweaks before starting with the ETCMC software.
6. Ensure your node is connected to the internet. Go to Settings -> Windows Update, check for updates, and install any available updates. If it says "You're up to date", pause the updates for the longest available time.
7. Go to Settings -> System -> Power & sleep, and set everything to 'Never'.
8. Go to Settings -> Accounts -> Sign-in options. Disable dynamic lock and set 'If you've been away, when should Windows require you to sign in again?' to 'Never'.
9. Go to Control Panel -> System and Security -> Windows Defender Firewall -> Turn Windows Defender Firewall on or off, select 'Turn off' everywhere, and press 'Ok'.
10. Go to Settings -> System -> Display and set resolution to 1920x1080
11. Install CCleaner.
12. You can install/enable both remote access options mentioned below.
13. (**OPTIONAL IF YOUR NODES WILL BE IN YOUR HOME NETWORK AND YOU WANT TO ACCESS THEM FROM HOME**) Go to Settings -> System -> Remote Desktop and turn on 'Remote Desktop'.
14. (**IF YOUR NODE WILL BE IN A DIFFERENT NETWORK OR YOU WANT TO ACCESS THEM FROM OUTSIDE YOUR HOME**) You can use TeamViewer, Radmin, AnyDesk, etc. for remote access to your nodes, but I recommend using [Google's Remote Desktop](https://remotedesktop.google.com/).
15. (**OPTIONAL, for a convenient way to find your node in the network**) Go to Settings -> System -> About -> Rename this PC, and set it the same as the username you created previously.

## ETCMC Part ✊
Assuming you are done with system setup and you have $249 in your self-custodial wallet or even ETCPOW, you are ready to start this section.

1. Turn off your node, disconnect the display, keyboard, mouse, and any other connected accessories except the display emulator.
2. Place your node where it will be permanently located, connect the ethernet cable (if using a wired connection), connect power, and turn it on.
3. Go to your workstation; further setup will be done remotely.
4. If you're going to use Chrome Remote Desktop, TeamViewer, or similar software, just disregard step 5.
5. If you decide to stick with Microsoft Remote Desktop within your home network, you will need to assign a static IP address to your node. Otherwise, your router might change your node's IP address, and you'll need to find it again. Setting up static IPs is beyond the scope of this manual, so just Google "ROUTER BRAND ROUTER MODEL how to make local IP static" or something similar. You will need the [Microsoft Remote Desktop client](https://learn.microsoft.com/en-us/windows-server/remote/remote-desktop-services/clients/remote-desktop-clients) on your workstation
6. As mentioned previously, you need to have ETCPOW in your self-custodial Web3 wallet on the ETC network.
7. The only way to acquire ETCPOW at the moment is through [Hebeswap DEX](https://hebeswap.com/). The optimal way is to prepare some ETC, send it to your wallet, connect the wallet to Hebeswap, and swap your ETC for ETCPOW. The current license price can be checked at [ETCMC store](https://etcpow-store-c33d80.netlify.app/). You will also need to import the ETCPOW token into your wallet to see your balance. Here's how to do it (verified with MetaMask and OneKey):
```
Open your wallet and click on 'Import Token'.
Token address: 0x6c3B413C461c42a88160Ed1B1B31d6f7b02a1C83.
The rest should fill out automatically.
Token Symbol: ETCPOW.
Decimal: 18.
Click 'Import'.
````
6. Assuming you have enough ETCPOW in your wallet and you are ready to buy your license, go to [shop](https://etcpow-store-c33d80.netlify.app/) and click 'Purchase with ETCPOW', then confirm the transaction with your wallet. DO NOT REFRESH THE PAGE, JUST WAIT FOR DOWNLOAD BUTTON!
7. Once the download button appears, click on it and you will be redirected to a form where you will need to fill in the unique username of your node (the one you're using as the Windows username, if you followed this manual) and your email. It's important to use a unique username for each license you buy, but the wallet should remain the same.
8. After submitting the form, you will be redirected to the download page. Please note that each license allows you to download the installer three times. The installation file is not unique and you can save it to a USB stick or a folder on your workstation and use it for the next nodes you set up.
9. Once you have downloaded the installer file and have remote access to your node from your workstation, let's set up the ETCMC software.
10. You can copy the installation file via a USB flash drive or through the remote connection you chose in previous steps.
11. Run the installer; the installation path is totally up to you, I'm using C:/ETCMC.
12. Once the installation is done, you will get an 'ETCMC LAUNCHER' shortcut on your desktop.
13. If this is not the first ETCMC node in your network, you need to change the network port. Please refer to the FAQ section below for guidance. Once the port configuration is complete, you are ready to proceed to step 14.
14. Right-click on it and select 'Run as administrator' (always start it as an administrator).
15. The 'ETCMC NODE LAUNCHER' window will open. Here, you need to choose the GETH CLIENT.
16. The GETH client will start in another window. Since this is the first start of your node software, you will need to register the node. **YOU CANNOT REGISTER MULTIPLE NODES WITH A SINGLE LICENSE; ONE LICENSE - ONE NODE**.
17. Click the 'REGISTER NODE' button. You will be prompted for your wallet address, username, and email.
18. You should use the exact values you used for the license purchase.
19. Click 'Register'. Once you get a successful response, close this popup. You will not need to do it again for the current node.
20. Your main buttons from now on will be 'EARN ETCPOW' and 'STOP NODE'. Click 'EARN ETCPOW' once.
21. Fresh nodes will download the full ETC blockchain before they start earning for you, which might take up to 5-6 hours. You don't need to do anything; earning will start once the blockchain is downloaded.

## Routine node management 👷‍♂️

Please keep in mind that any power cuts or improper shutdowns may harm your unclaimed balance, so always start and stop your node according to the instructions below.

### Node start 🏁
1. Right click on desktop shortcut -> Run as administrator
2. GETH client
3. EARN ETCPOW

### Node shutdown 🛑
1. STOP NODE
2. Close both ETCMC windows

## FAQ ❓
- **How to run multiple nodes in one network?**
    - To run multiple nodes in a single network, you need to configure a custom network port for each node.
    - The very first node can remain with its default settings; all subsequent nodes should have a custom port.
    - The default ETCMC node port is 30303. The next one should be 30306, followed by 30309, and so on. 
    - Navigate to your ETCMC software installation path -> ETCMC_GUI -> ETCMC_GETH. Right-click on START_GETH_FAST_NODE -> Show more options (skip this step in Windows 10) -> Edit.
    - Notepad will open. You need to find the line:
    - ```geth --classic --syncmode "snap" --cache 1024 --metrics --http --http.addr "localhost" --http.port "8545" --http.corsdomain "*" --ws --ws.addr "localhost" --ws.port "8546" --ws.origins "*" --datadir ".\gethDataDirFastNode" --identity "ETCMCgethNode" console```
    - Replace it with
    - ```geth --classic --syncmode "snap" --cache 1024 --metrics --http --http.addr "localhost" --http.port "8545" --http.corsdomain "*" --ws --ws.addr "localhost" --ws.port "8546" --ws.origins "*" --datadir ".\gethDataDirFastNode" --identity "ETCMCgethNode" --port 30306 console```
    - Simply add the port before the word console, like ```--port 30306```.
    - Press Ctrl + S to save.
    - Close notepad.
- My node isn't earning money! I'm constantly seeing an output like ```Looking for peers peercount=0 blah blah blah```. What should I do?
    - There might be several reasons. First, check that your node has internet access and that the internet can access your node.
    - To check internet access on the node, simply open Chrome, Edge, or whatever browser you have there and try to open any website.
    - To check if the internet can access your node, ensure UPnP is enabled on your router (as mentioned in the hardware list above) and verify that your node's IP address appears in the router's UPnP list.
    - If you have already verified that your internet input and output are okay, then the issue might stem from the ETCMC software/network side, and there is nothing special to do.
    - The ETCMC FAQ suggests "Gracefully stop your node, close the software, and reboot the PC" (instructions are in the node management section above). ETCMC support says to "patiently wait for it". The author of this document does the following: If your node has peercount=0 for 30 minutes or so - stop it, close the software, reboot the PC, and repeat until your node starts to earn ETCPOW.



## Donate 💸

If this guide was helpful for you and you want to say thank you you can tip me to
ETC/ETCPOW address **0xAf8AD530a794cc06c111917640FC3f2948D3c4b4**

## Useful links 🔗
- [![](https://dcbadge.vercel.app/api/server/etcmc)](https://discord.com/invite/etcmc)
