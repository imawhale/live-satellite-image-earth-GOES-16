# live-satellite-image-earth-GOES-16
Get image from live satellite feed of Earth (GOES-16 satellite) via CURL

MAC OS X (paste this code into Terminal):

curl $(curl -s https://www.star.nesdis.noaa.gov/GOES/fulldisk.php?sat=G16 | grep -o -e 'https://cdn.star.nesdis.noaa.gov/GOES16/ABI/FD/GEOCOLOR/[0-9]*_GOES16-ABI-FD-GEOCOLOR-1808x1808.jpg' | head -1) -o earth.jpg && open earth.jpg
reply


CLI (with wget):
wget $(curl -s https://www.star.nesdis.noaa.gov/GOES/fulldisk.php?sat=G16 | grep -o -e 'https://cdn.star.nesdis.noaa.gov/GOES16/ABI/FD/GEOCOLOR/[0-9]*_GOES16-ABI-FD-GEOCOLOR-1808x1808.jpg' | head -1) -O earth.jpg && display earth.jpg
