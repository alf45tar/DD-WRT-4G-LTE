# DD-WRT-4G-LTE

To convert an old WiFi router and phone into a high-performance LTE router in 2024, here's a step-by-step guide leveraging the stability and extended functionality provided by DD-WRT firmware.

## Benefits

- **Rock-Solid Stability**
  
  DD-WRT firmware is known for its stability and is frequently updated by the community.
  
- **Extended Features**

  Advanced networking features such as VPN support, QoS, VLAN, and more.
  
- **Cost-Effective**
  
  Reuses existing hardware, saving money on new equipment.
 
By converting your old router and smartphone into an LTE router, you achieve a robust and cost-effective solution that can **outperform many consumer-grade LTE routers** available in the market today. The combination of DD-WRT’s powerful features and the LTE capabilities of your smartphone makes for a versatile and reliable network setup.

It's true that technological advancements in smartphones and LTE modems have progressed at different rates. In 2017, smartphones such as the iPhone 8 were equipped with LTE Category 12 modems, which supported download speeds up to 600 Mbps. In contrast, many consumer LTE routers, particularly those targeting more budget-conscious markets, have continued to use lower category modems like Category 4, which support download speeds up to 150 Mbps.

## Materials Needed

- **Old Router** (compatible with DD-WRT)
  
  I am using a TP-Link Archer C9 lauched in 2014 with simultaneous 2.4GHz 600 Mbps and 5GHz 1300 Mbps connections for 1.9 Gbps of total available bandwidth.
  
- **Old Smartphone** with LTE capability
  
  I am using an iPhone 8 lauched in 2017 equipped with a Category 12 modem up to 600 Mbps in download.
  
- **USB Charging Cable**

## Step 1: Install DD-WRT on the Router

1. **Identify Router Compatibility**
   
   Check if your old router is compatible with DD-WRT firmware by visiting the DD-WRT database [here](https://dd-wrt.com/support/router-database/).

3. **Download DD-WRT Firmware**
   
   Download the appropriate DD-WRT firmware for your router model from the database.

5. **Flash the Router**

   Follow the router-specific instructions to flash DD-WRT onto your router. This usually involves:
    - Logging into the router’s web interface.
    - Uploading the DD-WRT firmware.
    - Waiting for the installation to complete.

## Step 2: Set Up the Smartphone as a Hotspot
 
  1. **Enable Hotspot**

     - Open Settings
       
       - Tap the *Settings* app on your iPhone

     - Select Cellular
     
       - Tap *Cellular* or *Mobile Data*, depending on your region

     - Enable Personal Hotspot

        - Tap *Personal Hotspot*
        - Toggle the switch to turn on *Allow Others to Join*
     
     - Configure Wi-Fi Password

       - Tap *Wi-Fi Password*
       - Enter a password that others will use to connect to your hotspot
       - Tap *Done* to save the password

  2. **Connect the Smartphone to the Router**

     Connecting your smartphone to the router via Wi-Fi tethering is more flexible than using USB tethering, as it allows you to move around freely and place your smartphone in the optimal location for the best 4G signal reception. This can improve the connection quality and speed for all devices connected to the hotspot.
    
     Using your smartphone as a hotspot can significantly drain its battery. Keeping it connected to a power source is crucial to ensure continuous operation. If your smartphone is close to the router, you can connect it directly to the router's USB port for charging. This can be an efficient way to keep your phone charged without using an additional power outlet. 

## Step 3: Configure the Router

1. Access Router Web Interface:
   
   - Connect to the router via a web browser using the default IP address (usually `192.168.1.1`)
   
2. Navigate to `Setup > Basic Setup`
   
   - Set the WAN Connection Type to *Automatic Configuration - DHCP* if you’re using the phone as a hotspot wirelessly
  
     ![](images/Setup%20-%20Basic%20Setup.jpg)

3. Navigate `Setup > Advanced Routing`

   - Set the Operating Mode to *Gateway*. In Gateway mode the router is hosting your network's connection to the Internet and performs NAT, while in other modes it does not.
  
     ![](images/Setup%20-%20Advanced%20Routing.jpg)
     
   
3. Configure Wireless Settings
   
   - Go to `Wireless > Basic Settings` and configure your WiFi SSID and WiFi password under `Wireless Security`
  
     ![](images/Wireless%20-%20Basic%20Settings.jpg)

     
     ![](images/Wireless%20-%20Wireless%20Security.jpg)

5.

6. Configure USB Tethering:
   - If using USB tethering, navigate to `Services > USB` and enable *Core USB Support*.
   - Set the WAN Connection Type to “Mobile Broadband” and input the necessary information such as APN if required.

     ![](images/Services%20-%20USB.jpg)
