# MSCONS Viewer

A free online parser and viewer for **MSCONS (EDIFACT)** files used in the German energy market.

Upload your MSCONS file and instantly explore its structure, sender, receiver, metering points, time series and quantities, without installing anything.

👉 https://mscons-viewer.grrodre.com

---

## Screenshot

![MSCONS Viewer screenshot](img/screenshot_mscons_viewer.png)

---

## Features

- Upload and inspect MSCONS EDIFACT files
- Structured view of segments and hierarchy
- Extract metering points, time periods and readings
- Human-readable breakdown of message content

---

## Use cases

- Debugging EDIFACT / MSCONS files  
- Understanding market communication messages  
- Inspecting meter readings and time series data  

---

## What is MSCONS?

MSCONS is an UN/EDIFACT message type standardised by BDEW for transmitting consumption and feed-in meter readings in the German electricity and gas markets.

A single MSCONS file can contain readings for multiple metering points across multiple time intervals, encoded in a compact text format that is difficult to read manually.

---

## Example (raw MSCONS)

```
UNA:+.? '
UNB+UNOC:3+9900123000006:293+9900987000004:293+260101:0800+1'
UNH+1+MSCONS:D:04B:UN:2.4c'
...
QTY+220:12345.678:KWH'
RFF+AVM:1-1:1.8.0'
UNT+13+1'
UNZ+1+1'
```

---

## What the viewer provides

- Parsed message structure
- Sender / receiver identification
- Metering point breakdown
- Time intervals and readings
- OBIS-linked quantities

---

## Technical notes

MSCONS interchanges follow a structured EDIFACT envelope:

- `UNB` / `UNZ` → interchange  
- `UNH` / `UNT` → message  
- segment groups → metering points and readings  

---

## Notes

This repository does not include the source code.

For custom implementations, integrations, or extensions of this tool, feel free to reach out.

---

## About

Built by Gregorio Rodrigo  
Making energy market data easier to work with

[grrodre@gmail.com](mailto:grrodre@gmail.com)
