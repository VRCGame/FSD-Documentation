# Adding Clients
## Adding ATC Clients
Euroscope and VRC will add ATC Clients (Even Observers) as shown \
`$AA{Callsign}:SERVER:{Full Name}:{Network ID}:{Password}:{Rating?}:{Protocol Version}`
<table>
    <tr>
        <th>Element</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>$AA</td>
        <td>Command: Add ATC Client</td>
    </tr>
    <tr>
        <td>{Callsign}</td>
        <td>From: Callsign of the Client</td>
    </tr>
    <tr>
        <td>SERVER</td>
        <td>To: 'SERVER'</td>
    </tr>
    <tr>
        <td>{Full Name}</td>
        <td>Full Name of the Controller</td>
    </tr>
    <tr>
        <td>{Network ID}</td>
        <td>VID/CID</td>
    </tr>
    <tr>
        <td>{Password}</td>
        <td>Password for the CID/VID</td>
    </tr>
    <tr>
        <td>{Rating?}</td>
        <td>Possibly ATC Rating, Unsure of real meaning</td>
    </tr>
    <tr>
        <td>{Protocol Version}</td>
        <td>Protocol Version</td>
    </tr>
</table>

## Adding Pilot Clients
vPilot, xPilot, and Swift add clients a similar way \
`$AP{Callsign}:SERVER:{Network ID}:{Password}:{Pilot Rating?}:{Protocol Version}:{Unknown}:{Full Name ICAO}`

<table>
    <tr>
        <th>Element</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>$AP</td>
        <td>Command: Add Pilot Client</td>
    </tr>
    <tr>
        <td>{Callsign}</td>
        <td>From: Callsign of the Client</td>
    </tr>
    <tr>
        <td>SERVER</td>
        <td>To: 'SERVER'</td>
    </tr>
    <tr>
        <td>{Network ID}</td>
        <td>VID/CID</td>
    </tr>
    <tr>
        <td>{Password}</td>
        <td>Password for the CID/VID</td>
    </tr>
    <tr>
        <td>{Pilot Rating?}</td>
        <td>Possibly Pilot Rating, unsure</td>
    </tr>
    <tr>
        <td>{Protocol Version}</td>
        <td>Protocol Version</td>
    </tr>
    <tr>
        <td>{Unknown}</td>
        <td>Unknown what this value does</td>
    </tr>
    <tr>
        <td>{Full Name ICAO}</td>
        <td>Full Name of the Pilot + Home Airport</td>
</table>