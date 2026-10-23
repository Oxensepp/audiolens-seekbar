# Changelog

## 1.2.0

- **Audio Lens Compare:** compare up to six versions of a song (e.g. original, remaster, vinyl, hi-res) in a window
  of their own. Select 2–6 tracks in a playlist and choose *Audio Lens → Compare* (or *View → Audio Lens
  Compare*).
  - The versions are aligned automatically, even with different pauses or speed (vinyl, PAL). All lanes share
    one timeline and marker; click a lane or press 1–6 to continue in another version at the same spot (A/B).
  - *Overlay* view: short-term loudness of all versions, the average third-octave spectrum or its difference to
    a reference version, optionally at equal loudness.
  - Any version can be the reference: alignment and the spectrum difference are measured against it. Click
    the circle in the *Ref* column to switch.
  - Table with LUFS-I, LRA, DR, true peak, PLR, bandwidth, alignment and quality findings; versions can be
    hidden.
  - Export a comparison sheet as PNG or to the clipboard.
  - Labels, default view and reference rule: *Preferences → Audio Lens Seekbar → Compare*.
- **Playback highlight:** lens and curves (default), lens reversed (the upcoming part is darker), curves only or
  off. Replaces *Shade played portion*. *Right-click → Display → Playback position → Highlight*
- The position marker can be hidden. *Right-click → Display → Playback position → Marker → Show marker*
- Waveform: L/R labels and the center line can be hidden. *Right-click → Lens → Waveform options*
- Freely adjustable level range (upper and lower limit). *Right-click → Lens → Spectrogram options → Level range
  → Custom…*
- Values and curve labels optionally without units. *Preferences → Audio Lens Seekbar → Metrics*
- Middle click: fullscreen (default), play / pause or nothing. *Right-click → Display → Middle click*
- Analysis by file type: all files, all except a list, or only a list — e.g. to skip slow-to-decode DST or
  video files; excluded tracks still work as a seekbar. *Preferences → Audio Lens Seekbar → Analysis*
- The adaptive album art theme follows the brightness of the cover: dark covers no longer give bright colors.
- Faster and sharper lens when zooming, panning and resizing.
- Smoother position marker on high refresh rate monitors, and less drawing load.
- *Follow playback* no longer moves a zoomed view while paused.

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
