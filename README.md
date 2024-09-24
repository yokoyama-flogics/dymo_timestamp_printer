# Raspberry Pi Dymo LabelWriter® Timestamp Printer

## Disclaimer

This software is provided as-is.  Currently, these files are the only
materials we can offer.  I may not be able to respond to questions
promptly.

![image](images/image.jpg)

## YouTube

- https://www.youtube.com/watch?v=e1wjYJmdkJ8

## Blog (originally in Japanese, translated to English by Google)

- [I Created a Timestamp (Date) Printer with Raspberry Pi (Google Translated)](https://translate.google.com/translate?hl=en&sl=auto&tl=en&u=https%3A%2F%2Fflogics.com%2Fwp%2Fja%2F2017%2F07%2Fraspberry-pi-%25E3%2581%25A7%25E3%2580%2581%25E3%2582%25BF%25E3%2582%25A4%25E3%2583%25A0%25E3%2582%25B9%25E3%2582%25BF%25E3%2583%25B3%25E3%2583%2597%25EF%25BC%2588%25E6%2597%25A5%25E4%25BB%2598%25EF%25BC%2589%25E3%2583%2597%25E3%2583%25AA%25E3%2583%25B3%25E3%2582%25BF%25E3%2582%2592%25E4%25BD%259C%25E3%2581%25A3%2F)

- [Continuation: I Created a Timestamp (Date) Printer with Raspberry Pi (Google Translated)](
https://flogics-com.translate.goog/wp/2017/07/%e7%b6%9a%e3%83%bbraspberry-pi-%e3%81%a7%e3%80%81%e3%82%bf%e3%82%a4%e3%83%a0%e3%82%b9%e3%82%bf%e3%83%b3%e3%83%97%ef%bc%88%e6%97%a5%e4%bb%98%ef%bc%89%e3%83%97%e3%83%aa%e3%83%b3%e3%82%bf%e3%82%92/?_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=ja&_x_tr_pto=wapp)

- [Troubleshooting Dymo Label Printer CUPS Driver (Google Translated)](https://flogics-com.translate.goog/wp/2023/02/dymo-cups-troubleshoot/?_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=ja&_x_tr_pto=wapp)

## File Descriptions

### [Directory `rpi/`](./rpi)

Raspberry Pi software written in shell script is located in the `bin/` directory.

- `printdatetime_server`: A label printing server that runs continuously.

- `printdatetime`: A test program for printing timestamp labels.  (Typically not needed.)

- `start_printdatetime_server`: A monitoring program that should be periodically run via cron or similar.

- `gen_datetime_label`: A sub-program that generates the label image, called by `printdatetime_server`.

- `lpr_datetime_label`: A sub-program that prints the label image, also called by `printdatetime_server`.

### [Directory `etc/`](./etc)

Miscellaneous files that may be helpful.  (Details have been forgotten.)

### [Directory `examples/`](./examples)

Example files for reference.

## Notes

- The Dymo Linux driver can be downloaded [here](https://www.dymo-label-printers.co.uk/news/download-dymo-sdk-for-linux.html).

- [This tutorial](http://www.penguintutor.com/linux/printing-cups) is very useful for setting up a Dymo printer with Raspberry Pi.

- You need to obtain the font file legally.

- Some additional software (e.g. ImageMagick) may be required.

- You can connect a button to start printing.  The GPIO number for the switch is defined by `PORT` in `printdatetime_server`.  Please refer to tutorials like [this one](https://www.circuitbasics.com/how-to-set-up-buttons-and-switches-on-the-raspberry-pi/).

- A more advanced library for GPIO monitoring can also be used.

- Feel free to fork this Git repository if you'd like. :)

Atsushi Yokoyama, Firmlogics

https://flogics.com/
