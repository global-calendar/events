## An international event database

A complete JSON5 file for all holidays, observances, events, international and national days.

Base language of this list is English and translations can serve via po files or can happen in the applications.

## Format

| Key         | Type              | Optional | Format            | Description |
| ----------- | ----------------- | -------- | ----------------- | ----------- |
| calender    | String            | No       | [a-z ]+           | The calendar that "day" and "month" belong to. eg. gregorian or jalali |
| month       | Integer           | No       | \d{1,2}           | Month of the event |
| day         | Integer or String | No       | (\d{1,2}|[a-z ]+) | Day of the event, can be a positive number larger than zero or a string like "first wed", "second tue", "last friday" or ... |
| description | Object            | No       | [\w ]+            | Contains at least "default" key and COULD have "short", "long". If it's not defined, they'll fallback to the default one |
| tags        | Array of String   | Yes      | [a-z0-9 ]+        | Possible tags, e.g. countries that this event is important in |
| holiday     | Array of String   | Yes      | [a-z ]+           | List of countries or regions that this event is holiday in |
| refs        | Array of String   | Yes      | [a-z ]+           | List of references |
