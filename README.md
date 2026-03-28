# ESPHome SSD1680 E-Paper Display Template (for ZJY152152-0154EAA)

A minimal ESPHome configuration to drive the **ZJY152152-0154EAA** 1.54‑inch e‑paper display (SSD1680 driver).  
This template uses `waveshare_epaper` component with the `2.13in-ttgo-b74` model, which is the only model I personally know of that works with this panel.
![IMG_20260329_024903](https://github.com/user-attachments/assets/e6d8f83f-4d5d-4c7f-842f-1b48bc8c812d)

## Hardware Wiring

| E‑Paper Pin | ESP32 Pin | Description        |
|-------------|-----------|--------------------|
| SCL         | GPIO18    | SPI Clock          |
| SDA         | GPIO23    | SPI Data (MOSI)    |
| CS          | GPIO15    | Chip Select        |
| DC          | GPIO17    | Data/Command       |
| RESET       | GPIO16    | Reset              |
| BUSY        | GPIO4     | Busy signal        |

> **Note**: Adjust pin numbers if your ESP32 board uses different GPIOs.

## Known Issues & Limitations
### Limited Display Area
The `2.13in-ttgo-b74` model is the only ESPHome driver that works with the `ZJY152152-0154EAA` panel. However, it is intended for a larger 2.13‑inch screen; as a result, the actual usable area is only 121×151 pixels (the physical panel is 152×152).

## Contributing
Issues and pull requests are welcome. This template is intended as a starting point; you can extend it with sensors, charts, or weather data.
