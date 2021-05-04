# "Thingsboard Widget Library" Documentation

## Table of Contents
1. [Control Widgets](#controlwidgets)  
	1.1 [Switch 1](#switch1)  
	1.2 [Toggle Button 1](#togglebutton1)  
	1.3 [Slider](#slider)  
	1.4 [Thermostat 1](#thermostat1)  
2. [Latest Value Widgets](#latestvaluewidgets)  
   2.1 [Fluid Level 1](#fluidlevel1)  
   2.2 [Fluid Level 2](#fluidlevel2)  
   2.3 [Light Bulb 1](#lightbulb1)  	

<div id="controlwidgets"/>

## 1. Control Widgets

<div id="switch1"/>

### 1.1 Switch 1

![image info](./pictures/switch11.png)
![image info](./pictures/switch12.png) 

<div id="togglebutton1"/>

### 1.2 Toggle Button 1

![image info](./pictures/togglebutton11.png)
![image info](./pictures/togglebutton12.png) 

<div id="slider"/>

### 1.3 Slider

![image info](./pictures/slider1.png)
![image info](./pictures/slider2.png) 

<div id="thermostat1"/>

### 1.4 Thermostat 1

Widget type: Control Widget

The Thermostat Wiget allows the graphical adjustment of a value using the two arrow keys. The values will be syncronized with the device at startup and sends the current values on change. The min and max as well as the Step-width can be adjusted.

### Parameters:


**Change request Method**

SetValue RPC Method - Default: setValue

**RPC request timeout**

Max. Response time for a RPC request. - Default: 500ms

**Status request Method**

Get Value RPC Method - Default: getValue

**Minimum Value**

Min. Value - Default: 0
   
**Maximum Value**

Max. Value - Default: 100   

**Step Width**

Step Width, can be 0.1 or 1 - Default: 1   
   

![image info](./pictures/thermostat11.png)

<div id="latestvaluewidgets"/>

## 2. Latest Value Widgets

<div id="fluidlevel1"/>

### 2.1 Fluid Level 1

![image info](./pictures/fluidlevel11.png)  

<div id="fluidlevel2"/>

### 2.2 Fluid Level 2

![image info](./pictures/fluidlevel21.png)  

<div id="lightbulb1"/>

### 2.3 Light Bulb 1

![image info](./pictures/lightbulb11.png)  