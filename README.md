# GPS Precision Tester

A mobile web page for checking whether a phone’s location (GPS / Wi‑Fi / cell) can reach **5–10 ft** precision indoors — for example inside a Walmart Supercenter.

Open it in Safari on an iPhone: **https://josephcagle.github.io/walmart-gps-test/**

Nothing is uploaded. Readings stay on the phone until you copy, share, or download the CSV.

## In-store test (about 10 minutes)

1. On the iPhone, turn **Wi‑Fi** and **Location Services** on, and keep **Precise Location** enabled for Safari. Open the link above in **Safari** (not in-app browsers), leave the tab in the foreground, and tap **Allow** when asked for location.
2. Tap **Start tracking**. Walk the store and watch the big accuracy number: **green ≤ 10 ft**, **yellow 10–30 ft**, **red > 30 ft**. Also note best / median / worst and the percent of readings ≤ 10 ft. The reported radius can be optimistic.
3. **Waypoints (no tape measure):** pick two easy-to-recognize spots about an aisle or two apart (aisle-end caps, pillars, etc.). Each time you walk past one, tap **Waypoint A** or **Waypoint B**. Do several A → B → A → B passes. The page shows the GPS distance between A and B, the spread of all A taps, the spread of all B taps, and how much the A↔B distance varies. If those spreads are larger than 10 ft, phone location is not precise enough for aisle-level navigation.
4. Stand still for 20–30 seconds and run the **stand-still test**. Then **Copy**, **Share**, or **Download** the CSV log so you can review it later.

## What the numbers mean

`coords.accuracy` from the browser is meters, roughly a 68% / 1‑sigma horizontal radius. The page converts to feet (× 3.28084).

Waypoint **spread** is the farthest tap from that waypoint’s average reported position, in feet. That is a real-world precision estimate.
