---
name: date-fns
description: Prefer date-fns for all date and time manipulation (parsing, formatting, arithmetic, comparisons) instead of custom utilities, built-in Date math, or other date libraries. Use when working with dates, times, or time ranges, or when the user mentions formatting dates, computing ranges, or handling time zones.
---

# date-fns

Always use **date-fns** to work with dates and times. Avoid ad‑hoc `Date` math, manual string manipulation, or adding new date libraries.

## When to use

- Parsing or formatting dates/times
- Adding or subtracting days, months, or other units
- Comparing dates (before/after, same day, within range)
- Building calendar views and date filters
- Converting between `Date` objects and ISO strings

## Setup

```bash
pnpm add date-fns
```

```typescript
import {
  addDays,
  addMonths,
  differenceInMinutes,
  format,
  isBefore,
  isSameDay,
  parseISO,
  startOfDay,
} from "date-fns";
```

## Parsing and formatting

Prefer `parseISO` and `format` instead of manual string slicing or `toLocaleString`.

```typescript
const date = parseISO("2024-03-10T12:00:00Z");

const label = format(date, "yyyy-MM-dd"); // 2024-03-10
const longLabel = format(date, "EEEE, MMMM d, yyyy"); // Sunday, March 10, 2024
```

For date-only strings that must be treated as UTC, normalize first (e.g. by appending `Z`) and document the behavior in a shared helper.

## Arithmetic

Use date-fns helpers for arithmetic instead of mutating `Date` or doing timestamp math by hand.

```typescript
const start = new Date();
const inSevenDays = addDays(start, 7);
const lastMonth = addMonths(start, -1);

const minutes = differenceInMinutes(new Date("2024-03-10T12:30Z"), new Date("2024-03-10T12:00Z"));
```

## Comparisons and ranges

Use comparison helpers for clarity.

```typescript
const isPast = isBefore(targetDate, new Date());
const sameDay = isSameDay(a, b);

const isWithinRange = !isBefore(date, rangeStart) && !isBefore(rangeEnd, date);
```

## Time zones

date-fns operates on `Date` objects and does not manage time zones by itself. Normalize inputs at the edges:

- For ISO strings: prefer `parseISO`.
- For date-only values: decide whether they are UTC or local and convert once in a shared utility.

Keep all date parsing/normalization in a small set of helpers instead of scattered `new Date(...)` calls.

## Rules

- Prefer date-fns helpers over manual `Date` arithmetic or string formatting.
- Do not introduce other date libraries (Moment, Day.js, Luxon, etc.).
- Centralize date utilities in shared modules so behavior (especially time zones) is consistent.

