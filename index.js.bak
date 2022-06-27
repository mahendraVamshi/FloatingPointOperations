function fun(src)
{
    window.scrollTo(0, 0);
    content=document.getElementById("content").innerHTML;
    loc="http://127.0.0.1:5500/main.htm"
    if (src==1){
        
        content=`
        <div id="mainheading">Floating point numbers</div><hr style="width:75%"/>
		
		
        <ol id="index">
            <li><a href="#riscv">RISC V</a></li>
            <li><a href="#eclass">E class processors</a></li>
            <li><a href="#earty">E-arty35T</a></li>
            <li><a href="#axi">AXI</a></li>
        </ol>
        <div style="font-size:25px;" id='riscv' > 
        RISC V
        </div><p><div id='info'><hr style='width:50%'/>
        &emsp;&emsp;&emsp;&emsp; SHAKTI is an open-source initiative led by the Reconfigurable Intelligent Systems Engineering (RISE) group at IIT-Madras. The objective of SHAKTI is to create production-grade processors,
        fully integrated System on Chips (SoCs), development boards, and software platforms based on SHAKTI.</p>
        The RISC-V ISA is the foundation for SHAKTI processors. Depending on the manufacturing foundry, the CPUs are built using either 22 nm FinFET or 180 nm CMOS technology.  "Base Processors," "Multi-Core Processors," and "Experimental Processors" are the three basic categories into which they have been divided.  The E and C-classes are the first set of indigenous processors aimed at Internet of Things (IoT), Embedded and Desktop markets.</p>
        <br/>
        
        <b style="font-size:25px;" id="eclass">E-class processors <hr style="width:50%"/></b>
<p>The E-class, designed for low-power and low-computer applications, are 32/64 bit microcontrollers capable of implementing
 all RISC-V ISA extensions. The E-class is a three-stage pipeline with an operational frequency of less than 200 MHz on silicon. It is capable of running real-time operating systems like FreeRTOS, Zephyr and eChronos. Market segments for E-class processors
  include smart cards, IoT devices, motor controls, and robotic platforms.</P> 

<p>E-arty35T is a SoC based on E-class. The E-arty35T SoC is a single-chip 32-bit E-class microcontroller with 128kB RAM. It has a Platform Level Interrupt Controller (PLIC), a Counter, 2 Serial Peripheral (SPI), 2 Universal Asynchronous Receiver Transmitter (UART), 1 Inter-Integrated Circuit (I2C), 6 Pulse Width Modulators (PWM), 32 General Purpose Input Output (GPIO) pins 
(of which the upper 16 GPIO pins are dedicated to onboard LEDs and switches), a Xilinx analog-to-digital (X-ADC).</p>
<br/>
<b style="font-size:25px;" id="earty">E-arty35T</b><hr style='width:75%'/>
<ul style="list-style-type:circle">
<li>	E-arty35Tis a SoC based on SHAKTI E class. </li>
<li>	E-arty35Tis supported on Artix 7 35T board.</li>
<li>	It has an abridged version of 32 bit E class. It includes I, M, A and C.</li>
</ul><br/><br/>
<b style="font-size:25px;" id="axi">AXI</b><hr style="width:50%"/>
<br/>
The ARM Advanced Microcontroller Bus Architecture 3 (AXI3) and 4 (AXI4) specifications include the Advanced eXtensible Interface (AXI), which is a parallel high-performance, synchronous, high-frequency, multi-master, multi-slave communication interface primarily intended for on-chip communication.
The AXI Interconnect IP connects one or more AXI memory-mapped Master devices to one or more memory-mapped Slave devices.
<br/> 
        <img src="./assets/axi.jpg"/>
        <hr style="width:75%"><br/>
        <div id="copyrights">
        &#xA9; Mahendra Vamshi,Jayasree and Dinesh<br/>
        Website floating point operation
        </div>
        </div>`
    }
    else if(src==2){
        
        content=`<div id='mainheading'> INTRODUCTION</div><hr style='width:75%'/><div id='info'><br/>Representation of floating point numbers :<br/>

        The scientific notation of fraction (F) and exponent (E) with a radix of 2 is used in computers to represent floating-point numbers. This notation is written as FX2^E. E and F both have
         the potential to be positive or negative. IEEE 754 is the standard used by contemporary computers to represent floating-point numbers. <br/><br/>
         &emsp;Types of representation: 
        <ul style="list-style-type:circle">
        <li>	Single-precision 32-bit  </li>
        <li>	Double-precision 64-bit</li></ul>
        A floating point number has three fields, viz, sign field ( S ), exponent field ( E ) and mantissa ( I ). The exponent field is added to a bias component to differentiate between negative and positive exponents. The decimal equivalent of this representation is
        <br/><br/><img src="./assets/fpintro.jpg" width=100px /><br/><br/>
        Here we have designed the architectures for 16-bit also to achieve moderate accuracy and lower resources.
         A floating point number can be represented in binary as<br/><br/>
         <img src="./assets/fpmain1.jpg"/><br/>
         <img src="./assets/fpmain2.jpg"/><br/>
         <img src="./assets/fpmain3.jpg"/><br/><br/><br/>
         The steps of converting a fixed point number to a floating point number are:<br/>
         <ul style="list-style-type:circle">
        	<li>Invert the number if the number is negative or if the MSB is logic 1.</li>
            <li>Count the leading zeros present in the number.</li>
            <li>Value of the mantissa is computed by left shifting the number according to the leading zero present in the number.</li>
        	<li>Subtract the leading zero count from (m-1) where m represents the number of integer bits are reserved for integers including the MSB bit.</li>
            <li>Add the result to the bias value to get the exponent.</li>
            <li>Sign of the fixed point number is the sign of the floating point number.</li>
            </ul>
        <br/>An example is given below to understand the fixed point to floating point conversion for 16-bit data width.<br/>
        <ul style="list-style-type:disc">
        <li>	The input fixed point number is a = 001000_0010000000 whose decimal value is 8.125 for m is 6-bits.</li>
        <li>	As this number is positive so no inversion is required.</li>
        <li>	There are two leading zero present in the number so it is left shifted by two bits. The result of shifting is 100000_1000000000.</li>
        <li>	The value of the mantissa is M=00000_100000 by choosing 11-bits from MSB and excluding the MSB.</li>
        <li>	The leading zero count is subtracted from (m-1) and the result is (5 – 2) = 3.</li>
        <li>	The result is added to the bias to get the exponent (E = (7+3) = 10).</li>
        <li>	Thus the floating point number is 0_1010_00000100000.</li>
        </ul>
        <hr style="width:75%"><br/>
        <div id="copyrights">
        &#xA9; Mahendra Vamshi,Jayasree and Dinesh<br/>
        Website floating point operation
        </div>
        </div>`
    }
    else if(src==3){
       
        content=`<div id='mainheading'> 
        OPERATIONS</div><hr style='width:75%'/>
        <ol id="index">
        <li><a href="#mul">Floating point Multiplication</a></li>
        <li><a href="#div">Floating point Division</a></li>
        <li><a href="#com">Floating point Comparision</a></li>
    </ol>
        <div id='mul'>floating point multiplication:<br/><hr style='width:50%'/><br/>
        A floating point multiplication between two numbers a and b can be expressed as<br/><br/>
        <img src="./assets/operation1.jpg" width=300px /><br/><br/>
        Thus it can be said that in a floating point multiplication, mantissas are multiplied and exponents are added.
        The major steps for a floating point division are: <br/>
        <ul style="list-style-type:circle">
        <li>	Extract the sign of the result from the two sign bits.</li>
        <li>	Add the two exponents ( E ). Subtract the bias component from the summation.</li>
        <li>	Multiply mantissa of b ( Mb ) by mantissa of a ( Mb ) considering the hidden bits.</li>
        <li>	If the MSB of the product is ‘1’ then shift the result to the right by 1-bit.</li>
        <li>	Due to this, the exponent is to be incremented according to the one bit right shift.</li>
        </ul>
        <br/>
        <div id='div'>floating point division:<br/><hr style='width:50%'/><br/>
        A floating point division where a number a divides another number b can be expressed as<br/><br/>
        <img src="./assets/operation2.jpg" width=300px /><br/><br/>
        Thus it can be said that in a floating point division, mantissas are divided and exponents are subtracted.<br/>
The major steps for a floating point division are<br/>
        <ul style="list-style-type:square">
            <li>Extract the sign of the result from the two sign bits.</li>
            <li>Find the magnitude of the difference between two exponents ( E ). Add E to the bias if Eb>Ea or subtract E from the bias if Eb < Ea.</li>
            <li>Divide mantissa of b ( Mb ) by mantissa of a ( Mb) considering the hidden bits.</li>
            <li>If there is a leading zero then normalize the result by shifting it left.</li>
            <li>Due to the normalization, the exponent is to be decremented according to the number of left shifts.</li>
        </ul>

        <br/>
        <div id='com'>Floating point comparison: (16 bit notation )<br/><hr style='width:50%'/><br/>
        The steps involving the comparison of two floating point numbers a and b are:
        <ul style="list-style-type:circle;">
            <li> Compare the sign bits. If both are of the same sign then proceed to the next step.</li>
            <li> Compare the exponents. If both exponents are also equal then go to the next step.</li>
            <li> Compare the mantissas. Generate three outputs ( <,> and =).</li>
        </ul><br/>
        Two sign bits are compared using a simple 1-bit comparator. A 4-bit comparator is used to compare the exponents. If both the numbers have the 
        same sign and their exponents are also equal then at the last step mantissas are compared. 
        The two mantissas are compared using a 11-bit comparator.<br/>
        <hr style="width:75%"><br/>
        <div id="copyrights">
        &#xA9; Mahendra Vamshi,Jayasree and Dinesh<br/>
        Website floating point operation
        </div>
        </div>`
    }
    else if(src==4){
       
        content=`<div id='mainheading'> 
        RESULTS</div><hr style='width:75%'/>
        <ol id="index">
        <li><a href="#mulr">Floating point Multiplication</a></li>
        <li><a href="#divr">Floating point Division</a></li>
        <li><a href="#comr">Floating point Comparision</a></li>
        </ol>
        <div id='mulr'>Floating point multiplication:<br/><hr style='width:50%'/><br/><br/>
        <img src="./assets/result1.jpg"/><br/><br/>
        <b style="position:relative;left:50px;">Cycle count ::  200</b><br/><br/><br/>

        <div id='divr'>Floating point division:<br/><hr style='width:50%'/><br/><br/>
        <img src="./assets/result2.jpg"/><br/><br/>
        <b style="position:relative;left:50px;">Cycle count ::  198</b><br/><br/><br/>

        <div id='comr'>Floating point comparator:<br/><hr style='width:50%'/><br/><br/>
        <img src="./assets/result3.jpg"/><br/><br/>
        <b style="position:relative;left:50px;">Cycle count ::  801</b>
        <hr style="width:75%"><br/>
        <div id="copyrights">
        &#xA9; Mahendra Vamshi,Jayasree and Dinesh<br/>
        Website floating point operation
        </div>

        `
    }
    else{
        
        content=`<div id='mainheading'> REFERENCE
        </div><hr style='width:75%'/><br/><br/><div id='info'>Source Code:<br/><br/>
        Floating point Multiplication:<br/>&emsp;&emsp;
            <a href="https://github.com/JaYaSrEe2406/Floating-Point-Multiplier">Floating point multiplier</a><br/><br/>

        Floating point Division:<br/>&emsp;&emsp;
        <a href="https://github.com/mahendraVamshi/Floating-point-divider">Floating point division</a><br/><br/>
        
        Floating point Comparator:<br/>&emsp;&emsp;
        <a href="https://github.com/DineshVenkatG/16-Bit-Floating-Point-Comparator">Floating point division</a><br/><br/>
        <hr style="width:75%"><br/>
        <div id="copyrights">
        &#xA9; Mahendra Vamshi,Jayasree and Dinesh<br/>
        Website floating point operation
        </div>
        </div>`
    }

    document.getElementById("content").innerHTML=content;
}