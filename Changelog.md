# Changelog

All notable changes to Venator Solunar Fishing are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project uses [Semantic Versioning](https://semver.org/).

## [0.3.0] - 2026-09-23

### Changed

- Renamed the site from Solunar Times to Venator Solunar Fishing, in both the page heading and the browser tab title.
- Reduced the heading size slightly on narrow screens so the longer name fits on two lines and stays clear of the header moon.

## [0.2.0] - 2026-09-23

### Added

- Location search that accepts a town or city name, a town with its state (for example, Big Lake, MN), or a ZIP code. Results come from the free Open-Meteo geocoding API, which needs no API key.
- Automatic fill of latitude, longitude, and time zone from the selected search result.
- A line under the search box showing the resolved place name, coordinates, and time zone in plain language (for example, Central Time).
- A match picker for ambiguous names, showing up to six results so the correct place can be selected.
- ZIP code handling that searches United States results first and falls back to a worldwide search if nothing matches.
- Clear error messages when a search finds no match or the location service can't be reached.
- Bookmark links that include the place name. A link containing only a place, such as `?place=Brainerd, MN`, runs the search when the page loads.
- A header scene with a night sky, a pine treeline reflected on the water, and a moon icon showing the current phase.
- Attribution for Open-Meteo and GeoNames in the page footer text.

### Changed

- Moved the Latitude, Longitude, and Time Zone fields into a collapsible "Enter coordinates instead" section.
- Editing Latitude or Longitude by hand now clears the search box and labels the spot as Custom coordinates.
- Use my location now clears the search box and labels the spot as Your location.
- Switched to a dark theme only. Forest greens are used for the page frame and buttons, water blues for major and minor periods, and amber for sunrise and sunset. Native date pickers also use dark styling.
- Lightened the minor period color so it stands out from the daylight band on the timeline bar.
- Prime notes are now highlighted in amber.
- The status line now reads "Showing N days," and the location appears in the resolved place line instead.
- Updated the intro text and the explanation at the bottom of the page.
- Clarified the latitude error message to explain that places closer to the poles are not supported.
- Printing now switches to a light color scheme suited for paper.
- Address bar updates are guarded so the page keeps working when opened as a local file.
- Removed the safe area padding and `viewport-fit=cover` setting, which were only needed for embedded hosting.

## [0.1.0] - Initial draft

### Added

- Solunar Times page calculating major and minor feeding periods, sunrise, and sunset entirely in the browser using Meeus-based sun and moon position math.
- Inputs for Latitude, Longitude, Time Zone, Start Date, End Date (up to 93 days), and Major and Minor period length.
- A daily card for each date with the moon phase and percent lit, a 24 hour timeline bar, and the time windows for each period.
- Prime notes when a major or minor period overlaps the hour before or after sunrise or sunset.
- Use my location button using the browser's location sharing.
- CSV download of the calculated times.
- Page address updates with each search so results can be bookmarked.
