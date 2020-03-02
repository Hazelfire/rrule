# rrule

Mitchell Vitez, 2020

## Usage

This code is meant to be used as a library so you don't have to write recurrence-rule-parsing code yourself

Use `stack test` to run tests

## Functionality

- `fromText` parses from a recurrence rule string to the Haskell RRule type
- `toText` formats an RRule to Text
- `description` gives you a description of what an RRule means, in English

## Possible future additions 

- `byEaster` as seen in the Python `dateutil` rrule implementation
- `toList :: RRule -> [UTCTime]` - a possibly-infinite list of all the `UTCTime`s described by an `RRule`
- Parse the numerals 0-6 as valid `Day`s
- Cover more of the iCalendar spec, for example handling the `DTSTART` flag, or `EXDATE` exceptions
- `before :: UTCTime -> RRule -> UTCTime` - get the last UTCTime before the given UTCTime satisfying this rule
- `after :: UTCTime -> RRule -> UTCTime` - get the first UTCTime after the given UTCTime satisfying this rule
- `between` to get the UTCTime(s) satisfying a rule and between two other UTCTimes
