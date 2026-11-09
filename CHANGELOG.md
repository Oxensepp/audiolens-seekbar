# Changelog

## 1.3.1

- **Bandwidth fixed:** tracks whose high frequencies fall off gradually (no lowpass) showed far too low a
  bandwidth, sometimes below 10 kHz – a lossy copy of the same track could show more than the lossless original.
  Lossy files at high sample rates counted encoder residue above the lowpass (AAC at 96 kHz: 34.4 instead of
  19.6 kHz).
- **Bandwidth explained:** for lossy files the readout names the encoder lowpass (*BW 19.6 kHz (encoder lowpass)*).
  In Compare the bandwidth column shows the loss against the reference in red, e.g. *19.6 kHz (−16.9) lowpass*.
- **Quality report:** a DC offset below −40 dBFS is now a note (blue) instead of a warning – inaudible and harmless.
  Lossy files no longer report *Upsampled* or *Resampled from 44.1 kHz*: their cutoff is the encoder's lowpass.
- New color theme **Amber** (night blue to amber). *Right-click → Appearance → Color theme*

## 1.3.0

- **Spectrum bars, much extended:** *Right-click → Lens → Spectrum bars options*
  - Live for streams, tracks of unknown length and excluded file types; optionally also for normal playback
    (*Use live audio while playing*).
  - Layouts: bottom-up, mirrored, stereo L top / R bottom, stereo L | R with the bass in the center or outside.
  - Frequency and level range, number of bars (auto, 16–256), octave and third-octave bands with standard center
    frequencies, A- or C-weighting (levels in dB(A) / dB(C)).
  - Response (fast, normal, smooth), peaks (classic, gravity, fade out), LED segments.
  - Timeline below the bars: waveform, progress bar or none; seeking only there.
  - Tooltip with band and level, optionally updating live.
  - Own preferences page: *Preferences → Audio Lens Seekbar → Spectrum bars*
- **Channel in every lens:** the waveform can show stereo, mix, left, right or side; single channels as signed,
  mirrored or half-wave. *Right-click → Lens → Waveform options*
- **Stereo spectrogram:** mirrored at 0 Hz (as before) or stacked with 0 Hz at the bottom of each half.
  *Right-click → Lens → Spectrogram options → Layout*
- **Guide lines:** your own frequencies (up to 8) and a common style (dotted, dashed, solid; width, color,
  opacity); also shown in Spectrum bars. *Spectrogram options → Guide lines*
- **Colors:** new color themes LCARS and Lagoon; own colors for waveform, spectrum bars and background; a theme
  for tracks without a cover in *Album art*; *Ensure contrast* keeps everything readable on any background.
  *Right-click → Appearance*
- **New built-in presets,** grouped as Analysis, Spectrum bars, Style and Retro: RTA (1/3 octave), Stereo Bars,
  Loudness Bars (A-weighted), Hi-Res Check, Stereo Image. *Right-click → Presets → Built-in*
- **Menus and preferences reorganized:** the context menu follows the preferences pages (*Appearance*: colors,
  playback position, transparency; *Display*: title, labels, behavior). Frequency labels, level scale and the new
  *Show channel labels (L/R)* now apply to all lenses. New preferences page *Appearance*; cache and pre-analysis
  moved to *Analysis*.
- The position marker can be drawn behind title, labels and values. *Appearance → Playback position → Marker →
  Behind text*

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
