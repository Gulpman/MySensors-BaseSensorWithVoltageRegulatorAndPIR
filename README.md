# MySensors-BaseSensorWithVoltageRegulatorAndPIR
A battery powerd (CR123A) basic sensor with onboard PIR mounting and voltage regulator to 3.3V

This is my first own eagle project.

<h1>What's on the sensor?</h1>
<ul>
<li>ATMega 328P-AU</li>
<li>NRF24L01+ SMD version</li>
<li>AT25DF512C-SSHN-B EEPROM (512k) (optional)</li>
<li>ATSHA204A (optional)</li>
<li>PIR Sensor 3.3V (optional)</li>
<li>MAX1724+ (optional - if you do not want to use it shorten jumper SJ2)</li>
<li>I2C header with Pullups</li>
<li>FTDI header</li>
<li>ISP header</li>
<li>CR123A battery holder</li>
<li>The following pins can be used via pin headers</li>
    <ul>
        <li>A1 to A2</li>
        <li>D3 to D6</li>
    </ul>
</ul>

Jumper SJ1 is useless at the moment - the idea behind it is that, dependent on the battery level the SHDN pin of the MAX 1724 could be set to low or high by the sketch running on the 328P. Help and hints for implementing this are highly appreciated. :)

The PCB is meant to fit into an ABS82 case. The ABS-82 is for example available at TME -> <a href="http://www.tme.eu/de/details/abs-82/universal-gehaeuse/">ABS-82 @ TME</a>. 

Big kudos go to Omega-5 from forum.fhem.org who had an eye on my first steps in the Eagle world and who is responsible at least for a few of the capacitors and their position very close to the 328P :)
I think I can admit that this sensor would have had no chance to function without him having a look on my files.

After the sensor has proven that it is functioning the next version will have the following improvements:
<ul>
<li>Smaller - PIR sensor will not be mounted onboard. Makes it cheaper to produce as well as more flexible.</li>
<li>Implementation of SJ1 - allow the sketch to shutdown the MAX 1724 if voltage of the battery is high enough.</li>
<li>Optional pullups for digital and anolog pins</li>
</ul>
