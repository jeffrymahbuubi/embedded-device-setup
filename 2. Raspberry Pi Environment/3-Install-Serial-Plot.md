# Install `SerialPlot`

In order to install `SerialPlot` software, it need to build from source. Type following commands to compile the software to the RaspberryPi environment,

1. Download the `SerialPlot` from GitHub: `wget https://github.com/hyOzd/serialplot/archive/refs/tags/v0.13.0.zip`
2. Download the necessary library: `apt install qt6-base-dev qt6-serialport-dev qt6-svg-dev git cmake build-essential`
3. Build the software: 

   ```bash
   mkdir build
   cd build
	
   cmake ..

   make -j2
   ```

4. In order to open `SerialPlot` from any directory, we need to create a symbolic link with the software by typing following command: 

   - Get the `realpath` of the `serialplot` by typing command `realpath ./serialplot`
   - Create symbolic link by following command `sudo ln -s {realpath_dir} /usr/local/bin/serialplot`
   - Confirm link is correctly initialized by typing command `which serialplot` it should output the `/usr/local/bin/serialplot`
   - To run SerialPlot type command `serialplot`