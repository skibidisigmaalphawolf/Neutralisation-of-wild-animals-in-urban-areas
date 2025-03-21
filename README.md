# Neutralisation-of-wild-animals-in-urban-areas
import RPi.GPIO as GPIO
import time

# Set up GPIO pins
PIR_SENSOR_PIN = x 
ALARM_PIN = x       

# GPIO setup
GPIO.setmode(GPIO.BOARD)
GPIO.setup(PIR_SENSOR_PIN, GPIO.IN)
GPIO.setup(ALARM_PIN, GPIO.OUT)

try:
    print("Starting the motion detector. Press S to stop.")
    while True:
        # Check for motion detection
        if GPIO.input(PIR_SENSOR_PIN):
            print("Motion detected! Alarm ON")
            GPIO.output(ALARM_PIN, GPIO.HIGH)  # Turn on the alarm
        else:
            print("No motion. Alarm OFF")
            GPIO.output(ALARM_PIN, GPIO.LOW)  # Turn off the alarm
        
        time.sleep(0.5)  # Delay for stability

except KeyboardInterrupt:
    print("Exiting the program.")
    GPIO.cleanup()  # Clean up GPIO settings

