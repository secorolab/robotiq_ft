# robotiq_ft

A C API to connect and read data from the Robotiq FT-300S sensor.

- The Driver code is from the [Robotiq Sensor Development Package](https://robotiq.com/support).

## Installation

To install the package, run the following command:

```bash
mkdir build && cd build

cmake .. -DCMAKE_BUILD_TYPE=Release

make -j$(nproc)
```

## Example

### Blocking

- This example will block until the sensor is connected and data is available.
- Even after connection, if it looses connection, it will block until it is reconnected.

```bash
./build/src/example/robotiq_ft_blocking_ex
```

### Non-blocking

- This example will try 5 times to connect to the sensor and exit if it fails.
- If it connects, it will read data from the sensor.

```bash
./build/src/example/robotiq_ft_non_blocking_ex
```
