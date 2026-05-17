# LamePod
There remains a lack of open source projects which provide the blueprints for chasis, firmware, and hardware for a DIY smart speaker. Major corperation voice assistants work off the backs of the FOSS communities and profiteer off of the data provided by such devices. I aim to provide an alternative for like minded individuals seeking highly polished DIY smart speakers that respect your privacy and the FOSS projects it is built on.

***Warning:*** *This project is still in complete infancy. Currently the repo is just for internal use right now as I work on implementing the first set of code. **It is NOT functional** as of now.*

## Overview
The LamePod project was conceived to imitate the functionality and aesthetics of the Apple HomePod using ESPHome, FOSS code, and open hardware. LamePod aspires to be a polished, good looking, highly functional alternative to corperate products which cost a lot of money, yet still profit off of your data at the cost of developers, the planet, and individuals. 

### Initial Proof of Concept Hardware
Currently the project is designed to operate around Sonocotta's ESP32 hardware projects. The initial proof of concept will incorperate the following hardware and a 3D printed chasis. 

|  Component | Hardware Used  |    Product Providing Component    |
| ---------- | -------------- | --------------------------------- |
|   Logic    |    ESP32-S3    |      Sonocotta Louder ESP32       |
|    DAC     |    TAS5805M    |      Sonocotta Louder ESP32       |
| Amplifier  |    TAS5805M    |      Sonocotta Louder ESP32       |
|  Ethernet  |      W5500     | Sonocotta Provided Ethernet Addon |
|  Speaker   |  4" Full Range |       Dayton Audio RS100-4        |
| Microphone |     XVF3800    |  Seeed Studio Respeaker XVF3800   |
|    LED     |   WS2812B 8x8  | BTF-LIGHTING WS2812B RGB 5050SMD  |
|   Power    |   20V 2A PSU*  |  Amazon EL Listed Wall Brick**    |
|  5V Down   | Buck Converter |      [DROK Buck Converter](https://www.amazon.com/dp/B01NALDSJ0?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1) |

\* *20V, 2A will provide a little less than 40W for the entire speaker*

\** *I wanted something somwehat safer than random power supplies off the internet (so UL or ETL listed for the US) that would provide enough power for the setup without requiring anything unsighly/bulky*

### Intended Expansions for Future Designs
The major change I would want to implement is a refinement on the speaker crossover setup. Currently my proof of concept is designed around a single, full range driver. This reduces the quality of the produced audio and limits the ability of the speaker to produce lower frequencies. The compromise was chosen to simplify the conception and expediate the release of the first prototype.


### Software & Firmware
ESPHome will be used as the basis for the firmware and software design of the DAC, amplifier, microphone, and LED components of the project. ESPHome firmware will be included in the project as modular ESPHome packages that can be included based on molularity and desired functionality. 


## AI Policy
### Paradigm
Generative AI is a product of stolen intelectual and creative properties and its use is damaging to the environment. In the opinion of this author, the former goes against the prinicples of FOSS software and the second is unacceptable, especially considering the little actual benefit provided by AI. 

### Policy
AI may be used for proofreading or rubber ducking purposes. AI may not be used to generate code. In other words, all code contained within this repository must be human made and all pull requests using AI generated code will be rejected.

## Credits
Much of the credit goes to the following repositories and projects:

[formatBCE Respeaker XVF3800](https://github.com/formatBCE/Respeaker-XVF3800-ESPHome-integration)

[sonocotta ESP32 Audio Dock](https://github.com/sonocotta/esp32-audio-dock)

Seeed Studio

[ESPHome](https://esphome.io/)