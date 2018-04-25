# Heldcoin
Shell script to install an [Heldcoin Masternode](http://heldcoin.xyz/) on a Linux server running Ubuntu 16.04. Use it on your own risk.  
***

## Installation for version 1.0.4
```
wget -q https://raw.githubusercontent.com/Realbityoda/Heldcoin/master/heldcoin_install.sh
bash heldcoin_install.sh
```
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Heldcoin Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **1500** HLDC to **MN1**.  
4. Wait for 16 confirmations.  
5. Go to **Help -> "Debug Window - Console"**  
6. Type the following command: **masternode outputs**  
7. Go to **Masternodes** tab  
8. Click **Create** and fill the details:  
* Alias: **MN1**  
* Address: **VPS_IP:PORT**  
* Privkey: **Masternode Private Key**  
* TxHash: **First value from Step 6**  
* Output index:  **Second value from Step 6**  
* Reward address: leave blank  
* Reward %: leave blank  
9. Click **OK** to add the masternode  
10. Click **Start All**  
***

## Usage:
```
heldcoind masternode status  
heldcoind getinfo
```
Also, if you want to check/start/stop **Heldcoin**, run one of the following commands as **root**:

```
systemctl status heldcoin #To check if Heldcoin service is running  
systemctl start heldcoin #To start Heldcoin service  
systemctl stop heldcoin #To stop Heldcoin service  
systemctl is-enabled heldcoin #To check if Heldcoin service is enabled on boot  
```  
***


## Donations

Any donation is highly appreciated  

**BCH**: qzgnck23pwfag8ucz2f0vf0j5skshtuql5hmwwjhds  
**ETH**: 0x765eA1753A1eB7b12500499405e811f4d5164554  
**LTC**: LNt9EQputZK8djTSZyR3jE72o7NXNrb4aB
