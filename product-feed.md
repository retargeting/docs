# Product Feed

In order for Retargeting to display only products available in stock you need to create a CSV feed that returns some informations about products.

## Requirements

This feed must be accesible on your website (eg. https://www.mywebsite.com/feed.csv)

## Recommendations

If possible update this feed every 2h-4h or even create it realtime when retargeting will access the link.

## CSV Header

```csv
"product id","product name","product url","image url",stock,price,"sale price",brand,category,"extra data"
```

## Example

```csv
"product id","product name","product url","image url",stock,price,"sale price",brand,category,"extra data"
12,"100g Pants",https://demo.store/apparel/mens-clothing/100g-pants/,https://demo.store/images/detailed/0/173283_0113298267324f438bac97eaf.jpg,22,100,75,Adidas,"Men's Clothing","{""variations"":{""Color"":{""id"":""White/Prime Green"",""price"":100,""sale_price"":100,""stock"":20,""margin"":null},""Size"":{""id"":""XX Large"",""price"":100,""sale_price"":100,""stock"":2,""margin"":null}},""margin"":null}"
17,"101 Things Everyone Should Know About Economics A Down and Dirty Guide to Everything from Securities and Derivatives to Interest Rates and Hedge Funds—And What They Mean For You",https://demo.store/books/business-and-investing/101-things-everyone-should-know-about-economics-a-down-and-dirty-guide-to-everything-from-securities-and-derivatives-to-interest-rates-and-hedge-fundsand-what-they-mean-for-you/,https://demo.store/images/detailed/0/Z6595.jpg,19,11.16,11.16,,"Business & Investing","{""variations"":[],""margin"":null}"
148,"16GB A Series Walkman Video MP3",https://demo.store/electronics/mp3-players/mp3-players/16gb-a-series-walkman-video-mp3/,https://demo.store/images/detailed/0/NWZA865BLK.jpg,10,219,130,Sony,"MP3 Players","{""variations"":[],""margin"":null}"
180,"18-55mm Portrait Lens",https://demo.store/electronics/cameras-and-photo/lenses/18-55mm-portrait-lens/,https://demo.store/images/detailed/0/EX-S1855SB_600.jpg,5,199.99,199.99,,Lenses,"{""variations"":[],""margin"":null}"
1,"65"" Class (64.5"" Diag.) LED 8000 Series Smart TV",https://demo.store/electronics/tv-and-video/led-tvs/65-class-64.5-diag.-led-8000-series-smart-tv/,https://demo.store/images/detailed/0/d85_smartTV.jpg,10,6499.99,5399.99,Samsung,"LED TVs","{""variations"":[],""margin"":null}"
241,"Apple® - iPad® with Retina® display Wi-Fi - 32GB - White",https://demo.store/electronics/computers/tablets/apple-ipad-with-retina-display-wi-fi-32gb-white/,https://demo.store/images/detailed/0/ipad-white-1.jpg,10,499,499,Apple,Tablets,"{""variations"":{""3G Connectivity"":{""id"":""Yes"",""price"":499,""sale_price"":499,""stock"":10,""margin"":null},""Memory capacity"":{""id"":""64GB"",""price"":499,""sale_price"":499,""stock"":0,""margin"":null}},""margin"":null}"
240,"Apple® - iPad® with Retina® display Wi-Fi - 64GB - Black",https://demo.store/electronics/computers/tablets/apple-ipad-with-retina-display-wi-fi-64gb-black/,https://demo.store/images/detailed/0/ipad-black-1.jpg,10,499,499,Apple,Tablets,"{""variations"":{""3G Connectivity"":{""id"":""Yes"",""price"":499,""sale_price"":499,""stock"":3,""margin"":null},""Memory capacity"":{""id"":""64GB"",""price"":499,""sale_price"":499,""stock"":7,""margin"":null}},""margin"":null}"
60,AVIC-Z130BT,https://demo.store/electronics/car-electronics/gps-and-navigation/avic-z130bt/,https://demo.store/images/detailed/0/AVIC-Z130BT_reg.jpg,10,1499,1499,Pioneer,"GPS & Navigation","{""variations"":[],""margin"":null}"
94,"Batman: Arkham City (X360)",https://demo.store/video-games/x-box-one/batman-arkham-city-x360/,https://demo.store/images/detailed/0/1000176186_f.jpg,19,59.99,59.99,"Warner Home Video ","X-Box One","{""variations"":[],""margin"":null}"
96,"Batman: Arkham City (X360) CE",https://demo.store/video-games/x-box-one/batman-arkham-city-x360-ce/,https://demo.store/images/detailed/0/1000235553_f.jpg,4,99.99,99.99,"Warner Home Video ","X-Box One","{""variations"":[],""margin"":null}"
201,"Beethoven Piano Concertos Nos. 1 & 2",https://demo.store/music/classical/beethoven-piano-concertos-nos.-1-and-2/,https://demo.store/images/detailed/0/url_uploaded_file_13287720374f3373c6eef1f.jpg,20,12.67,12.67,,Classical,"{""variations"":[],""margin"":null}"
114,"Birds of Prey: The Complete Series (DVD)",https://demo.store/movies-and-tv/movies-dvd/birds-of-prey-the-complete-series-dvd/,https://demo.store/images/detailed/0/1917865.jpg,9,14.24,14.24,"Warner Home Video ","Movies (DVD)","{""variations"":[],""margin"":null}"
196,"Feeding the Monkies At Ma Maison (Zappa)",https://demo.store/music/rock/feeding-the-monkies-at-ma-maison-zappa/,https://demo.store/images/detailed/0/feedingthemonkies_frntLRG.jpg,24,17,17,,Rock,"{""variations"":[],""margin"":null}"
43,FH-P8000BT,https://demo.store/electronics/car-electronics/in-dash-stereos/fh-p8000bt/,https://demo.store/images/detailed/0/FH-P8000BT_main_Lrg.jpg,15,369,369,Pioneer,"In-Dash Stereos","{""variations"":[],""margin"":null}"
104,"Final Destination 5 (Blu-ray)",https://demo.store/movies-and-tv/blu-ray-discs/final-destination-5-blu-ray/,https://demo.store/images/detailed/0/3083326.jpg,15,29.95,29.95,"Warner Bros.","Blu-ray Discs","{""variations"":[],""margin"":null}"
76,"FLIPSIDE with MOTOBLUR",https://demo.store/electronics/cell-phones/motorola/flipside-with-motoblur/,https://demo.store/images/detailed/0/217Lf0Ah3rL._SX220_.jpg,10,439.99,439.99,Motorola,Motorola,"{""variations"":[],""margin"":null}"
129,"Fore CR1",https://demo.store/sports-and-outdoors/bikes/road-bikes/fore-cr1/,https://demo.store/images/detailed/0/1316633534_CR1-2012-315.jpg,10,1799,1799,,"Road Bikes","{""variations"":[],""margin"":null}"
127,"Fore CR5 SRAM Red",https://demo.store/sports-and-outdoors/bikes/road-bikes/fore-cr5-sram-red/,https://demo.store/images/detailed/0/1312496083_CR5-2011-315-sram.jpg,10,4779,4779,,"Road Bikes","{""variations"":[],""margin"":null}"
121,"Fringe: The Complete Third Season",https://demo.store/movies-and-tv/tv-shows-dvd/fringe-the-complete-third-season/,https://demo.store/images/detailed/0/2980261.jpg,20,17.99,17.99,"Warner Home Video ","TV Shows (DVD)","{""variations"":[],""margin"":null}"
103,"Fringe: The Complete Third Season (Blu-Ray)",https://demo.store/movies-and-tv/blu-ray-discs/fringe-the-complete-third-season-blu-ray/,https://demo.store/images/detailed/0/2980245.jpg,20,23.99,23.99,"Warner Home Video ","Blu-ray Discs","{""variations"":[],""margin"":null}"
95,"Game Party: In Motion (X360)",https://demo.store/video-games/x-box-one/game-party-in-motion-x360/,https://demo.store/images/detailed/0/2832686.jpg,24,19.99,19.99,"Warner Home Video ","X-Box One","{""variations"":[],""margin"":null}"
182,"GBC® Smart-View® 3-Ring Report Cover",https://demo.store/office-supplies/desk-accessories/gbc-smart-view-3-ring-report-cover/,https://demo.store/images/detailed/0/mbank15770_w550_h550.jpg,30,6.8,6.8,,"Desk Accessories","{""variations"":[],""margin"":null}"
41,"Gift Set (Onesie Plus Socks)",https://demo.store/apparel/womens-clothing/gift-set-onesie-plus-socks/,https://demo.store/images/detailed/0/X32679_01.jpg,0,35,35,Adidas,"Women's Clothing","{""variations"":{""Size"":{""id"":""XX Large"",""price"":35,""sale_price"":35,""stock"":0,""margin"":null}},""margin"":null}"
56,GM-6500F,https://demo.store/electronics/car-electronics/amplifiers/gm-6500f/,https://demo.store/images/detailed/0/GM-6500F_large.jpg,10,220,220,Pioneer,Amplifiers,"{""variations"":[],""margin"":null}"
247,"Nokia N1 Pad 7.9"" Quad-Core 64bit 2.3GHz 2GB 32GB Android 5.0",https://demo.store/electronics/computers/tablets/nokia-n1-pad-7.9-quad-core-64bit-2.3ghz-2gb-32gb-android-5.0/,https://demo.store/images/detailed/1/nokia_n1_perspectives_-_app.jpg,21,329.49,329.49,,Tablets,"{""variations"":{""Color"":{""id"":""Yellow"",""price"":329.49,""sale_price"":329.49,""stock"":19,""margin"":null},""3G Connectivity"":{""id"":""Yes"",""price"":329.49,""sale_price"":329.49,""stock"":1,""margin"":null},""Memory capacity"":{""id"":""128GB"",""price"":329.49,""sale_price"":329.49,""stock"":1,""margin"":null}},""margin"":null}"
120,"Samsung Galaxy S II, Epic 4G Touch (Black)",https://demo.store/electronics/cell-phones/samsung/samsung-galaxy-s-ii-epic-4g-touch-black/,https://demo.store/images/detailed/0/d710_600x600_xlarge_cf.jpg,9,199.99,199.99,Samsung,Samsung,"{""variations"":[],""margin"":null}"
223,"Samsung Galaxy Tab 8.9 (Wi-Fi Only) - 32GB Metallic Gray",https://demo.store/electronics/computers/tablets/samsung-galaxy-tab-8.9-wi-fi-only-32gb-metallic-gray/,https://demo.store/images/detailed/0/p7310_400x400_large1_cf_1.jpg,9,499.99,499.99,Samsung,Tablets,"{""variations"":[],""margin"":null}"
14,"Toshiba 40E220U 40"" Class 1080P HD LCD TV",https://demo.store/electronics/tv-and-video/plasma-tvs/toshiba-40e220u-40-class-1080p-hd-lcd-tv/,https://demo.store/images/detailed/0/40e220u.jpg,14,499.99,499.99,Toshiba,"Plasma TVs","{""variations"":[],""margin"":null}"
9,"Toshiba 42TL515U 42"" Class 1080P 3D LED HD TV",https://demo.store/electronics/tv-and-video/3d-tvs/toshiba-42tl515u-42-class-1080p-3d-led-hd-tv/,https://demo.store/images/detailed/0/led-tv-42TL515-01.jpg,15,999.99,999.99,Toshiba,"LED TVs","{""variations"":[],""margin"":null}"
140,"Yamaha PDX-11 DB",https://demo.store/electronics/mp3-players/mp3-speaker-systems/yamaha-pdx-11-db/,https://demo.store/images/detailed/0/p149239z.jpg,10,99.95,99.95,Yamaha,"MP3 Speaker Systems","{""variations"":[],""margin"":null}"
141,"Yamaha PDX-11 GR",https://demo.store/electronics/mp3-players/mp3-speaker-systems/yamaha-pdx-11-gr/,https://demo.store/images/detailed/0/p149240z.jpg,10,99.95,99.95,Yamaha,"MP3 Speaker Systems","{""variations"":[],""margin"":null}"
144,"Yamaha PDX-30BU",https://demo.store/electronics/mp3-players/mp3-speaker-systems/yamaha-pdx-30bu/,https://demo.store/images/detailed/0/p98945z.jpg,11,99.95,99.95,Yamaha,"MP3 Speaker Systems","{""variations"":[],""margin"":null}"
143,"Yamaha PDX-30PI",https://demo.store/electronics/mp3-players/mp3-speaker-systems/yamaha-pdx-30pi/,https://demo.store/images/detailed/0/p98947z.jpg,7,79.95,79.95,Yamaha,"MP3 Speaker Systems","{""variations"":[],""margin"":null}"
142,"Yamaha TSX-130WH",https://demo.store/electronics/mp3-players/mp3-speaker-systems/yamaha-tsx-130wh/,https://demo.store/images/detailed/0/p95910z.jpg,10,399.95,399.95,Yamaha,"MP3 Speaker Systems","{""variations"":[],""margin"":null}"
13,"Your Idea, Inc. 12 Steps to Building a Million Dollar Business -- Starting Today!",https://demo.store/books/business-and-investing/your-idea-inc.-12-steps-to-building-a-million-dollar-business-starting-today/,https://demo.store/images/detailed/0/Z2580.jpg,9,12,11.96,,"Business & Investing","{""variations"":[],""margin"":null}"
```
