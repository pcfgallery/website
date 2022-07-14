---
title: People Picker V1
metadate: hide
categories:
  - user
  - aad
  - picker
image: /assets/images/people-picker-v1.jpg
visit: 
download: 'https://github.com/HanumantPatil/PeoplePickerV1'
demo_youtube: 
model_support: true
canvas_support: false
portals_support: false
license_defined: true
managed_solution: false
authors:
  - hanumant_patil
---
A control for "multi" or "single" select people picker.

Control Features:

- We can user this control as "Single user select"
- We can user this control as "Multi user select"
- This control will access users from "AAD User" Table or "User" table

This solution gives the ability to select Single User or Multiple users from the people picker. It works on the User(systemuser) table or AAD User(aaduser) table of the Dataverse.
Since multi-select people picker is not there yet, this can be used as an alternate. It is build on top of Multiline text field. Moreover we have some filtering issue while using lookup column with AAD user table to overcome filtering problem, we will use this control as solution.
