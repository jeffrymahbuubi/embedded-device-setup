# Jetson Nano Graphic User Interface Setup

## Example Code

- Create a new file called `test-GUI.py` and do following `gedit test-GUI.py` to write testing code for ensuring `PyQt5` environment setup properly:  

```bash
import sys
from PyQt5.QtWidgets import QApplication, QLabel

app = QApplication(sys.argv)
label = QLabel("Hello, PyQt5!")
label.show()
sys.exit(app.exec_())
```

- If `PyQt5` is installed correctly running `python test-GUI.py` should open simple GUI

## Setup Command

- Install `PyQt5` environment by following: `sudo apt-get install qt5-default`



