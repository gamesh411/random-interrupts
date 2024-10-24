# Random Interrupt Helper - Usage Guide

## Basic Usage

The Random Interrupt Helper is a command-line tool that generates random interrupts over a specified time period, inspired by Andrew Huberman's research on productivity and focus. Here's how to use it:

1. Open a terminal or command prompt.
2. Navigate to the project directory.
3. Run the script with the required arguments:

```
python src/random_interrupt/main.py --overall-time <minutes> --number-of-interrupts <count> [--min-gap <minutes>] [--notification-title <title>] [--notification-message <message>] [--notification-timeout <seconds>]
```

## Arguments

- `--overall-time`: (Required) The total time period in minutes for which you want to generate interrupts.
- `--number-of-interrupts`: (Required) The total number of interrupts to generate.
- `--min-gap`: (Optional) The minimum time between interrupts in minutes.
- `--notification-title`: (Optional) Title for the notification (default: "Random Interrupt").
- `--notification-message`: (Optional) Message for the notification (default: "Time for a break!").
- `--notification-timeout`: (Optional) Notification timeout in seconds (default: 10).

## Examples

1. Generate 5 interrupts over a 60-minute period:
   ```
   python src/random_interrupt/main.py --overall-time 60 --number-of-interrupts 5
   ```

2. Generate 10 interrupts over a 2-hour period with a minimum gap of 5 minutes:
   ```
   python src/random_interrupt/main.py --overall-time 120 --number-of-interrupts 10 --min-gap 5
   ```

3. Generate 5 interrupts over a 60-minute period with custom notification settings:
   ```
   python src/random_interrupt/main.py --overall-time 60 --number-of-interrupts 5 --notification-title "Focus Break" --notification-message "Take a deep breath" --notification-timeout 15
   ```

4. Combine all optional parameters:
   ```
   python src/random_interrupt/main.py --overall-time 90 --number-of-interrupts 6 --min-gap 10 --notification-title "Productivity Boost" --notification-message "Stand up and stretch!" --notification-timeout 20
   ```

## Behaviour

- The script will generate random interrupt times based on your input.
- It will print the generated interrupt times to the console.
- At each interrupt time, a desktop notification will be displayed with the specified title, message, and timeout duration.
- The script will run for the entire duration specified by `--overall-time`.

## Tips

- Use this tool to implement random break schedules in your work routine.
- Experiment with different settings to find what works best for your focus and productivity.
- Customize notification messages to include specific actions or reminders.
- Adjust the notification timeout to ensure you have enough time to read and act on the message.
- Remember that this tool is inspired by Andrew Huberman's research on optimizing focus and productivity throughout the day.

For more information on the science behind this approach, visit [Huberman Lab](https://hubermanlab.com/).
