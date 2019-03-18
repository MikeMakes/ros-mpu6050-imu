# ros-mpu6050-imu
A ros package (not everything tested, not yet finished) that reads imu mpu6050 mesurements via i2c bus of a raspberry pi.

It uses the lib smbus [someday here will be a link] which only have read_byte and write_byte, so I wrote i2cbus.py which handle i2c bus and others read&write functions.
In mpu6050.py there is the stuff that only is related to the imu and not the i2c bus; registers, measurements, modes...
As an example look at talker.py, which publish in the topics /imu1_rawImu and /imu1_scaledImu the measurements. 
