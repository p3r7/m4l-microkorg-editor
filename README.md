# m4l-microkorg-editor

Ableton microKORG editor w/ bidirectional editing.


## Usage

On the microKORG, set the value of `MIDI > LOCAL` to `EXTERNAL` or `AUTO`. The default value (`ON`) may cause glitches in the SysEx communication.

Use a quality MIDI interface, not a 5$ no-name one.
Cheap interfaces will scramble (if not filter entirely) SysEx and NRPN communication.

If you use a MIDI channel other than 1, modify the value of the `CHAN.` control in the lower right corner of the device. Ableton is smart enough to override the channel value for standard midi messages (e.g. when using the `Ext. Instrument` device) but will have to clue on how to do so for the proprietary SysEx messages.


## Next steps

- [ ] Vocoder support
- [ ] allow editing RO parameters (by forcing a complete SysEx dump onto the microKORG)


## Resources

SysEx parsing implemented using the [official microKORG MIDI implementation specs](http://i.korg.com/uploads/Support/MK1_633652915168960000.pdf).

Some additional information can be found in the [Owner's Manual](https://cdn.korg.com/us/support/download/files/8f226053113b3be59753dcce14e74cca.pdf).


## Acknowledgements

Based on [Microkorg editor 1.0](https://maxforlive.com/library/device/6404/microkorg-editor) by [@dru93](https://maxforlive.com/profile/user/dru93), itself a fork of [Korg MS-2000 2.0	](https://maxforlive.com/library/device/900/korg-ms-2000) by [@grymmjack](https://maxforlive.com/profile/user/grymmjack) ([gh](https://github.com/grymmjack)).

SysEx parsing code heavily inspired by [@Jeremy](https://cycling74.com/author/531ee78c4db05f8762373b5f)'s [Building a Synthesizer Editor with JavaScript, Part 3](https://cycling74.com/tutorials/building-a-synthesizer-editor-with-javascript-part-3) article.
