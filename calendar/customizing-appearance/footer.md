---
title: Footer
page_title: Footer
description: Footer
slug: calendar-customizing-appearance-footer
tags: footer
published: True
position: 3
---

# Footer



## 

The Footer/Status bar area of __RadCalendar__ is located below the main calendar content area. 

![calendar-customizing-appearance-footer 003](images/calendar-customizing-appearance-footer003.png)

By default the footer contains a string showing the current date and time and two buttons - __Clear__ button and __Today__ button. The __Clear__ button is used to clear all selected dates in __RadCalendar__ and the __Today__ button navigates to the current date. The following properties of __RadCalendar__ are used to modify appearance and functionality of the footer:



* __ShowFooter__ - gets or sets whether RadCalendar will display its footer/status bar area 

* __TodayButton__ - gets an instance of RadButtonElement representing the Today button in the footer. 

#### __[C#] Using the Today button__

{{region usingTodayButton}}
	            radCalendar1.TodayButton.Text = "Go to Today";
	            radCalendar1.TodayButton.Image = imageList1.Images[0];
	{{endregion}}



#### __[VB.NET] Using the Today button__

{{region usingTodayButton}}
	        RadCalendar1.TodayButton.Text = "Go to Today"
	        RadCalendar1.TodayButton.Image = ImageList1.Images(0)
	{{endregion}}



* __ClearButton__ - gets an instance of RadButtonElement representing the Clear button in the footer.



