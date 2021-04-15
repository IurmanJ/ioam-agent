# IOAM Agent for Python3

Note: specific ioam-agent for [CLT](https://github.com/IurmanJ/cross-layer-telemetry).

1) Install dependencies:
```
pip3 install bitstruct grpcio grpcio-tools
```

2) Compile the proto3 [IOAM Trace API](https://github.com/IurmanJ/ioam-proto3):
```[bash]
git clone https://github.com/IurmanJ/ioam-proto3.git
python3 -m grpc_tools.protoc -Iioam-proto3/ --python_out=. --grpc_python_out=. ioam-proto3/ioam_trace.proto
```

3) Run it:
```[bash]
sudo python3 ioam-agent.py -i <interface> [-o]
```

### Output Mode

Use `-o`.

This mode will print IOAM traces in the console.

### Report Mode

Default mode.

This mode will report IOAM traces to a collector via grpc. **The collector must be defined as an environment variable**:
```[bash]
IOAM_COLLECTOR=address:port
```
