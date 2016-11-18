# SparkFun_BME280

This is basically 
SparkFunBME280 
BME280 Arduino library made by
Marshall Taylor @ SparkFun Electronics
May 20, 2015
https://github.com/sparkfun/BME280_Breakout

Changes in this fork by Vladimir Blanshey Nov. 2016:

- Chip Configuration setup is done in BME280::begin()
to apply I2C interface and to set the highest oversampling rate (16x for pressure reading and 2x for temperature)
for the atmospheric pressure measurement for avionics application.

- Wire.begin() has been removed to be included in the user setup() code
as it is also used by other libraries and also general approach should be not to initialize neither instantiate one library inside another library.

- Coefficient to convert pressure into altitude in readFloatAltitudeMeters() changed to 44330.0
to better match the satelite data
