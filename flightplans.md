# Flight plans
All flight plans follow the 
[FAA domestic Flight plan format](https://www.faa.gov/documentLibrary/media/Form/FAA_Form_7233-1_7_31_17.pdf) and are requested as shown \
`$FP(callsign):*A:(VFR/IFR):(acft type):(spd):(origin):(sched dep):(alt):(dest):(EET):(FOB):(alt airport):(remarks)`

| Element       | Description                   |
| -------       | -----------                   |
| $FP           | Command: Flight Plan          |
| {callsign}    | From: Callsign of the Client  |
| *A            | Unknown Function              |
| {VFR/IFR}     | Flight Plan Type              |
| {acft type}   | Aircraft Type                 |
| {spd}         | Speed                         |
| {origin}      | Origin Airport                |
| {sched dep}   | Scheduled Departure Time      |
| {alt}         | Altitude                      |
| {dest}        | Destination Airport           |
| {EET}         | Estimated Enroute Time        |
| {FOB}         | Fuel on Board                 |
| {alt airport} | Alternate Airport             |
| {remarks}     | Remarks                       |

## Acknowledgement
The acknowledgement is sent as shown \
`#TM(own callsign):FP:(flightplan callsign) GET`

And the server will reply\
`#PCserver:(own callsign):CCP:BC:(flightplan callsign):0`

## Modifying Flight Plans
Flight plans can be modified by sending the following \
`$AM(callsign):SERVER:(fplan callsign):(VFR/IFR):(acft type):(spd):(origin):(sched dep):(alt):(dest):(EET):(FOB):(alt airport):(remarks)`

| Element           | Description                   |
| -------           | -----------                   |
| $AM               | Command: Modify Flight Plan   |
| {callsign}        | From: Callsign of the Client  |
| SERVER            | To: 'SERVER'                  |
| {fplan callsign}  | Flight Plan Callsign          |
| {VFR/IFR}         | Flight Plan Type              |
| {acft type}       | Aircraft Type                 |
| {spd}             | Speed                         |
| {origin}          | Origin Airport                |
| {sched dep}       | Scheduled Departure Time      |
| {alt}             | Altitude                      |
| {dest}            | Destination Airport           |
| {EET}             | Estimated Enroute Time        |
| {FOB}             | Fuel on Board                 |
| {alt airport}     | Alternate Airport             |
| {remarks}         | Remarks                       |