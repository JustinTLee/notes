# CAD tools for digital logic

## 1 Introduction
* CAD tools packaged into CAD system composed of:
    * design entry
    * synthesis/optimization
    * simulation
    * physical design

<br/>
<br/>

---

<br/>
<br/>

## 2 Design entry
* formulates a description of circuit being designed
* 2 types:
    * **schematic capture** - graphical representation of a circuit diagram
    * **hardware description language** (**HDL**) - describes behavior of circuit diagram in code
* schematic capture components:
    * circuit elements from a _library_
    * subcircuits with known outputs in _hierarchical design_
* HDL components:
    * 2 main types:
        * Verilog HDL
        * VHDL (_Very High Speed Integrated Circuit HDL_)
    * offers portability between different digital technologies as a standard language
    * signals represented as variables
    * logic functions expressed as variable assignment
    * modular - supports hierarchical design

<br/>
<br/>

---

<br/>
<br/>

## 3 Synthesis
* implements efficient circuits from initial specifications
* compiles Verilog code into network of logic gates
* optimization of circuits depend on user constraints

<br/>
<br/>

---

<br/>
<br/>

## 4 Simulation
* verifies expected behavior
* a _functional simulator_ generates logical expressions during synthesis
* user supplies input values
* output is a timing diagram
    * in real life, there is a _propagation delay_ of circuit from:
        * time it takes for all input signals to change
        * time it takes for signal to go across wire

<br/>
<br/>

---

<br/>
<br/>

## 5 Physical design
* maps circuit specified from synthesis to resources available on target chip
* **configuration** - circuit implemented on actual chip

---

<br/>
<br/>