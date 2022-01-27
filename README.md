# Implementation details of LeTSrPPG
Detailed facial ROI definition

![Figure 1.](https://user-images.githubusercontent.com/3102772/28667872-f392f46a-72ff-11e7-935b-933d33011583.png)

The 22 unit local regions is defined as follows: (1 37 69 2); (37 42 41 40 70 69); (40 28 31 70); (28 43 71 31); (43 48 47 46 72 71); (46 17 16 72); (2 69 73 4 3); (69 70 74 73); (70 30 34 74); (30 71 75 34); (71 72 76 75); (72 16 15 14 76); (4 73 49 5); (73 74 62 49); (74 34 63 62); (34 75 64 66); (75 76 55 64); (76 14 13 55); (5 49 68 7 6); (68 67 58 9 8 7); (67 66 11 10 9 58); (66 55 13 12 11).


<!---[Figure 2.](https://user-images.githubusercontent.com/3102772/28668093-e258c85e-7300-11e7-8c24-8700070140c6.png) --->


<!---Finally, every 4 unit neighbor (Figure 6) REGION OF INTERESTs are combined to form 15 overlapped local REGION OF INTERESTs. As such, local region of interests are defined along the index of the 22 local unit regions. The details are listed as follows, (1 2 7 8); (2 3 8 9); (3 4 9 10); (4 5 10 11); (5 6 11 12); (7 8 13 14); (8 9 14 15); (9 10 15 16); (10 11 16 17); (11 12 17 18); (13 14 19); (14 15 19 20); (15 16 20 21); (16 17 21 22); (17 18 20).--->


The 9 local regions for background LeTSrPPG feature are defined based on the landmark index in Figure 1 as follows: 
ROI.feature(1).ptsIdx = [0 1 2 3 72 73 33 30 29 28 27 39 40 41 36]+1;

ROI.feature(2).ptsIdx = [36 68 72 73 33 74 75 71 45 46 47 42 27 39 40 41]+1;

ROI.feature(3).ptsIdx = [27 28 29 30 33 74 75 13 14 15 16 45 46 47 42]+1;

ROI.feature(4).ptsIdx = [1 2 3 4 48 61 62 33 30 69 68]+1;

ROI.feature(5).ptsIdx = [68 72 48 61 62 63 54 75 71 70 30 69]+1;

ROI.feature(6).ptsIdx = [30 33 51 62 63 54 12 13 14 15 71 70]+1;

ROI.feature(7).ptsIdx = [3 4 5 6 7 8 66 62 33 73 72]+1;

ROI.feature(8).ptsIdx = [72 48 50 6 7 8 9 10 55 54 75 74 33 73]+1;

ROI.feature(9).ptsIdx = [33 62 57 8 9 10 11 12 13 75 74]+1;

We select 4 background regions close to landmark 1, 3, 15, 17
The side length of background regions is determined by the distance between landmark 20 and 25.


