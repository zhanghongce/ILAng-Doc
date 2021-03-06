# Architectural States

## Defining inputs/states

There are three major types supported in ILAng:

* Boolean -- flags or one-bit signals in the design
* Bit-vector -- multi-bit registers \(or sometimes one-bit signals\)
* Memory \(array\) -- buffers, memory system, etc. 

### Input signals

To define an Boolean \(one-bit\) input signal of the ILA model:

```cpp
auto cmd = m.NewBoolInput("Cmd");
```

To define a bit-vector \(multi-bits\) type input signal:

```cpp
auto in_addr = m.NewBvInput("InAddr", 32);
auto in_data = m.NewBvInput("InData", 8);
```

Note that, currently, ILAng does not support memory/array typed input signals.  

### State variables

In ILAng, architectural state variables are those that can be updated by the instruction commands. It can be one of the output signals or some intermediate signal/register. To define a Boolean \(one-bit\) state variable:

```cpp
auto check_pass = m.NewBoolState("CheckPass");
```

To define a bit-vector \(multi-bits\) state variable, you need to provide the bit-width:

```cpp
auto acc_status = m.NewBvState("AccStatus", 3);
```

You can also define memory/array typed state variables by specifying the bit-width of the address and the data \(key and element\). 

```cpp
auto buffer = m.NewMemState("Buffer", 32, 8);
```

## Accessing inputs/states

The architectural state variables can be accessed by their name.

```cpp
auto in_addr = m.input("InAddr");
auto buffer = m.state("Buffer");
```

It can also be enumerated.

```cpp
for (auto i = 0; i < m.input_num(); i++) {
    auto ith_input = m.input(i);
}
for (auto j = 0; j < m.state_num(); j++) {
    auto jth_state = m.state(j);
}
```

