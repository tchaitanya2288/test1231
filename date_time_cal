Python Date & Time:

A Python program can handle date and time in several ways. 

Converting between date formats is a common chore for computers. 

Python's time and calendar modules help track dates and times.

What is Tick?

Time intervals are floating-point numbers in units of seconds. 

Particular instants in time are expressed in seconds since 12:00am, January 1, 1970(epoch).

There is a popular time module available in Python which provides functions for working with times,
and for converting between representations. 

The function time.time() returns the current system time in ticks since 12:00am, January 1, 1970(epoch).

Example
#!/usr/bin/python
import time;  # This is required to include time module.

ticks = time.time()
print "Number of ticks since 12:00am, January 1, 1970:", ticks

Output:
Number of ticks since 12:00am, January 1, 1970: 7186862.73399


Date arithmetic is easy to do with ticks. 
However, dates before the epoch cannot be represented in this form. 

Dates in the far future also cannot be represented this way 
- the cutoff point is sometime in 2038 for UNIX and Windows.


TimeTuple?
Many of Python's time functions handle time as a tuple of 9 numbers,
as shown below −

Index	Field				Values
0		4-digit year		2008
1		Month			1 to 12
2		Day			1 to 31
3		Hour			0 to 23
4		Minute			0 to 59
5		Second			0 to 61 (60 or 61 are leap-seconds)
6		Day of Week		0 to 6 (0 is Monday)
7		Day of year		1 to 366 (Julian day)
8		Daylight savings	-1, 0, 1, -1 means library determines DST


The above tuple is equivalent to struct_time structure. 
This structure has following attributes :

Index	Attributes		Values
0		tm_year			2008
1		tm_mon			1 to 12
2		tm_mday			1 to 31
3		tm_hour			0 to 23
4		tm_min			0 to 59
5		tm_sec			0 to 61 (60 or 61 are leap-seconds)
6		tm_wday			0 to 6 (0 is Monday)
7		tm_yday			1 to 366 (Julian day)
8		tm_isdst		-1, 0, 1, -1 means library determines DST

-----------------------------------------------------------
Getting current time:

To translate a time instant from a seconds since the 
epoch floating-point value into a time-tuple, 
pass the floating-point value to a function (e.g., localtime) 
that returns a time-tuple with all nine items valid.

#!/usr/bin/python
import time

localtime = time.localtime(time.time())
print "Local current time :", localtime

Output:
Local current time : time.struct_time(tm_year=2013, tm_mon=7, 
tm_mday=17, tm_hour=21, tm_min=26, tm_sec=3, tm_wday=2, tm_yday=198, tm_isdst=0)

-----------------------------------------------------------
Getting formatted time:

You can format any time as per your requirement, 
but simple method to get time in readable format is asctime() :

#!/usr/bin/python
import time;

localtime = time.asctime( time.localtime(time.time()) )
print "Local current time :", localtime

Output:
Local current time : Tue Jan 13 10:17:09 2009
-----------------------------------------------------------
Getting calendar for a month:

The calendar module gives a wide range of methods to play with yearly and monthly calendars. 
Here, we print a calendar for a given month ( Jan 2008 ) :

#!/usr/bin/python
import calendar

cal = calendar.month(2008, 1)
print "Here is the calendar:"
print cal

Output:
Here is the calendar:
    January 2008
Mo Tu We Th Fr Sa Su
    1  2  3  4  5  6
 7  8  9 10 11 12 13
14 15 16 17 18 19 20
21 22 23 24 25 26 27
28 29 30 31
-----------------------------------------------------------
The time Module:

There is a popular time module available in Python which provides functions for working with times and for converting between representations. 

Below are the list of all available methods:

-----------------------------------------------------------
Python time altzone() Method:

Description: 
The method altzone() is the attribute of the time module. 
This returns the offset of the local DST timezone, in seconds west of UTC, if one is defined. 
This is negative if the local DST timezone is east of UTC (as in Western Europe, including the UK). 
Only use this if daylight is nonzero.

Syntax: time.altzone

Note:
This method returns the offset of the local DST timezone, in seconds west of UTC,
if one is defined.

Example
#!/usr/bin/python
import time

print "time.altzone %d " % time.altzone

Output:
time.altzone() 25200
-----------------------------------------------------------
Python time asctime() Method:

Description : 
The method asctime() converts a tuple or struct_time representing a time as returned by gmtime() or localtime() to a 24-character string of the following form: 'Tue Feb 17 23:21:05 2009'.

Syntax : time.asctime([t]))

Parameters:
t -- This is a tuple of 9 elements or struct_time representing 
a time as returned by gmtime() or localtime() function.

Note:
This method returns 24-character string of the following form: 'Tue Feb 17 23:21:05 2009'.

Example
#!/usr/bin/python
import time

t = time.localtime()
print "time.asctime(t): %s " % time.asctime(t)

Output:
time.asctime(t): Tue Feb 17 09:42:58 2009
-----------------------------------------------------------
Python time clock() Method:

Description: 
The method clock() returns the current processor time as a floating point number expressed in seconds on Unix. 
The precision depends on that of the C function of the same name, 
but in any case, this is the function to use for benchmarking Python or timing algorithms.

On Windows, this function returns wall-clock seconds elapsed since the first call to this function, as a floating point number, based on the Win32 function QueryPerformanceCounter.

Syntax : time.clock()

Note:
This method returns the current processor time as a floating point number expressed in
seconds on Unix and in Windows it returns wall-clock seconds elapsed since the first call to this function, as a floating point number.

Example:
#!/usr/bin/python
import time

def procedure():
    time.sleep(2)

# measure process time
t0 = time.clock()
procedure()
print (time.clock() - t0, "seconds process time")

# measure wall time
t0 = time.time()
procedure()
print (time.time() - t0, "seconds wall time")

Output:
0.0 seconds process time
2.50023603439 seconds wall time

Note: Not all systems can measure the true process time. 
On such systems (including Windows), 
clock usually measures the wall time since the program was started.
-----------------------------------------------------------
Python time ctime() Method:

Description: 
The method ctime() converts a time expressed in seconds since the epoch to a string representing
local time. 
If secs is not provided or None, the current time as returned by time() is used. 
This function is equivalent to asctime(localtime(secs)). 
Locale information is not used by ctime().

Syntax : time.ctime([ sec ])

Parameters:
sec -- These are the number of seconds to be converted into string representation.

Note:
This method does not return any value.

Example
#!/usr/bin/python
import time

print "time.ctime() : %s" % time.ctime()

Output:
time.ctime() : Tue Feb 17 10:00:18 2009
-----------------------------------------------------------
Python time gmtime() Method:

Description: 
The method gmtime() converts a time expressed in seconds since the epoch
to a struct_time in UTC in which the dst flag is always zero. 
If secs is not provided or None, the current time as returned by time() is used.

Syntax: time.gmtime([ sec ])

Parameters:
sec -- These are the number of seconds to be converted
into structure struct_time representation.

Note: 
This method does not return any value.

Example:
#!/usr/bin/python
import time

print "time.gmtime() : %s" % time.gmtime()

Output:
time.gmtime() : (2009, 2, 17, 17, 3, 38, 1, 48, 0)
-----------------------------------------------------------
Python time localtime() Method:

Description:
The method localtime() is similar to gmtime() but it converts number of seconds to local time.
If secs is not provided or None, the current time as returned by time() is used. 
The dst flag is set to 1 when DST applies to the given time.

Syntax: time.localtime([ sec ])

Parameters:
sec -- These are the number of seconds to be converted into structure struct_time representation.

Note: 
This method does not return any value.

Example
#!/usr/bin/python
import time
print "time.localtime() : %s" % time.localtime()

Output:
time.localtime() : (2009, 2, 17, 17, 3, 38, 1, 48, 0)

-----------------------------------------------------------
Python time mktime() Method:

Description:
The method mktime() is the inverse function of localtime(). 
Its argument is the struct_time or full 9-tuple and it returns a floating point number, for compatibility with time().

If the input value cannot be represented as a valid time, either OverflowError or ValueError will be raised.

Syntax : time.mktime(t)

Parameters:
t -- This is the struct_time or full 9-tuple.

Note:
This method returns a floating point number, for compatibility with time().

Example
#!/usr/bin/python
import time

t = (2009, 2, 17, 17, 3, 38, 1, 48, 0)
secs = time.mktime( t )
print "time.mktime(t) : %f" %  secs
print "asctime(localtime(secs)): %s" % time.asctime(time.localtime(secs))

Output:
time.mktime(t) : 1234915418.000000
asctime(localtime(secs)): Tue Feb 17 17:03:38 2009
-----------------------------------------------------------
Python time sleep() Method:

Description:
The method sleep() suspends execution for the given number of seconds. 

The argument may be a floating point number to indicate a more precise sleep time.

The actual suspension time may be less than that requested because any caught signal will terminate the sleep() following execution of that signal's catching routine.

Syntax: time.sleep(t)

Parameters:
t -- This is the number of seconds execution to be suspended.

Note:
This method does not return any value.

Example
#!/usr/bin/python
import time

print "Start : %s" % time.ctime()
time.sleep( 5 )
print "End : %s" % time.ctime()

Output:
Start : Tue Feb 17 10:19:18 2009
End : Tue Feb 17 10:19:23 2009
-----------------------------------------------------------
Python time strftime() Method:

Description: 
The method strftime() converts a tuple or struct_time representing a time as returned by gmtime()
or localtime() to a string as specified by the format argument.

If t is not provided, the current time as returned by localtime() is used.
format must be a string. An exception ValueError is raised if any field in t is outside of the allowed range.

Syntax: time.strftime(format[, t])

Parameters:
t -- This is the time in number of seconds to be formatted.

format -- This is the directive which would be used to format given time.
The following directives can be embedded in the format string:

Directive:
%a - abbreviated weekday name
%A - full weekday name
%b - abbreviated month name
%B - full month name
%c - preferred date and time representation
%C - century number (the year divided by 100, range 00 to 99)
%d - day of the month (01 to 31)
%D - same as %m/%d/%y
%e - day of the month (1 to 31)
%g - like %G, but without the century
%G - 4-digit year corresponding to the ISO week number (see %V).
%h - same as %b
%H - hour, using a 24-hour clock (00 to 23)
%I - hour, using a 12-hour clock (01 to 12)
%j - day of the year (001 to 366)
%m - month (01 to 12)
%M - minute
%n - newline character
%p - either am or pm according to the given time value
%r - time in a.m. and p.m. notation
%R - time in 24 hour notation
%S - second
%t - tab character
%T - current time, equal to %H:%M:%S
%u - weekday as a number (1 to 7), Monday=1. Warning: In Sun Solaris Sunday=1
%U - week number of the current year, starting with the first Sunday as the first day of the first week
%V - The ISO 8601 week number of the current year (01 to 53), where week 1 is the first week that has at least 4 days in the current year, and with Monday as the first day of the week
%W - week number of the current year, starting with the first Monday as the first day of the first week
%w - day of the week as a decimal, Sunday=0
%x - preferred date representation without the time
%X - preferred time representation without the date
%y - year without a century (range 00 to 99)
%Y - year including the century
%Z or %z - time zone or name or abbreviation
%% - a literal % character
Return Value
This method does not return any value.

Example:
#!/usr/bin/python
import time

t = (2009, 2, 17, 17, 3, 38, 1, 48, 0)
t = time.mktime(t)
print time.strftime("%b %d %Y %H:%M:%S", time.gmtime(t))

Output:
Feb 18 2009 00:03:38
-----------------------------------------------------------
Python time strptime() Method:

Description:
The method strptime() parses a string representing a time according to a format.
The return value is a struct_time as returned by gmtime() or localtime().

The format parameter uses the same directives as those used by strftime();
it defaults to "%a %b %d %H:%M:%S %Y" which matches the formatting returned by ctime().

If string cannot be parsed according to format, or if it has excess data after parsing, ValueError is raised.

Syntax : time.strptime(string[, format])

Parameters:
string -- This is the time in string format which would be parsed based on the given format.

format -- This is the directive which would be used to parse the given string.

The following directives can be embedded in the format string:

Directive
%a - abbreviated weekday name
%A - full weekday name
%b - abbreviated month name
%B - full month name
%c - preferred date and time representation
%C - century number (the year divided by 100, range 00 to 99)
%d - day of the month (01 to 31)
%D - same as %m/%d/%y
%e - day of the month (1 to 31)
%g - like %G, but without the century
%G - 4-digit year corresponding to the ISO week number (see %V).
%h - same as %b
%H - hour, using a 24-hour clock (00 to 23)
%I - hour, using a 12-hour clock (01 to 12)
%j - day of the year (001 to 366)
%m - month (01 to 12)
%M - minute
%n - newline character
%p - either am or pm according to the given time value
%r - time in a.m. and p.m. notation
%R - time in 24 hour notation
%S - second
%t - tab character
%T - current time, equal to %H:%M:%S
%u - weekday as a number (1 to 7), Monday=1. Warning: In Sun Solaris Sunday=1
%U - week number of the current year, starting with the first Sunday as the first day of the first week
%V - The ISO 8601 week number of the current year (01 to 53), where week 1 is the first week that has at least 4 days in the current year, and with Monday as the first day of the week
%W - week number of the current year, starting with the first Monday as the first day of the first week
%w - day of the week as a decimal, Sunday=0
%x - preferred date representation without the time
%X - preferred time representation without the date
%y - year without a century (range 00 to 99)
%Y - year including the century
%Z or %z - time zone or name or abbreviation
%% - a literal % character

Note:
This return value is struct_time as returned by gmtime() or localtime().

Example:
#!/usr/bin/python
import time

struct_time = time.strptime("30 Nov 00", "%d %b %y")
print ("returned tuple: %s " % struct_time)

Output:
returned tuple: (2000, 11, 30, 0, 0, 0, 3, 335, -1)
-----------------------------------------------------------
Python time time() Method:

Description:
The method time() returns the time as a floating point number expressed in seconds since the epoch, in UTC.

Note: Even though the time is always returned as a floating point number, not all systems provide time with a better precision than 1 second. While this function normally returns non-decreasing values, it can return a lower value than a previous call if the system clock has been set back between the two calls.

Syntax : time.time()

Note:
This method returns the time as a floating point number expressed in seconds since the epoch, in UTC.

Example
#!/usr/bin/python
import time

print "time.time(): %f " %  time.time()
print time.localtime( time.time() )
print time.asctime( time.localtime(time.time()) )

Output:
time.time(): 1234892919.655932
(2009, 2, 17, 10, 48, 39, 1, 48, 0)
Tue Feb 17 10:48:39 2009

-----------------------------------------------------------
Python time tzset() Method:

Description:
The method tzset() resets the time conversion rules used by the library routines.

The environment variable TZ specifies how this is done.

The standard format of the TZ environment variable is (whitespace added for clarity):

std offset [dst [offset [,start[/time], end[/time]]]]
std and dst: Three or more alphanumerics giving the timezone abbreviations. These will be propagated into time.tzname.

offset: The offset has the form: .hh[:mm[:ss]]. This indicates the value added the local time to arrive at UTC. If preceded by a '-', the timezone is east of the Prime Meridian; otherwise, it is west. If no offset follows dst, summer time is assumed to be one hour ahead of standard time.

start[/time], end[/time]: Indicates when to change to and back from DST. The format of the start and end dates are one of the following:

Jn: The Julian day n (1 <= n <= 365). Leap days are not counted, so in all years February 28 is day 59 and March 1 is day 60.

n: The zero-based Julian day (0 <= n <= 365). Leap days are counted, and it is possible to refer to February 29.

Mm.n.d: The d'th day (0 <= d <= 6) or week n of month m of the year (1 <= n <= 5, 1 <= m <= 12, where week 5 means 'the last d day in month m' which may occur in either the fourth or the fifth week). Week 1 is the first week in which the d'th day occurs. Day zero is Sunday.

time: This has the same format as offset except that no leading sign ('-' or '+') is allowed. The default, if time is not given, is 02:00:00.

Syntax : time.tzset()

Note:
This method does not return any value.

Example
#!/usr/bin/python
import time
import os

os.environ['TZ'] = 'EST+05EDT,M4.1.0,M10.5.0'
time.tzset()
print time.strftime('%X %x %Z')

os.environ['TZ'] = 'AEST-10AEDT-11,M10.5.0,M3.5.0'
time.tzset()
print time.strftime('%X %x %Z')

Output:
13:00:40 02/17/09 EST
05:00:40 02/18/09 AEDT
-----------------------------------------------------------

-----------------------------------------------------------

