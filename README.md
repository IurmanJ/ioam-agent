# IOAM Agent

```[bash]
python3 ioam-agent.py -i <interface> [-o]
```

The IOAM Agent can be run in two different modes: output or report.

### Output Mode

Use `-o`.

This mode will print IOAM traces in the console.

### Report Mode

Default mode.

This mode will report IOAM traces to a collector via grpc, based on the [IOAM Trace API](https://github.com/IurmanJ/ioam-proto3).

The collector must be defined as an environment variable:
```[bash]
IOAM_COLLECTOR=address:port
```
