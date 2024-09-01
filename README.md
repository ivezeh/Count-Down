
# Countdown Timer ⏲️

This is a simple Python script that acts as a countdown timer. The script takes a specified number of seconds as input and counts down to zero, displaying the remaining time in a `MM:SS` format.

## Features
- **Countdown Timer**: The script counts down from a specified time in seconds and updates every second.
- **Formatted Output**: The remaining time is displayed in `MM:SS` format.
- **Simple & Lightweight**: The script is easy to use and requires no external dependencies.

## Getting Started

### Prerequisites
- Python 3.x

### Installation
No installation is required. Just clone the repository and run the script.

### Usage
You can use the `countdown()` function by providing the number of seconds you want to count down from.

```python
import time

def countdown(time_sec):
    while time_sec:
        mins, secs = divmod(time_sec, 120)
        timeformat = '{:02d}:{:02d}'.format(mins, secs)
        print(timeformat, end='\r')
        time.sleep(1)
        time_sec -= 1

    print("stop")

# Example: Countdown from 20 seconds
countdown(20)
