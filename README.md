# homebridge-accessory-neurio
A [neur.io](http://neur.io) accessory plugin for [Homebridge](https://github.com/nfarina/homebridge).

# Installation
Run these commands:

    % sudo npm install -g homebridge
    % sudo npm install -g homebridge-accessory-neurio

On Linux, you might see this output for the second command:

    npm ERR! pcap@2.0.0 install: node-gyp rebuild
    npm ERR! Exit status 1
    npm ERR!

If so, please try

    % apt-get install libpcap-dev

and try

    % sudo npm install -g homebridge-accessory-neurio

again!

NB: If you install homebridge like this:

    sudo npm install -g --unsafe-perm homebridge

Then all subsequent installations must be like this:

    sudo npm install -g --unsafe-perm homebridge-accessory-neurio

# Configuration
Edit `~/.homebridge/config.json`, inside `"accessories": [ ... ]` add:

    { "accessory" : "neurio"
    , "name"      : "Home Energy Monitor"
    , "location"  : "a.b.c.d"

    // optional, here are the defaults
    , "options"   : { "ttl": 600, "verboseP" : false }

    // also optional, supply either both or neither
    , "username"  : "Aladdin"
    , "password"  : "OpenSesame"
    }

How can you determine the IP address (`"a.b.c.d"`)?
Run [homespun-discovery](https://github.com/homespun/homespun-discovery),
of course.
