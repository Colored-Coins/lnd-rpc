# lnrpc

Tiny wrapper around the [gRPC library](https://github.com/grpc/grpc/tree/master/src/node/src)
for the [lnd](https://github.com/lightningnetwork/lnd) RPC API.

### Install

`grpc` is configured as a peerDependency and must be installed alongside this library:

    npm install --save grpc lnrpc

### Use

    const lnrpc = require('lnrpc')
        , grpc = require('grpc')
        , client = new lnrpc.Lightning('localhost:10009', grpc.credentials.createInsecure())

    client.getInfo(new lnrpc.GetInfoRequest(), (err, info) => ...)

### License

https://github.com/Colu-platform/colu-nodejs/blob/master/LICENSE
