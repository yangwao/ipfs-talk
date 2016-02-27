# ipfs cat from mars

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

Now sit and watch video from Juan Benet at Standford about IPFS, learn what are distributed networks  
https://www.youtube.com/watch?v=HUVmypx9HGI
