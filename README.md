# Appointments

A free tool for formerly incarcerated individuals to keep track of appointments in the first months home (parole check-ins, drug tests, classes, court dates, interviews, and office visits) and add them to a phone's calendar with reminders. It runs entirely in the browser: no account, no server, and nothing typed into it is sent anywhere unless the person chooses the optional Google Calendar button, which says so.

Try it at https://olivercrocco.com/appointments/, or download `appointments.html` and open it in any browser. The single file works without the internet.

It was built for a pre-release employment skills course in Louisiana and is part of the [Reentry Toolkit](https://olivercrocco.com/reentry/). Nothing in it is specific to Louisiana.

## What it does

- Records each appointment with its kind, date, time, place, and what to bring, and whether it repeats: every week, every two weeks, every month on the same weekday (such as the first Monday), or every month on the same date, with an optional end date. A list shows what is coming up in the next two weeks.
- Makes a standard calendar file (.ics) of every appointment, with reminders the day before and one hour before and the repeats included. Opening it on a phone adds everything to the phone's own calendar, so the reminders keep working without the tool.
- Uses plain titles by default ("Appointment" instead of "Parole check-in") so details do not show on a lock screen. The full name stays inside each event.
- Offers an optional "Add to Google Calendar" button for each appointment, for Android phones whose calendar app will not open the file.
- Prints the next 30 days and the repeating appointments on one page.
- Offers "Keep my work on this device" for a person's own phone or computer. Otherwise nothing is stored, and work is kept with "Save my work."
- Includes "See an example," a "Try it with an example" walk-through with made-up appointments, and a button that reads each step aloud.

## Notes on the calendar file

The file follows the iCalendar standard (RFC 5545). Times are written as local time, so they show at the same clock time on the phone. Repeat dates shown in the tool were checked against an independent calendar library for eight patterns, including the 31st of every month and a fifth weekday. Changes made later in the tool do not update the phone; the phone's calendar holds the appointments once they are added.

## Files

- `appointments.html`: the whole tool in one file. This is the source of truth.
- `build-web.mjs`: builds `web/` for sites whose Content-Security-Policy blocks inline scripts. Run `node build-web.mjs` after editing.
- `web/`: the built web version.

## License

MIT. See `LICENSE`.

Built for formerly incarcerated individuals and the programs that support them, by Oliver S. Crocco, Louisiana State University.
