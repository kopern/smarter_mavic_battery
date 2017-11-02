# smarter_mavic_battery

The target of this project is to create a better Mavic battery, which will be licenced as open source.

The imprevements will be:

1. We will use a higher density battery than the ones used by the Mavic battery:

	The original Mavic battery is using LI-ION Polimer cells with a weight for 202grams and provide 43.6 Watts of power. This translates into 215Watts/kg. I was able to fly 15km with this kind of battery and still have 12% energy left)
	LG 18650HG2 battery has 11.5Watts in 48grams which translates to 240Watts/kg, which is 11.5% improvement in capacity for the same weight (16.72km range should be achievable)
	NCR18650GA battery has 11.9 Watts in 48grams which translates to 247Watts/kg, which is 14.8% improvement in capacity for the same weight (17.22km range expected)
	300Watt/kg batteries are expected to be soon avaialble. These would result in 39.5% improvement therefore we should be able to fly 20.9km)
	
	Technical considerations:
	
	Due to the low voltage of the LG HG2 / NCR GA batteries, we cannot use 3 batteries in series. Logical would be to try to use 4 batteries in series but at the moment I am not sure if Mavic can work properly with the high voltage provided by these batteries while fully charged. My intention is to use a DC/DC switching converter to keep the voltage in the parameters of the original batteries.
	This will offer us the possibility of using 5 or 6 batteries as well to increase the flight time, although the weight will be increased.
	I expect to test a 4x2 battery configuration as well in order to provide a backup should one of the battery chain fail during mid flight but this will increase the weight of the drone considerably (184 grams).
	We could also look into using 3x2 battery chain but we need to provide a step-up converter in order to keep the drone flying for the whole voltage range of the battery.
	
2. I intend to add at a later date a gps tracker. We will use this tracker to transmit the GPS position of the Mavic drone in order to be able to recover it should it fly away for any reason.
As a technical solution I find inconvenient the GSM transmitter due to the requirement of 3rd party services and GPRS subscription. My intention is to build from ground uo a tracker which uses LORA technology instead of GSM. 
The chip that I inted to use is SX1276. This chip is able to transmit data up to 48km line of sight, without the need of a GSM transmitter or GSM network. 

3. All hardware and software will be open source therefore the cost of this battery will be considerably lower than the original battery.

Note:  My time is currently limited and I am not sure if I will be able to complete this project alone. I am happy to accept contributions to this project.
