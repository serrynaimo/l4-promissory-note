# Day & Date Functions Reference

Library with some basic functions to enable math with dates and days following ISO 8601.
Functions return datestamps (Number of days since 1st January 1970).
A week begins on Monday
Check the test/daydate.l4 file to see examples


## Constants

### Time Periods
- `Months in a year`: 12
- `Days in a year`: 365.2425 (accounts for 4-year leap cycle with 100 and 400 year exceptions)
- `Days in a month`: 30.436875 (average month length)
- `Days in a week`: 7

### Weekday Constants
Following ISO standard with January 1, 1970 being a Thursday:

| Weekday | Alias | Value |
|---------|-------|-------|
| `Monday` | `Mon` | 4 |
| `Tuesday` | `Tue` | 5 |
| `Wednesday` | `Wed` | 6 |
| `Thursday` | `Thu` | 0 |
| `Friday` | `Fri` | 1 |
| `Saturday` | `Sat` | 2 |
| `Sunday` | `Sun` | 3 |


## Date Constructors

### `Date` (from components)
Creates a date from day, month, and year components.
- **Given**: 
  - `day`: NUMBER (day of month)
  - `month`: NUMBER (month number 1-12)
  - `year`: NUMBER (year)
- **Giveth**: DATE object with day, month, and year properties

### `Date` (from NUMBER datestamp)
Creates a date from datestamp.
- **Given**: 
  - `days`: NUMBER datestamp
- **Giveth**: DATE object with day, month, and year properties

### `Days to date`
Converts datestamp into a DATE object.
- **Given**: 
  - `days`: NUMBER datestamp
- **Giveth**: DATE object with day, month, and year properties


## Datestamp Constructors

### `Date to days`
Converts a DATE object to datestamp.
- **Given**: 
  - `date`: DATE object
- **Giveth**: NUMBER datestamp

### `Day` (from components)
Creates a datestamp from day, month, and year.
- **Given**: 
  - `day`: NUMBER (day of month)
  - `month`: NUMBER (month number 1-12)
  - `year`: NUMBER (year)
- **Giveth**: NUMBER datestamp

### `Day` (from date)
Creates a datestamp from a DATE object.
- **Given**: 
  - `date`: DATE object
- **Giveth**: NUMBER datestamp

### `Year` (from year)
Gets the datestamp for the first day of a year.
- **Given**: 
  - `year`: NUMBER (year)
- **Giveth**: NUMBER datestamp

### `Year` (from date)
Gets the datestamp for the first day of a year from a DATE object.
- **Given**: 
  - `date`: DATE object
- **Giveth**: NUMBER datestamp

### `Month` (from components)
Gets the datestamp for the first day of a month.
- **Given**: 
  - `month`: NUMBER (month number 1-12)
  - `year`: NUMBER (year)
- **Giveth**: NUMBER datestamp

### `Month` (from date)
Gets the datestamp for the first day of a month from a DATE object.
- **Given**: 
  - `date`: DATE object
- **Giveth**: NUMBER datestamp

### `Week`
Gets the datestamp for the first day of a week.
- **Given**: 
  - `week`: NUMBER (week number)
  - `year`: NUMBER (year)
- **Giveth**: NUMBER datestamp



## Month Constructors
These functions create datestamps for specific months. Each takes a day and year and returns a datestamp.
E.g. `January 1 2025 -> 20088`

- `January` (AKA `Jan`)
- `February` (AKA `Feb`)
- `March` (AKA `Mar`)
- `April` (AKA `Apr`)
- `May`
- `June` (AKA `Jun`)
- `July` (AKA `Jul`)
- `August` (AKA `Aug`)
- `September` (AKA `Sep`)
- `October` (AKA `Oct`)
- `November` (AKA `Nov`)
- `December` (AKA `Dec`)


## Datestamp Math Helpers

### `Months since year start to days` (from components)
Calculates days from start of year to a given month.
- **Given**: 
  - `month`: NUMBER (month number 1-12)
  - `year`: NUMBER (year)
- **Giveth**: NUMBER (days)

### `Months since year start to days` (from date)
Calculates days from start of year to a given month from a DATE object.
- **Given**: 
  - `date`: DATE object
- **Giveth**: NUMBER (days)

### `Days in month` (from components)
Calculates number of days in a given month.
- **Given**: 
  - `month`: NUMBER (month number 1-12)
  - `year`: NUMBER (year)
- **Giveth**: NUMBER (days in month)

### `Days in month` (from date)
Calculates number of days in a given month from a DATE object.
- **Given**: 
  - `date`: DATE object
- **Giveth**: NUMBER (days in month)

### `Days in year` (from year)
Calculates number of days in a given year.
- **Given**: 
  - `year`: NUMBER (year)
- **Giveth**: NUMBER (365 or 366)

### `Days in year` (from date)
Calculates number of days in a given year from a DATE object.
- **Given**: 
  - `date`: DATE object
- **Giveth**: NUMBER (365 or 366)

### `Years to days` (from year)
Calculates days from year 0 to a given year.
- **Given**: 
  - `year`: NUMBER (year)
- **Giveth**: NUMBER (days)

### `Years to days` (from date)
Calculates days from year 0 to a given year from a DATE object.
- **Given**: 
  - `date`: DATE object
- **Giveth**: NUMBER (days)


## Weekday Functions

### `Weekday of` (from days)
Gets the weekday number (0-6) for a given date.
- **Given**: 
  - `date`: NUMBER (datestamp) or DATE object
- **Giveth**: NUMBER (0-6)

### `Weekday of 1st day of month` (from components)
Gets the weekday of the first day of a month.
- **Given**: 
  - `month`: NUMBER (month number 1-12)
  - `year`: NUMBER (year)
- **Giveth**: NUMBER (0-6)

### `Weekday of 1st day of month` (from date)
Gets the weekday of the first day of a month from a DATE object.
- **Given**: 
  - `date`: DATE object
- **Giveth**: NUMBER (0-6)

### `Weekday of 1st day of year` (from year)
Gets the weekday of January 1st of a year.
E.g. `2025 -> Wednesday`
- **Given**: 
  - `year`: NUMBER (year)
- **Giveth**: NUMBER (0-6)

### `Weekday of 1st day of year` (from date)
Gets the weekday of January 1st of a year from a DATE object.
- **Given**: 
  - `date`: DATE object
- **Giveth**: NUMBER (0-6)


## Week Functions

### `Week`
Gets the week of the year number for a given date.
- **Given**: 
  - `date`: NUMBER (datestamp) or DATE object
- **Giveth**: NUMBER (week number)

### `Weeks in year` (from year)
Calculates number of weeks in a given year.
E.g. `2004 -> 53`
- **Given**: 
  - `year`: NUMBER (year)
- **Giveth**: NUMBER (52 or 53)

### `Weeks in year` (from date)
Calculates number of weeks in a given year from a DATE object.
- **Given**: 
  - `date`: DATE object
- **Giveth**: NUMBER (52 or 53)


## Attribute Checkers

### `is weekend`
Checks if a given date falls on a weekend.
- **Given**: 
  - `date`: NUMBER (datestamp) or DATE object
- **Giveth**: BOOLEAN

### `is weekday`
Checks if a given date falls on a weekday.
- **Given**: 
  - `date`: NUMBER (datestamp) or DATE object
- **Giveth**: BOOLEAN

### `is leap year` (from year)
Checks if a given year is a leap year. 
E.g. `2004 -> TRUE`
- **Given**: 
  - `year`: NUMBER (year)
- **Giveth**: BOOLEAN

### `is leap year` (from date)
Checks if a given date's year is a leap year.
- **Given**: 
  - `date`: DATE object
- **Giveth**: BOOLEAN


## Relative Time Phrases

### `the day after`
Gets the date for the day AFTER a given date.
- **Given**: 
  - `date`: NUMBER (datestamp) or DATE object
- **Giveth**: NUMBER (datestamp)

### `the day before`
Gets the date for the day BEFORE a given date.
- **Given**: 
  - `days`: NUMBER (datestamp) or DATE object
- **Giveth**: NUMBER (datestamp)

### `the week after`
Gets the date for Monday of NEXT week from a given date.
- **Given**: 
  - `date`: NUMBER (datestamp) or DATE object
- **Giveth**: NUMBER (datestamp)

### `the week before`
Gets the date for Monday of the PREVIOUS week from a given date.
- **Given**: 
  - `date`: NUMBER (datestamp) or DATE object
- **Giveth**: NUMBER (datestamp)

### `the month after`
Gets the date for the first day of NEXT month.
- **Given**: 
  - `date`: NUMBER (datestamp) or DATE object
- **Giveth**: NUMBER (datestamp)

### `the month before`
Gets the date for the first day of PREVIOUS month.
- **Given**: 
  - `date`: NUMBER (datestamp) or DATE object
- **Giveth**: NUMBER (datestamp)



## Comparators

### `the earlier of`
Returns the earlier of two dates.
- **Given**: 
  - `date1`: NUMBER (datestamp) or DATE object
  - `date2`: NUMBER (datestamp) or DATE object
- **Giveth**: NUMBER (datestamp)

### `the later of`
Returns the later of two dates.
- **Given**: 
  - `date1`: NUMBER (datestamp) or DATE object
  - `date2`: NUMBER (datestamp) or DATE object
- **Giveth**: NUMBER (datestamp)


## Stringify Functions

### `Name of month`
Converts a datestamp to month name. (e.g. January)
- **Given**: 
  - `days`: NUMBER (datestamp) or DATE object
- **Giveth**: STRING (month name)

### `Name of weekday`
Converts a datestamp to weekday name. (e.g. Monday)
- **Given**: 
  - `days`: NUMBER (datestamp) or DATE object
- **Giveth**: STRING (weekday name)
