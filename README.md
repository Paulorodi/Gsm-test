# After Uploading the Code

##  Power Everything Properly

For SIM800L:

 
* Insert SIM card
* Ensure SIM has:

  * airtime ama sms
  * no PIN lock

---

#  What You Will See on LCD

## First Screen

```text id="4dc7pk"
Starting...
```

This means Arduino has started.

Wait about 5 seconds.

---

## Second Screen

```text id="m6uwpz"
Testing GSM
```

Arduino is checking whether SIM800L responds.

---

# Check SIM800L LED

Very important.

## Fast blinking every 1 second

```text id="t4gx2q"
Not connected to network yet
```

Wait longer.

OR:

* weak signal
* SIM issue
* insufficient power

---

## Slow blinking every 3 seconds 

```text id="x59e0y"
Connected to network
```

Now SMS can work.

---

#  If Everything Works

LCD changes to:

```text id="jlwmzr"
GSM Connected
```

Then:

```text id="u6u1ru"
Checking Net
```

Then:

```text id="jlwmnq"
Network Ready
Signal OK
```

Then:

```text id="hdbn1v"
Sending SMS
```

Finally:

```text id="e8pj8w"
SMS Sent
```

Then:

```text id="93qq6g"
Waiting SMS
```

---

#  Check Your Phone

You should receive:

```text id="93qz7d"
Hello from SIM800L Arduino Test
```

If received → project works correctly 

---

#  Open Serial Monitor

In Arduino IDE:

## Set:

```text id="w0p3g5"
Baud Rate = 9600
```

and:

```text id="v7xlj6"
Both NL & CR
```

You will see debugging info like:

```text id="r4xv72"
Starting SIM800L Test
Testing GSM Module
OK
GSM Connected Successfully
Sending SMS...
SMS SENT SUCCESSFULLY
```

---

#  How to Receive SMS

Send a message from your phone to the SIM card inside SIM800L.

LCD will show:

```text id="7tm9ml"
New SMS
```

Then back to:

```text id="g8h7l5"
Waiting SMS
```

Meanwhile Serial Monitor displays the actual message:

```text id="l5fnyo"
+CMT: "+254712345678"
Hello Arduino
```

---

#  How to Send AT Commands Manually

Type commands in Serial Monitor.

Example:

## Test module

```text id="rt6fyt"
AT
```

Reply:

```text id="n6m7l0"
OK
```

---

## Check signal

```text id="1cjlwm"
AT+CSQ
```

Example reply:

```text id="qorv9n"
+CSQ: 20,0
```

Signal guide:

| Value | Meaning   |
| ----- | --------- |
| 5–10  | Weak      |
| 15–20 | Good      |
| 20+   | Excellent |

---

## Check network registration

```text id="u3ofl6"
AT+CREG?
```

Good replies:

```text id="gdu0j6"
+CREG: 0,1
```

or

```text id="l70p86"
+CREG: 0,5
```

---








```Osama replcae my number with yours/common phone number at gsm block ensure you have screen```
