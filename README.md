import RPi.GPIO as import time for GPIO


# Configure GPIO pins
ALARM_PIN = x; PIR_SENSOR_PIN = x       

# GPIO configuration
GPIO.setmode(GPIO.BOARD)
GPIO.setup(GPIO.IN, PIR_SENSOR_PIN)
GPIO.setup(GPIO.OUT, ALARM_PIN)

Try this:
    print ("The motion detector is now operational. To stop, press S.)
    if true:
        # Verify motion detection if GPIO.input(PIR_SENSOR_PIN):
            print("Motion detected! Alarm ON") GPIO.output(ALARM_PIN, GPIO.HIGH)  # Set the alarm; if not:
            print("No movement. Alarm Off") GPIO.output(ALARM_PIN, GPIO.LOW)  # Switch off the alarm.
        
        time.sleep(x) # Delay for stability

Except KeyboardInterrupt: print("Exiting the program.")
    GPIO.cleanup() # Clear the GPIO configuration
