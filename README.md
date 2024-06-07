# DD-WRT-4G-LTE

To convert an old WiFi router and phone into a high-performance LTE router in 2024, here's a step-by-step guide leveraging the stability and extended functionality provided by DD-WRT firmware.

## Benefits

- **Rock-Solid Stability:** DD-WRT firmware is known for its stability and is frequently updated by the community.
- **Extended Features:** Advanced networking features such as VPN support, QoS, VLAN, and more.
- **Cost-Effective:** Reuses existing hardware, saving money on new equipment.
 
By converting your old router and smartphone into an LTE router, you achieve a robust and cost-effective solution that can outperform many consumer-grade LTE routers available in the market today. The combination of DD-WRT’s powerful features and the LTE capabilities of your smartphone makes for a versatile and reliable network setup.

## Materials Needed

- **Old Router** (preferably compatible with DD-WRT)
- **Old Smartphone** with LTE capability
- **USB Charging Cable**

## Step 1: Install DD-WRT on the Router

1. **Identify Router Compatibility:**
   
   Check if your old router is compatible with DD-WRT firmware by visiting the DD-WRT database here.

3. **Download DD-WRT Firmware:**
   
   Download the appropriate DD-WRT firmware for your router model from the database.

5. **Flash the Router:**

   Follow the router-specific instructions to flash DD-WRT onto your router. This usually involves:
    - Logging into the router’s web interface.
    - Uploading the DD-WRT firmware.
    - Waiting for the installation to complete.

## Step 2: Set Up the Smartphone as a Hotspot

  1. **Enable Hotspot:**

     On your old smartphone, go to Settings > Network & Internet > Hotspot & Tethering.
     Enable Mobile Hotspot and configure the SSID (network name) and password.

  2. **Connect the Smartphone to the Router:**

     Use a USB cable to connect the smartphone to the router. Some routers with DD-WRT support USB tethering directly. If not, you can still use the phone as a wireless hotspot.

## Step 3: Configure the Router
1. Access Router Web Interface:
   - Connect to the router via a web browser using the default IP address (usually 192.168.1.1).
   
3. Navigate to Setup > Basic Setup:
   - Set the WAN Connection Type to “Automatic Configuration - DHCP” if you’re using the phone as a hotspot wirelessly.
   
3. Configure USB Tethering:
   - If using USB tethering, navigate to Services > USB and enable Core USB Support and USB Over Ethernet (RNDIS).
   - Set the WAN Connection Type to “Mobile Broadband” and input the necessary information such as APN if required.
   
5. Configure Wireless Settings:
   - Go to Wireless > Basic Settings and configure your WiFi SSID and security settings under Wireless Security.
