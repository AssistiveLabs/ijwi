# ijwi
ijwi-tangible AAC device using RFID tech

You will need to install these libraries ) to be able to run both of the scripts.
For information on installing libraries, see:
http://www.arduino.cc/en/Guide/Libraries
- Rfid-master
- SFEMP3shield
- SdFat

Ijwi uses two Arduino scripts:
a) Ijwi-main.ino: this script enables ijwi to be ijwi, this is the one
you load for ijwi to read the stickers and work in AAC device mode.
b) Ijwi-write.ino: this is the code you load to program the RFID
stickers.


To program stickers:
- Modify the portion of code below depending on the number that
corresponds to each sound track, sounds and track numbers need to be
transformed to hexagesimal. Here is a handy website for this:
http://www.rapidtables.com/convert/number/decimal-to-hex.htm


byte sector = 1;
byte blockAddr = 4;
byte dataBlock[] = {
0x01, 0x20, 0x03, 0x04, // 255, 255, 3, 4,
0x05, 0x06, 0x07, 0x08, // 5, 6, 7, 8,
0x08, 0x09, 0xff, 0x0b, // 9, 10, 255, 12,
0x0c, 0x0d, 0x0e, 0x0f // 13, 14, 15, 16
};

You have many numbers to play with here. This means you can link your RFID label and sticker to multiple sound files. We originally linked it to two languages using the first two numbers in the block. 

* if you are interested in getting the original ijwi sound files in Kinyarwanda and English please contact me (@svsquared) at svalenciv [at] gmail.com ) 

