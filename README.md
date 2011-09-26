##Introduction

I was looking for a simple calendar for a project I'm working on. All I needed was something 
where you could navigate through the months and click on a day to select it. 
Unfortunately, I couldn't find a Yii extension for that, so I ended up 
developing one myself: Simple Calendar

Simple Calendar will render a calendar without using any client side code. 
Everything works with links and query string parameters.

##Installation

Just extract the contents of the package to your extensions directory. Usually protect/extensions

##Usage

To use it, add the following to your view:

    <?php $this->widget('ext.simple-calendar.SimpleCalendarWidget'); ?>

This will render a calendar where each of the days displayed is a link in the following format:

http://example.com/current_url?month=current_month&year=current_year&day=select_day

The previous and next month links are created exactly the same way:

http://example.com/current_url?month=current_month&year=current_year&day=last_day_of_the_month

Using the query string parameters, you can get the selected date and use it wherever you need.

By default, Simple Calendar will render the calendar to the current date. If you 
need it to start displaying any other date, just pass it in the widget initialization:

    <?php $this->widget('ext.simple-calendar.SimpleCalendarWidget', array('year' => 2012, 'month' => 12, 'day' => 21); ?>

##Links
* [Try out a demo](http://www.davialexandre.com.br/demos/simple-calendar/)