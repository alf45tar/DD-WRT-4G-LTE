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

Connecting your smartphone to the router via Wi-Fi tethering is more flexible than using USB tethering, as it allows you to move around freely and place your smartphone in the optimal location for the best 4G signal reception. This can improve the connection quality and speed for all devices connected to the hotspot.
 
  1. **Enable Hotspot**

     - Open Settings
       
       - Tap the *Settings* app on your iPhone

     - Select Cellular
     
       - Tap *Cellular* or *Mobile Data*, depending on your region

     - Enable Personal Hotspot

        - Tap *Personal Hotspot*
        - Toggle the switch to turn on *Allow Others to Join*
        - Toggle the switch to turn on *Maximize Compatibility* to use 2.4 GHz connection.
     
     - Configure Wi-Fi Password

       - Tap *Wi-Fi Password*
       - Enter a password that others will use to connect to your hotspot
       - Tap *Done* to save the password
      
     The hotspot network name will be the phone name. In my case `iPhone 8`.

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
   
   - Go to `Wireless > Basic Settings` and configure
      - `Radio Mode` to *Station*
      - `Network Mode` to *N Only*
      - `Service Set Identifier (SSID)` with your smartphone hotspot name
      - `Network Configuration` as *Unbridged*
       
     ![](images/Wireless%20-%20Basic%20Settings.jpg)

     Set WiFi password under `Wireless Security` in `WPA Shared Key`
     
     ![](images/Wireless%20-%20Wireless%20Security.jpg)

4. Enable USB

   Using your smartphone as a hotspot can significantly drain its battery. Keeping it connected to a power source is crucial to ensure continuous operation. If your smartphone is close to the router, you can connect it directly to the router's USB port for charging. This can be an efficient way to keep your phone charged without using an additional power outlet.
   
   - To charge your smarphone via router USB, navigate to `Services > USB` and enable *Core USB Support*
   
     ![](images/Services%20-%20USB.jpg)

## Step 4: Connect the Router to the Smartphone

If no devices are connected to the hotspot for a period of time, the iPhone may automatically turn off the hotspot to save battery.

  - Simply turning the hotspot off and back on to reactivate the hotspot
  - A few moment later your router will be connected. Confirm the connection in `Status > WAN`

  ![](images/Status%20-%20WAN.jpg)
