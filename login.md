# Prelogin
When a Client opens a TCP Connection on port 6809, the server is expected to identify itself like this: \
\
`$DISERVER:CLIENT:VATSIM FSD {Version}:{token}` 

<table>
    <tr>
        <th>Element</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>$DISERVER</td>
        <td>Command: Server Identify <br> From: 'SERVER'</td>
    </tr>
    <tr>
        <td>CLIENT</td>
        <td>To: 'CLIENT'</td>
    </tr>
    <tr>
        <td>VATSIM FSD {Version}</td>
        <td>Server Version</td>
    </tr>
    <tr>
        <td>{token}</td>
        <td>22-character hexadecimal string that changes on every login. Can be static for our purposes.</td>
    </tr>
</table>

The Client Must respond with \
`$ID{Callsign}:SERVER:{client id}:{client string}:3:2:{network ID}:{num}`
<table>
    <tr>
        <th>Element</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>$ID</td>
        <td>Command: Client Identify</td>
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
        <td>{client id}</td>
        <td>4 Character String; See Below</td>
    </tr>
    <tr>
        <td>{client string}</td>
        <td>Human Readable String</td>
    </tr>
    <tr>
        <td>3</td>
        <td>Protocol Version</td>
    </tr>
    <tr>
        <td>2</td>
        <td>Protocol Revision</td>
    </tr>
    <tr>
        <td>{network ID}</td>
        <td>CID</td>
    </tr>
    <tr>
        <td>{num}</td>
        <td>Signed 9 Digit Int</td>
    </tr>
</table>

## Client Codes 
<table>
    <tr>
        <th>Code</th>
        <th>Client</th>
    </tr>
    <tr>
        <td>de1e</td>
        <td>VRC</td>
    </tr>
    <tr>
        <td>69d7</td>
        <td>EuroScope 3.2</td>
    </tr>
    <tr>
        <td>48e2</td>
        <td>Swift</td>
    </tr>
    <tr>
        <td>8834</td>
        <td>vPilot</td>
    </tr>
</table>

Once that handshake is complete, The client will
[add a client.](addclient.md)
