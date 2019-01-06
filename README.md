# pfs
Flight software for Project Caelus, written in Python.

## Development


## Structure
- *main.py*
    - The file that is run
    - Use `python3 main.py`
    - Loops through submodules defined in *config.yml*
    - Starts the submodules
- *config.yml*
    - Configuration on what to run
    - Contains submodule-level parameters
- *modules/*
    - Each submodule has a `start()` function
    - *telemetry.py*
        - `enqueue()`
        - `send()`
        - `receive()`
    - *external.py*
        - Get methods for all sensors
        - Set methods for RCS and EDF (motors)
    - *tvc.py*
        - Calls get methods in *external.py*
        - Processing of sensor data and responding accordingly
        