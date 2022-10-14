# Adding Clients
## Adding ATC Clients
Euroscope and VRC will add ATC Clients (Even Observers) as shown \
`$AA{Callsign}:SERVER:{Full Name}:{Network ID}:{Password}:{Rating?}:{Protocol Version}`

| Element       | Description                   |
| -------       | -----------                   |
| $AA           | Command: Add ATC Client       |
| {Callsign}    | From: Callsign of the Client  |
| SERVER        | To: 'SERVER'                  |
| {Full Name}   | Full Name of the Controller   |
| {Network ID}  | CID                           |
| {Password}    | Password                      |
| {Rating?}     | Int from 1-12, Possibly Rating|
| {Protocol Version} | Protocol Version         |

## Adding Pilot Clients
vPilot, xPilot, and Swift add clients a similar way \
`$AP{Callsign}:SERVER:{Network ID}:{Password}:{Pilot Rating?}:{Protocol Version}:{Unknown}:{Full Name ICAO}`

| Element           | Description                       |
| -------           | -----------                       |
| $AP               | Command: Add Pilot Client         |
| {Callsign}        | From: Callsign of the Client      |
| SERVER            | To: 'SERVER'                      |
| {Network ID}      | CID                               |
| {Password}        | Password                          |
| {Pilot Rating?}   | Int from 1-12, Possibly Rating    |
| {Protocol Version}| Protocol Version                  |
| {Unknown}         | Unknown                           |
| {Full Name ICAO}  | Full Name of the Pilot + Home apt |


## Footnote
It appears that `#AA` and `#AP` go to every connected client \
For our application, we would call an `#AA` function for every controller within a scenario and `#AP` for every pilot within a scenario. 