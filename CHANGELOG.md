# Changelog

## 1.0.0 — first release

- Lenses: spectrogram, waveform (plain / 3-band), spectrum bars at the playback position, loudness heatmap;
  the lens can be switched off.
- Metrics: up to four curves out of 16 (dynamics, level, loudness, stereo, spectrum) and 17 values, clipping /
  true-peak markers, phase correlation strip.
- Loudness, LRA and true peak per ITU-R BS.1770 / EBU R128, verified with the EBU Loudness Test Set and
  ITU-R BS.2217 (122/122 checks); multichannel files measured over all channels.
- DR per the TT DR Offline Meter algorithm (matches foo_dr_meter).
- Optional quality report: upsampling, lossy source, fake bit depth, clipping, DC offset, inter-sample peaks,
  mono compatibility.
- Per-panel settings and names, 9 built-in presets plus user presets, 19 color themes.
- Zoom and pan with finer re-analysis, multi-monitor fullscreen, image and analysis-sheet export.
- Playlist menu: analyze into the cache / remove from the cache; optional pre-analysis of the next track;
  memory and compressed disk cache.
- Default UI and Columns UI (panel and toolbar), 64 and 32 bit.
