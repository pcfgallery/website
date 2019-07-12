---
title: Auto Number Control
metadate: hide
categories:
  - autonumber
image: /assets/images/autonumber.png
visit: 
download: 'https://github.com/rajsekhar311/Auto-Number-PCF-Control'
authors:
  - phani_raja_sekhar
---

A control to generate Auto Number based on the format specified. 
1. Use {} if you want to show constant values like prefix or suffix. Example: {ACC}
2. Use [] if you want to show field value. Example: [accountnumber]
3. Use [()] if you want to show value from the lookup field. Example: [parentaccountid(numberofemployees)]
4. You can use any separator in between. Example: {ACC}-[accountnumber]-[parentaccountid(numberofemployees)] and the output would be {ACC}-1001-200
