Why This Makes Sense:
Logical Dependency: The coordinate auto-updating feature depends on having fresh location data from the continuous location updates
User Experience: If location tracking stops, it would be confusing to have coordinate updates still "running" but using stale data
Clean State Management: Prevents orphaned intervals and ensures the UI accurately reflects the current state
User Flow Now:
User starts location tracking → Button greys out, updates every 10s
User starts coordinate auto-updating → Both buttons are grey, coordinates update every 10s
User stops location tracking → Both features stop automatically, both buttons return to normal
If user wants coordinate updates again, they need to restart location tracking first
This creates a more intuitive and reliable system where the dependency between location tracking and coordinate updates is automatically managed!