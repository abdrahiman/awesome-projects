# ⭐ Goal

Create a tool that measures and reports internet connection speed. Your solution should test both download and upload speeds, and provide accurate results in a user-friendly format. This project can be implemented as a web application, mobile app, command-line interface (CLI), or any other method you prefer.

## 🚨 Requirements

1. Measure download speed in Mbps (Megabits per second)
2. Measure upload speed in Mbps
3. Calculate and display latency (ping) in milliseconds
4. Present results in a clear, easy-to-understand format
5. Ensure accuracy of measurements
6. Handle errors gracefully (e.g., no internet connection)

## 💼 Usage

### Input

- User initiates the speed test through your chosen interface (button click, command, etc.)

### Output

- Download speed: X.XX Mbps
- Upload speed: X.XX Mbps
- Latency: XX ms
- (Optional) Historical data or comparison to average speeds in the user's area

Example output (CLI):

```bash
$ speedtest run
Running speed test...
Download: 75.42 Mbps
Upload: 15.23 Mbps
Latency: 28 ms
```

## 🧪 Testing

- Run your speed test tool multiple times and compare results with known reliable speed test services
- Test on different network conditions (fast/slow connections, wired/wireless)
- Verify that the tool handles poor or no internet connectivity gracefully
- If applicable, test on different devices or browsers to ensure consistent functionality

## 🍥 Bonus

- Implement a graphical representation of speed over time
- Add the ability to schedule regular tests and store historical data
- Create a shareable report of speed test results
- Implement network diagnostics to identify potential issues affecting speed
- Add a feature to test speed to specific servers or locations
