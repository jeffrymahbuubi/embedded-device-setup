# Jetson Nano Virtual Environment Setup

## Setup Command

- The most important things when creating a `venv` is to use `--system-site-packages` since all virtual environment should inherit from the main system packages. Following is how to correctly virtual environment in Jetson Nano, 

```bash
pip3 install virtualenv
python3 -m virtualenv -p python3 env --system-site-packages
```

- Change the `env` to other name of virtual environment, e.g., `venv`
- To activate virtual environment, use this command `source env/bin/activate`