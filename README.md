# live-satellite-image-earth-GOES-16
Get image from live satellite feed of Earth (GOES-16 satellite) via CURL.

For MAC OS X, paste this code into Terminal:

curl $(curl -s https://www.star.nesdis.noaa.gov/GOES/fulldisk.php?sat=G16 | grep -o -e 'https://cdn.star.nesdis.noaa.gov/GOES16/ABI/FD/GEOCOLOR/[0-9]*_GOES16-ABI-FD-GEOCOLOR-1808x1808.jpg' | head -1) -o earth.jpg && open earth.jpg
reply


For CLI with wget paste this code into Terminal:
wget $(curl -s https://www.star.nesdis.noaa.gov/GOES/fulldisk.php?sat=G16 | grep -o -e 'https://cdn.star.nesdis.noaa.gov/GOES16/ABI/FD/GEOCOLOR/[0-9]*_GOES16-ABI-FD-GEOCOLOR-1808x1808.jpg' | head -1) -O earth.jpg && display earth.jpg

![earth](https://user-images.githubusercontent.com/50163135/72247019-5a0b1b80-3637-11ea-9115-b988a3dbe1d2.jpg)
