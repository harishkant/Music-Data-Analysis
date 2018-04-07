# Music-Data-Analysis

                                              Music Data Analysis

A leading music-catering company is planning to analyse large amount of data received from
varieties of sources, namely mobile app and website to track the behaviour of users, classify users,
calculate royalties associated with the song and make appropriate business strategies. The file server
receives data files periodically after every 3 hours.



DATA CREATION
Using Python to create the data set file for xml and txt data.

-- Code for XML Data
from random import choice
from random import randint
from typing import List

file = open("D:/file.xml", "w")
file.write("<records>\n")

count = 0
while (count < 21):
    geo_cd_list = ["A", "E", "AU", "AP", "U"]
    song_end_type_list = ["0", "1", "2", "3"]
    timestamp_list: List[str] = ["2016-05-10 12:24:22", "2016-05-09 22:12:36", "2016-05-10 01:38:09",
                                 "2017-05-09 08:09:22"]
    start_ts_list: List[str] = ["2016-05-10 12:24:22", "2016-05-09 22:12:36", "2016-05-10 01:38:09",
                                "2017-05-09 08:09:22"]
    end_ts_list: List[str] = ["2016-05-10 12:24:22", "2016-05-09 22:12:36", "2016-05-10 01:38:09",
                              "2017-05-09 08:09:22"]

    if count % 15 == 0:
         user_id = ""
    else:
                user_id = "U" + str(randint(100, 200))
                song_id = "3" + str(randint(200, 210))
    if count % 11 == 0:
        artist_id = ""
    else:
        artist_id = "A" + str(randint(300, 305))
        timestamp = choice(timestamp_list)
        start_ts = choice(start_ts_list)
        end_ts = choice(end_ts_list)
    if count % 12 == 0:
        geo_cd = ""
    else:
        geo_cd = choice(geo_cd_list)
        station_id = "ST" + str((randint(400, 415)))
        song_end_type = choice(song_end_type_list)
        like = str(randint(0, 1))
        dislike = str(randint(0, 1))
        file.write("<records>\n")
        file.write("<user_id>%s</user_id>\n" % user_id)
        file.write("<song_id>%s</song_id>\n" % song_id)
        file.write("<artist_id>%s</artist_id>\n" % artist_id)
        file.write("<timestamp>%s</timestamp>\n" % timestamp)
        file.write("<start_ts>%s</start_ts>\n" % start_ts)
        file.write("<end_ts>%s</end_ts>\n" % end_ts)
        file.write("<geo_cd>%s</geo_cd>\n" % geo_cd)
        file.write("<station_id>%s</station_id>\n" % station_id)
        file.write("<song_end_type>%s</song_end_type>\n" % song_end_type)
        file.write("<like>%s</like>\n" % like)
        file.write("<dislike>%s</dislike>\n" % dislike)
        file.write("</records>\n")
    count = count + 1
    print("HI")
file.close()

---- Data Screenshot

![xml file screen shot](https://user-images.githubusercontent.com/34162166/38451713-8f6ab16a-3a52-11e8-88ea-1d2e49ec1e1a.png)


------- Code for TXT Data-----------------

from random import choice
from random import randint
from typing import List

file = open("D:/file.txt", "w")

count = 0
while (count < 21):
    geo_cd_list = ["A", "E", "AU", "AP", "U"]
    song_end_type_list = ["0", "1", "2", "3"]
    timestamp_list: List[str] = ["1465230523", "1465130523", "1475130523",
                                 "14595130523"]
    start_ts_list: List[str] = ["1465230523", "1465130523", "1475130523",
                                "14595130523"]
    end_ts_list: List[str] = ["1465230523", "1465130523", "1475130523",
                              "14595130523"]

    if count % 15 == 0:
        user_id = ""
    else:
        user_id = "U" + str(randint(100, 200))
        song_id = "3" + str(randint(200, 210))
    if count % 11 == 0:
        artist_id = ""
    else:
        artist_id = "A" + str(randint(300, 305))
        timestamp = choice(timestamp_list)
        start_ts = choice(start_ts_list)
        end_ts = choice(end_ts_list)
    if count % 12 == 0:
        geo_cd = ""
    else:
        geo_cd = choice(geo_cd_list)
        station_id = "ST" + str((randint(400, 415)))
        song_end_type = choice(song_end_type_list)
        like = str(randint(0, 1))
        dislike = str(randint(0, 1))
        file.write("%s, %s, %s, %s, %s, %s, %s, %s, %s, %s, %s\n" % (user_id,song_id,artist_id,timestamp,start_ts,end_ts,geo_cd,station_id,song_end_type,like,dislike))
    count = count + 1
    print("HI")
file.close()

---- Data ScreenShot---

![txt file screenshot](https://user-images.githubusercontent.com/34162166/38451715-948ff146-3a52-11e8-909c-a0f632278b0f.png)


