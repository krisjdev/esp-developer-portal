---
title: "Dedicated Agent Skills for Wokwi"
date: "2026-11-17"
summary: "Teach your agents how to run, test, debug and profile embedded firmware with Wokwi using our dedicated skills."
authors:
  - "wokwi"
tags:
  - IDE
  - release
  - debugging
  - Wokwi
  - AI
---

Agents are capable of writing firmware, but verifying or debugging changes on physical hardware presents unique challenges.
Fortunately for developers, Wokwi can present a unique solution to this issue. Since Wokwi provides virtual hardware by
simulating it, attaching an agent is as simple as providing an interface from the simulation to the agent itself. This
is done via our [`wokwi-cli`](https://docs.wokwi.com/wokwi-ci/cli-installation) and [automation scenarios](https://docs.wokwi.com/wokwi-ci/automation-scenarios).

## Get Started

Follow the installation instructions provided in the skills repository on GitHub at [github.com/wokwi/skills](https://github.com/wokwi/skills)!

{{< github repo="wokwi/skills" >}}

## Available Skills

New skills are being added frequently, so make sure you check out the skills repository and give it a star to follow
along! The following below are currently available and should give you an idea of what is possible when you pair Wokwi
together with your agent.

### Find Memory Leaks

Catch slow memory leaks in ESP-IDF firmware by simulating hours of use within seconds and watching the free heap
value as reported by the simulation engine. Perfect for catching suspected leaks, firmware soaks, stress or endurance
tests, or to debug a device that runs out of memory after hours or days.

We even have a [heap leak demo](https://github.com/wokwi/esp32-heap-leak-demo) to demonstrate this functionality in Wokwi.

{{< figure
  src="img/heap.webp"
  alt="Free heap (bytes) graphed against time from boot. Free heap drops below the set threshold roughly eight seconds after boot."
  caption="Free heap (bytes) graphed against time from boot. Free heap drops below the set threshold roughly eight seconds after boot."
>}}

### Test LVGL UIs

Regression test LVGL-based (or other) UIs with scripted taps, swipes and button presses. The simulated display is compared
with a reference screenshot pixel-by-pixel. Supports custom chip displays and touchscreens.

### Debug ESP32 Firmware

Decode a panic backtrace, reproduce the bug with scripted inputs, capture I2C/SPI/UART traffic and attach GDB, all without
physical wires or probes. Great for fixing crashes, debugging panics, figuring out watchdog resets, hangs, intermittent
faults and deciphering unexpected/incorrect bus traffic.

### Verify ESP-IDF Built Firmware

Uses our ESP-IDF companion, [`idf-wokwi`](https://docs.wokwi.com/wokwi-ci/idf-wokwi-usage), to run and verify ESP-IDF
firmware in the simulator directly from `idf.py`. Can be used for general testing directly after builds.

## Feedback and Future Skills

Is there a skill that you'd like to see added to Wokwi? Or maybe something doesn't work as expected? Please let us know
by getting into touch or by joining the [official Wokwi Discord](https://wokwi.com/discord)!