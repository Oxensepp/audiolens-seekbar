# Changelog

## 1.1.0

- **Position marker** can be configured: width (down to a crisp 1 px line), color (white, theme color or your
  own), dark outline, smooth or whole-pixel movement. *Right-click → Display → Position marker*
- **Transparent background:** the panel can show the background of your layout or skin; the opacity of the lens
  is adjustable. *Right-click → Display → Transparent background*
- Darkening of the played part can be switched off. *Right-click → Display → Shade played portion*
- Loudness values are labelled LUFS-I, LUFS-M and LUFS-S.
- About 40 % smaller disk cache, and the new format is designed to stay valid in future versions. Cache files from
  1.0 are not reused: each track is analyzed once more.
- Several panels showing the same track (e.g. spectrogram and waveform) now share one analysis.
- Fixed: in Default UI layout editing mode, right-click shows the layout menu again (e.g. *Replace UI Element*).
- Fixed: the quality report badge shows its details even when tooltips are off; findings are also written to the
  console.
- Fixed: the loudness heatmap no longer repeats values that are already shown in the corner.

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
