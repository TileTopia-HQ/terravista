# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.0] — 2025-07-14

### Added

- **Camera model** — Continuous zoom (0–22), bearing, pitch, Web Mercator projection, viewport-aware tile range calculation.
- **Gesture recognition** — Multi-touch state machine (pan, pinch-zoom, rotate, tilt) with camera delta output.
- **Tile cache** — LRU eviction with configurable size limits (256 MB / 50K tiles), per-region offline pre-fetch, URL template system.
- **Offline vector store** — On-device feature CRUD with GeoJSON geometry, sync status tracking (Synced/PendingCreate/PendingUpdate/PendingDelete/Conflict), bbox queries, GeoJSON export.
- **Style engine** — Mapbox GL-compatible style definitions with zoom-level interpolated properties, Fill/Line/Symbol/Circle/Raster layer types.
- **Turn-by-turn navigation** — On-device route tracking, step-by-step instructions, off-route detection (50m threshold), arrival notification.
- **Location service** — GPS coordinate model, haversine distance/bearing, tracking modes (None/Follow/FollowWithHeading/FollowWithCourse), abstract `LocationProvider` trait.
- **Render pipeline** — Frame-based command buffer (Clear/DrawRasterTile/DrawVectorLayer/DrawLocationMarker/DrawRoute), visible tile placement calculation, HiDPI awareness.
- **C FFI bindings** — 15 exported functions via `terravista-ffi` crate (cdylib + staticlib), `tv_` prefixed flat C API for Swift/Kotlin consumption.
- **Documentation** — Comprehensive README with architecture, API reference, platform integration examples. GitHub Pages landing site.

[0.1.0]: https://github.com/TileTopia-HQ/terravista/releases/tag/v0.1.0
