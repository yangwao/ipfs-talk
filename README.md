# IPFS: Cat From Mars

![](cat_from_mars.jpg)

### Before start
#### Deploy IPFS locally
https://github.com/ipfs/go-ipfs/#build-from-source
```
ipfs init
ipfs daemon
```
your daemon is running and you will see output like this
```
wao@astrid~> ipfs daemon
Initializing daemon...
Swarm listening on /ip4/127.0.0.1/tcp/4001
Swarm listening on /ip4/192.168.223.118/tcp/4001
Swarm listening on /ip6/::1/tcp/4001
API server listening on /ip4/127.0.0.1/tcp/5001
Gateway (writable) server listening on /ip4/127.0.0.1/tcp/8080
Daemon is ready
```
#### Chrome extension
https://chrome.google.com/webstore/detail/ipfs-station/kckhgoigikkadogfdiojcblegfhdnjei
https://github.com/xicombd/ipfs-chrome-station

### Let begin talk

Print IPFS 'whoami'

```
ipfs id
```

IPFS who I'm connected do

```
ipfs swarm peers
```

List IPFS peers propagated addresses - great for debugging

```
ipfs swarm addrs
```

Fetch some file from me and play 8-bit music!

```
ipfs cat /ipfs/QmZNcmfFptDCRMtuTgpVsjW4Ntq5874N99K1EhYsacVfYS > 4344493_8_Bit_Adventure-52693751.mp3
afplay 4344493_8_Bit_Adventure-52693751.mp3
```

How I did that
```
ipfs add 4344493_8_Bit_Adventure-52693751.mp3
```

And you have shiny running daemon, open in browser
http://localhost:5001/webui/

Continue with Tour feature
```
ipfs tour
ipfs tour --help
```

And you can run your own static site on IPFS, like I do http://hackerdome.xyz

This trick is using old-school DNS with TXT record in it, it's feature of ipfs gateway to keep touch with non-modern world.
IPFS will fetch TXT record with hash of ipfs object and fetch it from IPFS network and will server it to your browser

```
wao@astrid~> dig +short hackerdome.xyz
104.236.76.40
104.236.179.241
128.199.219.111
104.236.176.52
162.243.248.213
104.236.151.122
178.62.61.185
178.62.158.247
wao@astrid~> dig +short -t TXT hackerdome.xyz
"dnslink=/ipfs/QmRFfsLBwVbCcWiguFeB6QXbjABbvefxA1Uu7axRrfGbuX"
```


Now sit and watch video from Juan Benet at Standford about IPFS, learn what are distributed networks  
https://www.youtube.com/watch?v=HUVmypx9HGI
