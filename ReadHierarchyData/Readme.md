# How to read hierarchical data with Kofax RPA
This guide will show how to convert this [webpage](https://www.sec.gov/Archives/edgar/data/84839/000117120021000076/i21062_ex21.htm) into a list of data, which shows the parent of a hierarchy.
It converts this  
![image](https://user-images.githubusercontent.com/47416964/118660143-35582280-b7ee-11eb-98ea-006c789acc7c.png)

to this by keeping track of who the Parent company is by the indent level  
Name | Location | Percentage | Parent | Level
--- | --- | --- | --- | ---
Rollins, Inc. | Delaware |  |  | 1
Orkin, LLC | Delaware |  | Rollins, Inc. | 2
Orkin Systems, LLC | Delaware |  | Orkin, LLC | 3
Orkin S.A de C.V. | Mexico |  | Orkin, LLC | 3
Orkin Expansion, Inc. | Delaware |  | Orkin, LLC | 3
Rollins Dutch Holdings C.V. | Netherlands | 99% | PCO Acquisitions, Inc. | 5
Rollins Investment, LLC | Delaware | 1% | PCO Acquisitions, Inc. | 5
Rollins Dutch Holdings C.V | Netherlands |  | Rollins Investment, LLC | 6

This is achieved by building a list of Parent Companies and keeping track of the level.  
This robot shows how to add items to a list and then remove them again.  

Kofax RPA has no internal concept of a list or array

