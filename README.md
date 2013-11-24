androPlanePIDfloats
===================

An Android app implemented as an Activity for testing PID control implementation.

The purpose is to test the implementation intended for integration with the IOIO library.

Uses GPS to determine waypoint locations and cross track error (CTE). 
The CTE is an angle which a difference between current heading (read from orientation matrix 
that uses both accelerometers and magnetometers) and the bearing to the next waypoint.

The control output is a bank angle (-30 to 30 deg).
The control output is shown in a text field.
Uses a separate thread for PID control.
Processes events sent to onLocationChanged and onSensorChanged in dedicated threads.
Uses weighted running average to smooth out sensor readings.
Uses float type for parameters, converts results of Math class methods to float from double.

