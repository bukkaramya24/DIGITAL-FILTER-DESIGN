# DIGITAL-FILTER-DESIGN  

COMPANY: CODTECH IT SOLUTION
NAME: BUKKA RAMYA
INTERN ID: COD123
DOMAIN: VLSI
DURATION: 4WEEKS
MENTOR: NEELA SANTOSH 


#DESCRIPTION OF MY TASK
          In this project, we designed and tested a digital FIR (Finite Impulse Response) filter using Verilog, a hardware description language used to model digital systems. FIR filters are widely used in digital signal processing to remove noise or unwanted parts from signals. They are called "finite" because they only use a limited number of past input values to calculate the output, and they are very stable since they do not use feedback.

           We created a 4-tap FIR filter, which means it uses the current input and the last three inputs to compute the output. The filter multiplies each input by a number called a coefficient and then adds up the results to produce the final output. In our case, we chose the coefficients to be 1, 2, 3, and 4. These numbers were fixed in the Verilog code. So, for any new input, the output is calculated like this: output = 1 × current_input + 2 × previous_input + 3 × second_previous + 4 × third_previous.

            To build the filter, we used a shift register in Verilog to store the latest four input values. On every clock cycle, the input values shift to the right, and the newest input goes into the first register. The output is calculated using these values and the coefficients. The output is updated every time the clock signal rises, and we also added a reset signal so that the filter can be initialized to zero before starting.

            We also wrote a testbench in Verilog to simulate the filter. A testbench is like a tester program that sends inputs to the filter and observes the outputs to check if it works properly. In the testbench, we created a clock signal and applied a few different input values over time. Some values were positive, some were zero, and some were negative to check how the filter responds in different situations. We also used a reset signal at the start to make sure everything begins from zero.

            After running the simulation using Icarus Verilog (a free Verilog compiler), we used GTKWave to view the results. GTKWave shows the waveforms of the signals, such as the clock, input, and output, over time. We could clearly see how the input values were shifting through the filter and how the output changed according to the inputs and coefficients. The output matched the expected values, proving that the FIR filter was working correctly.

![Image](https://github.com/user-attachments/assets/a828304b-4ab1-49f8-b8a6-265c85389953)
![Image](https://github.com/user-attachments/assets/130aa691-d9ed-4be0-a0c7-37e8588d5d19)
