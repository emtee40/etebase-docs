---
title: Calendar (iCalendar)
---

Calendars store calendar event information using the [iCalendar format](https://en.wikipedia.org/wiki/ICalendar).

The iCalendar format has different versions, and iCalendars of all versions can be stored in this type, but the recommended version is 2.0.

This collection type only supports the `VEVENT` iCalendar type (calendar events), for tasks, please refer to the [tasks specifications](./tasks).

## Collection

### Collection type: `etebase.vevent`

This is the type indicating it's an iCalendar event collection.

### Metadata

#### name: string

The user visible name of the calendar.

#### description: string (optional)

The user visible description of the calendar.

#### color: string (recommended)

The user visible color of the calendar as `#RRGGBB` or `#RRGGBBAA`.

#### mtime: milliseconds since epoch

When was this collection last modified.


## Item

### Metadata

#### type: leave empty

If the type is empty, it indicates a event item. New types may be added in the future.

#### name: the UID of the event item

This is exactly the same as the UID inside the event itself, and is used for quick lookup.

#### mtime: milliseconds since epoch

When was this item last modified. Useful for sorting based on modification time.

### Content

The content of the item is the iCalendar item itself and nothing else.
