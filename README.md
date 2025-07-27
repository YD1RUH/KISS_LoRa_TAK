<a href="https://info.flagcounter.com/DroY"><img src="https://s01.flagcounter.com/count2/DroY/bg_FFFFFF/txt_000000/border_CCCCCC/columns_8/maxflags_20/viewers_0/labels_0/pageviews_0/flags_0/percent_0/" alt="Flag Counter" border="0"></a>

# KISS_LoRa_TAK
A way KISS (Keep It Simple Stupid), integrated TAK with ESP LoRa Module

<p>
  <img src="https://github.com/YD1RUH/KISS_LoRa_TAK/blob/main/images/LoRa.jpg?raw=true" alt="KISS_LoRa_TAK" width="60%">
</p>

## How to install
- clone this repository: `git clone https://github.com/YD1RUH/KISS_LoRa_TAK.git`
- get in to directory: `cd  KISS_LoRa_TAK`
- install ESP driver, download from [here](https://www.silabs.com/developer-tools/usb-to-uart-bridge-vcp-drivers?tab=downloads), choose `CP210x Windows Drivers`
- download esptool, you can download form [here](https://github.com/espressif/esptool/releases)
- unzip, then set the path directory of esptool that you unzip to `windows environtment variable`

### TTGO LoRa32-OLED
- on directory `KISS_LoRa_TAK`, open CMD and execute this command: `esptool --chip esp32 --port COM[change your port Detected] --baud 460800 write-flash 0x10000 firmware.bin 0x290000 spiffs.bin`
- wait until Upload Process done.

## How to use
1. **First**, KISS_LoRa_TAK will be started as a **HotSpot**, information **SSID** and **Password** will be apear in **OLED**
2. Open browser using Incognito Mode, then access url `tak.local`. this is a webUI for LoRa Parameter Configuration: <br><p>
  <img src="https://github.com/YD1RUH/KISS_LoRa_TAK/blob/main/images/webUI_Config.jpg?raw=true" alt="KISS_LoRa_TAK" width="40%"></p>
3. **It's Recomended** to do configuration on **Config Menu**. after you Click **Save**, KISS_LoRa_TAK will reboot then **SSID** and **Password** will be changes also the LoRa configuration.
4. Connect again to **KISS_LoRa_TAK** hotspot with your new configuration.

## How to start with ATAK
1. Open **ATAK**
2. select `Setting` - `Network Preferences` - `Network Connection preferences` - `Manage Server Connection` - `klik hamburger icon` - `Choose Add`
3. fill the setting like this: <br><p>
  <img src="https://github.com/YD1RUH/KISS_LoRa_TAK/blob/main/images/network_Config.jpg?raw=true" alt="KISS_LoRa_TAK" width="40%"></p>
4. after select `OK`, thick cheklist connection, and wait until CoT streaming status **green** like this: <br><p>
  <img src="https://github.com/YD1RUH/KISS_LoRa_TAK/blob/main/images/Result.jpg?raw=true" alt="KISS_LoRa_TAK" width="40%"></p>
5. now you KISS_LoRa_TAK will be forwarded every `CoT`, `PoI`, `Geofence`, and `message` over **LoRa**

## Feedback
- **Really apreciate** if your mind give me a feedbeack: [Submit Feedback](https://forms.gle/ndPy9DZC3oz5MFPu8)
- **Support** me: [Pateron](https://www.patreon.com/YD1RUH)

## Recommendation LoRa Configuration
<table border="1" cellpadding="8" cellspacing="0">
  <thead>
    <tr>
      <th>Environment</th>
      <th>SF (Spreading Factor)</th>
      <th>Bandwidth (kHz)</th>
      <th>TX Power (dBm)</th>
      <th>Gain (dB)</th>
      <th>Purpose / Effect</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Urban (Dense Buildings)</td>
      <td>SF9 – SF12</td>
      <td>125</td>
      <td>17–20</td>
      <td>4–6</td>
      <td>Good wall penetration; better reliability at the cost of data rate</td>
    </tr>
    <tr>
      <td>Suburban (Houses, Low-rise)</td>
      <td>SF8 – SF10</td>
      <td>125–250</td>
      <td>14–18</td>
      <td>3–5</td>
      <td>Balanced for moderate range and power efficiency</td>
    </tr>
    <tr>
      <td>Rural (Open Field)</td>
      <td>SF7 – SF9</td>
      <td>250–500</td>
      <td>14–17</td>
      <td>0–3</td>
      <td>Fast transmission, long distance in Line-of-Sight</td>
    </tr>
    <tr>
      <td>Indoor (Short Distance)</td>
      <td>SF7 – SF9</td>
      <td>250–500</td>
      <td>10–14</td>
      <td>0–2</td>
      <td>Low latency and power-efficient communication</td>
    </tr>
    <tr>
      <td>Hilly or Forested Terrain</td>
      <td>SF10 – SF12</td>
      <td>125</td>
      <td>17–20</td>
      <td>4–6</td>
      <td>Better performance through non-line-of-sight and foliage</td>
    </tr>
    <tr>
      <td>Critical/Long-Range Application</td>
      <td>SF11 – SF12</td>
      <td>125</td>
      <td>20</td>
      <td>6</td>
      <td>Max range and reliability, at the expense of speed and power</td>
    </tr>
  </tbody>
</table>

## Next To Do ...
- Collaboaration build for another boards
- Waiting someone crazy funding this project to create rugged device

<a href="https://info.flagcounter.com/V2ew"><img src="https://s01.flagcounter.com/map/V2ew/size_m/txt_000000/border_CCCCCC/pageviews_0/viewers_0/flags_0/" alt="Flag Counter" border="0"></a>
