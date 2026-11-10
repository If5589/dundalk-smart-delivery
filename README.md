# Dundalk Smart Delivery V3.0

V3 adds a delivery workflow:
- Add stops using OpenStreetMap address search or parcel-label OCR.
- Set the current GPS location as route origin (permission required).
- Select car or walking mode.
- Use Valhalla public routing API to calculate a road-time matrix, order up to 8 stops, and request route geometry.
- See numbered A/B/C stops and route line on the map.
- Tap Start delivery to open Google Maps turn-by-turn navigation for the current stop.
- After completing a drop, return to the PWA and tap Next stop. The app records the completed delivery locally and advances to the next stop.
- Open the full route in Google Maps.
- Export/import local delivery history.

## Important limitations
This is not a full Google Maps navigation engine. Google Maps provides live turn-by-turn voice guidance, live traffic and its own vehicle/navigation UI after Start delivery is tapped. Return to this app after each drop and tap Next stop to launch the next destination.
The app's route map and route estimates use public OpenStreetMap/Valhalla data. Public demo servers have fair-use limits and no uptime guarantee; they do not guarantee live traffic. Address search uses public Nominatim; not every Irish Eircode is indexed. Verify every selected address and route before driving.
The optimiser uses current GPS location if permitted; otherwise it starts at the first stop. Up to 8 stops. It uses approximate road-time optimisation, not a guarantee of globally best delivery schedule.
Addresses/coordinates are sent to public mapping services when searching or calculating routes. Local history is stored in IndexedDB on this device and is not app-level encrypted. Protect your iPhone with a strong passcode; keep backups private.
