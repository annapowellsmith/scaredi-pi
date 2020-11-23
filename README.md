**Scaredi-Pi**: The **S**imple **C**ovid **A**mbient **R**eporting **E**-ink **DI**splay for **Pi**.

Script to obtain the latest normalised confirmed Covid-19 case numbers in a local authority,
and display then on an e-paper screen powered by your Raspberry Pi. Run this as a cron job to
update the numbers as often as you like.

<img src="https://i.imgur.com/IK3rQEi.jpg" width="400" style="margin-left: 20px" alt="Dashboard showing case numbers">

Case numbers are obtained from [the official UK coronavirus dashboard API](https://coronavirus.data.gov.uk/details/developers-guide).

Tested on raspberrypi 5.4.51 with a [1.54 inch V2 Waveshare EPD](https://www.waveshare.com/wiki/1.54inch_e-Paper_Module).

To run:

- Install requirements and the [waveshare_epd Python library](https://github.com/waveshare/e-Paper)
  (the latter can't be installed by pip because of the ampersand in the filepath).
- Add a TTF font file of your choice to the `assets` directory
- Update the constants in the script for your chosen font and local authority
- Update the `waveshare_epd` import and drawing commands as needed for your own e-paper screen