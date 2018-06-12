# IPv6

## Subnet prefix lengths

```bash
2402:9400:0000:0000:0000:0000:0000:0001
XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XXXX
      ||| |||| |||| |||| |||| |||| ||||
      ||| |||| |||| |||| |||| |||| |||128
      ||| |||| |||| |||| |||| |||| ||124
      ||| |||| |||| |||| |||| |||| |120
      ||| |||| |||| |||| |||| |||| 116
      ||| |||| |||| |||| |||| |||112
      ||| |||| |||| |||| |||| ||108
      ||| |||| |||| |||| |||| |104
      ||| |||| |||| |||| |||| 100
      ||| |||| |||| |||| |||96
      ||| |||| |||| |||| ||92
      ||| |||| |||| |||| |88
      ||| |||| |||| |||| 84
      ||| |||| |||| |||80
      ||| |||| |||| ||76
      ||| |||| |||| |72
      ||| |||| |||| 68
      ||| |||| |||64
      ||| |||| ||60
      ||| |||| |56
      ||| |||| 52
      ||| |||48
      ||| ||44
      ||| |40
      ||| 36
      ||32
      |28
      24
```

## Subnet size

| IPv6 CIDR Subnet     | Number of IPs                                      |
| -------------------- | -------------------------------------------------: |
| /128                 | 1                                                  |
| /127                 | 2                                                  |
| /126                 | 4                                                  |
| /125                 | 8                                                  |
| /124                 | 16                                                 |
| /123                 | 32                                                 |
| /122                 | 64                                                 |
| /121                 | 128                                                |
| /120                 | 256                                                |
| /119                 | 512                                                |
| /118                 | 1,024                                              |
| /117                 | 2,048                                              |
| /116                 | 4,096                                              |
| /115                 | 8,192                                              |
| /114                 | 16,384                                             |
| /113                 | 32,768                                             |
| /112                 | 65,536                                             |
| /111                 | 131,072                                            |
| /110                 | 262,144                                            |
| /109                 | 524,288                                            |
| /108                 | 1,048,576                                          |
| /107                 | 2,097,152                                          |
| /106                 | 4,194,304                                          |
| /105                 | 8,388,608                                          |
| /104                 | 16,777,216                                         |
| /103                 | 33,554,432                                         |
| /102                 | 67,108,864                                         |
| /101                 | 134,217,728                                        |
| /100                 | 268,435,456                                        |
| /99                  | 536,870,912                                        |
| /98                  | 1,073,741,824                                      |
| /97                  | 2,147,483,648                                      |
| /96                  | 4,294,967,296                                      |
| /95                  | 8,589,934,592                                      |
| /94                  | 17,179,869,184                                     |
| /93                  | 34,359,738,368                                     |
| /92                  | 68,719,476,736                                     |
| /91                  | 137,438,953,472                                    |
| /90                  | 274,877,906,944                                    |
| /89                  | 549,755,813,888                                    |
| /88                  | 1,099,511,627,776                                  |
| /87                  | 2,199,023,255,552                                  |
| /86                  | 4,398,046,511,104                                  |
| /85                  | 8,796,093,022,208                                  |
| /84                  | 17,592,186,044,416                                 |
| /83                  | 35,184,372,088,832                                 |
| /82                  | 70,368,744,177,664                                 |
| /81                  | 140,737,488,355,328                                |
| /80                  | 281,474,976,710,656                                |
| /79                  | 562,949,953,421,312                                |
| /78                  | 1,125,899,906,842,624                              |
| /77                  | 2,251,799,813,685,248                              |
| /76                  | 4,503,599,627,370,496                              |
| /75                  | 9,007,199,254,740,992                              |
| /74                  | 18,014,398,509,481,985                             |
| /73                  | 36,028,797,018,963,968                             |
| /72                  | 72,057,594,037,927,936                             |
| /71                  | 144,115,188,075,855,872                            |
| /70                  | 288,230,376,151,711,744                            |
| /69                  | 576,460,752,303,423,488                            |
| /68                  | 1,152,921,504,606,846,976                          |
| /67                  | 2,305,843,009,213,693,952                          |
| /66                  | 4,611,686,018,427,387,904                          |
| /65                  | 9,223,372,036,854,775,808                          |
| Residential – /64    | 18,446,744,073,709,551,616                         |
| /63                  | 36,893,488,147,419,103,232                         |
| /62                  | 73,786,976,294,838,206,464                         |
| /61                  | 147,573,952,589,676,412,928                        |
| /60                  | 295,147,905,179,352,825,856                        |
| /59                  | 590,295,810,358,705,651,712                        |
| /58                  | 1,180,591,620,717,411,303,424                      |
| /57                  | 2,361,183,241,434,822,606,848                      |
| /56                  | 4,722,366,482,869,645,213,696                      |
| /55                  | 9,444,732,965,739,290,427,392                      |
| /54                  | 18,889,465,931,478,580,854,784                     |
| /53                  | 37,778,931,862,957,161,709,568                     |
| /52                  | 75,557,863,725,914,323,419,136                     |
| /51                  | 151,115,727,451,828,646,838,272                    |
| /50                  | 302,231,454,903,657,293,676,544                    |
| /49                  | 604,462,909,807,314,587,353,088                    |
| Business – /48       | 1,208,925,819,614,629,174,706,176                  |
| /47                  | 2,417,851,639,229,258,349,412,352                  |
| /46                  | 4,835,703,278,458,516,698,824,704                  |
| /45                  | 9,671,406,556,917,033,397,649,408                  |
| /44                  | 19,342,813,113,834,066,795,298,816                 |
| /43                  | 38,685,626,227,668,133,590,597,632                 |
| /42                  | 77,371,252,455,336,267,181,195,264                 |
| /41                  | 154,742,504,910,672,534,362,390,528                |
| /40                  | 309,485,009,821,345,068,724,781,056                |
| /39                  | 618,970,019,642,690,137,449,562,112                |
| /38                  | 1,237,940,039,285,380,274,899,124,224              |
| /37                  | 2,475,880,078,570,760,549,798,248,448              |
| /36                  | 4,951,760,157,141,521,099,596,496,896              |
| /35                  | 9,903,520,314,283,042,199,192,993,792              |
| /34                  | 19,807,040,628,566,084,398,385,987,584             |
| /33                  | 39,614,081,257,132,168,796,771,975,168             |
| ISP – /32            | 79,228,162,514,264,337,593,543,950,336             |
| /31                  | 158,456,325,028,528,675,187,087,900,672            |
| /30                  | 316,912,650,057,057,350,374,175,801,344            |
| /29                  | 633,825,300,114,114,700,748,351,602,688            |
| /28                  | 1,267,650,600,228,229,401,496,703,205,376          |
| /27                  | 2,535,301,200,456,458,802,993,406,410,752          |
| /26                  | 5,070,602,400,912,917,605,986,812,821,504          |
| /25                  | 10,141,204,801,825,835,211,973,625,643,008         |
| /24                  | 20,282,409,603,651,670,423,947,251,286,016         |
| /23                  | 40,564,819,207,303,340,847,894,502,572,032         |
| /22                  | 81,129,638,414,606,681,695,789,005,144,064         |
| /21                  | 162,259,276,829,213,363,391,578,010,288,128        |
| /20                  | 324,518,553,658,426,726,783,156,020,576,256        |
| /19                  | 649,037,107,316,853,453,566,312,041,152,512        |
| /18                  | 1,298,074,214,633,706,907,132,624,082,305,024      |
| /17                  | 2,596,148,429,267,413,814,265,248,164,610,048      |
| /16                  | 5,192,296,858,534,827,628,530,496,329,220,096      |
| /15                  | 10,384,593,717,069,655,257,060,992,658,440,192     |
| /14                  | 20,769,187,434,139,310,514,121,985,316,880,384     |
| /13                  | 41,538,374,868,278,621,028,243,970,633,760,768     |
| /12                  | 83,076,749,736,557,242,056,487,941,267,521,536     |
| /11                  | 166,153,499,473,114,484,112,975,882,535,043,072    |
| /10                  | 332,306,998,946,228,968,225,951,765,070,086,144    |
| /9                   | 664,613,997,892,457,936,451,903,530,140,172,288    |
| /8                   | 1,329,227,995,784,915,872,903,807,060,280,344,576  |


## Example allocations

```/64``` IPv6 allocations are usually given to end users, who do not require any VLANs. It allows auto configuration, or SLAAC so makes life a lot easier when configuring.

```bash
2402:9400:1000:0::/64
2402:9400:1000:1::/64
2402:9400:1000:2::/64
2402:9400:1000:3::/64
2402:9400:1000:4::/64
2402:9400:1000:5::/64
2402:9400:1000:6::/64
2402:9400:1000:7::/64
2402:9400:1000:8::/64
2402:9400:1000:9::/64
2402:9400:1000:a::/64
2402:9400:1000:b::/64
2402:9400:1000:c::/64
2402:9400:1000:e::/64
2402:9400:1000:e::/64
2402:9400:1000:f::/64
2402:9400:1000:10::/64
2402:9400:1000:11::/64
```

```/48``` allocations are usually provided to business, who require additional VLANs or may require the range to be split up.  Using a ```/48``` allocation would allow them to do so.

```bash
2402:9400:10::/48
2402:9400:11::/48
2402:9400:12::/48
2402:9400:13::/48
2402:9400:14::/48
2402:9400:15::/48
2402:9400:16::/48
2402:9400:17::/48
2402:9400:18::/48
2402:9400:19::/48
2402:9400:1a::/48
2402:9400:1b::/48
2402:9400:1c::/48
2402:9400:1e::/48
2402:9400:1f::/48
2402:9400:20::/48
```