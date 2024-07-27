# Raspberry Pi Surveillance Robotic Car

A simple project to create a web-controlled surveillance robotic car using a Raspberry Pi and a webcam.

## Features

- Live video streaming
- Web-based control for movement

## Components

- Raspberry Pi
- USB Webcam
- DC Motors and Robot chassis
- L293D Motor Driver IC
- Power bank

## Setup Instructions

### Raspberry Pi Setup

1. **Update Raspbian OS:**
    ```bash
    sudo apt-get update
    ```

2. **Install Flask:**
    ```bash
    pip install Flask
    ```

### Motion Setup

1. **Install Motion:**
    ```bash
    sudo apt-get install motion
    ```

2. **Enable Motion Daemon:**
    ```bash
    sudo nano /etc/default/motion
    ```
    Set `start_motion_daemon=yes`

3. **Set Permissions:**
    ```bash
    sudo chown motion:motion /var/lib/motion/
    ```

4. **Configure Motion:**
    ```bash
    sudo nano /etc/motion/motion.conf
    ```
    Set `stream_localhost off`

5. **Start Motion Service:**
    ```bash
    sudo /etc/init.d/motion restart
    ```

### Flask Setup

1. **Create HTML File:**
    Save the following HTML code as `templates/robot.html`:



2. **Create Python Code:**
    Save the following Python code as `robot.py`:

  

## Usage

1. Run the Python script:
    ```bash
    python robot.py
    ```

2. Open a web browser and go to:
    ```
    http://YOUR_RPI_IP:5010
    ```

3. Use the web interface to control the robot.

## License

This project is licensed under the MIT License.
