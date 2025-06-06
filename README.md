# T-FLIPFLOP-POSEDGE

# DEVELOPED BY: NITHISH S
# REGISTER NO: 2122242401045

**AIM:**

To implement  T flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**T Flip-Flop**

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**TRUTH TABLE**

![300544901-cdd7fb32-539f-4b66-bb8d-f305a153c886](https://github.com/user-attachments/assets/83d561f5-e355-4e8e-9212-7fb86ec93405)


**PROGRAM**
```PYTHON
  module T(q,qb,t,clock);
  input t,clock;
  output reg q;
  output qb;
  
  always @ (posedge(clock))
  begin
  q<=(t^q);
  end
  assign qb=(~q);
  endmodule
```

**RTL LOGIC FOR FLIPFLOPS**

![448025952-4ea2e7f7-1733-4900-9d27-8ab1d5484bdb](https://github.com/user-attachments/assets/a96a4e47-2ded-4258-9e39-03c18bbecff3)


**TIMING DIGRAMS FOR FLIP FLOPS**

![448027067-228f5215-07bd-4e4c-bf60-7a475324a1de](https://github.com/user-attachments/assets/3ada042b-1dc9-4716-8f8d-bcfa917fb860)


**RESULTS**
RESULTS Thus the implemenetation of T flip flop has been verified using verilog code.
