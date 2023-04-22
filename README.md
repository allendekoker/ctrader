# Tokyo Session Strategy

This is a cTrader robot written in C# that implements a basic trading strategy for the Tokyo trading session.

## Overview

The Tokyo Session Strategy opens a long position at the start of the Tokyo trading session and holds the position until the end of the session. The robot will not open any positions outside of the specified time range.

## Parameters

The robot has three parameters that can be adjusted to suit your trading preferences:

- Lot Size: the size of the position to open, in lots (default value is 2.0)
- Stop Loss (pips): the distance from the entry price to set the stop loss level, in pips (default value is 450)
- Take Profit (pips): the distance from the entry price to set the take profit level, in pips (default value is 500)

## Trading Logic

The robot's trading logic is as follows:

1. Check if the current time is within the specified trading time range (2:00 AM to 6:45 PM UTC).
2. Calculate the stop loss and take profit levels based on the specified distance in pips.
3. Calculate the position size based on the lot size and account balance.
4. Place a long order with the calculated stop loss, take profit, and position size.

If the order is executed successfully, the robot will print a message to the console with the entry price, stop loss, and take profit levels. If the order fails, the robot will print an error message to the console.

## Usage

To use the Tokyo Session Strategy, follow these steps:

1. Open the cTrader platform.
2. Create a new cBot and copy the code into the editor.
3. Set the parameters to your preferred values.
4. Compile and run the robot.
5. Monitor the console output for updates on the status of the open position.

Note: This strategy is intended as an educational example and should not be used for live trading without first testing it thoroughly on a demo account.
