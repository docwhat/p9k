Prototyping ideas for PowerLevel9K
==================================

This repo is about prototyping some ideas for [PowerLevel9k](https://github.com/bhilburn/powerlevel9k); a configurable prompt system.

## Usage

You have several approaches, depending on your plugin manager or preference.

The easiest is just `source ./p9k.theme`.  This can be re-run and will flush any cached p9k functions.

Alternatively, add the `functions/` directory to your `fpath` and use the normal prompt system to load it.

Configuration
-------------

There are three array variables that you can set:

- `p9k_left_segments` — The left prompt (aka `$PROMPT` or `$PS1`).
- `p9k_right_segments` — The right prompt (aka `$RPROMPT`).
- `p9k_xtrace_segments` — The `XTRACE` prompt; activated via `set -x`.

Each element in the segments arrays is of the form `<name>::<fg>::<bg>`:

- `<name>` The name of the segment. The complete list can be found via `functions/p9k_segment_<name>`.
- `<fg>` The foreground color. Use the color names or the numbers from 0 to 255 if your terminal has 256 colors.
- `<bg>` The background color. Use the color names or the numbers from 0 to 255 if your terminal has 256 colors.
