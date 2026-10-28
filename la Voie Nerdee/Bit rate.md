*Bit rate* is the number of bits used to represent one second of a digital audio.

It is measured in kilobits per second (kbps) and is calculated by multiplying the [[bit depth]] by the [[sample rate]], then by the number of audio channels.

For example, a stereo 16-bit audio with a 44.1 kHz sample rate would have a bit rate of 1,411,200 bps, or 1411.2 kbps (16 × 44100 × 2).

## 🎛️ VBR vs CBR

### VBR

VBR (stands for *Variable Bit Rate*) dynamically changes the data rate based on audio complexity.

During a quiet pause or a constant note line, VBR drops the bitrate lower, while a loud, dense, or complex multi-instrumental chorus makes it raise the bitrate to preserve clarity.

This makes it possible to achieve clean, high-quality audio while keeping small overall file size.

### CBR

CBR (stands for *Constant Bit Rate*) uses the exact same amount of bits per second throughout the entire audio file, regardless of the complexity of an audio fragment.

CBR-encoded audio files are compatible with almost all audio playback devices, but the price for this compatibility is a larger file size comparing to VBR.





[^1]: Sources:
		https://www.waveroom.com/blog/bit-rate-vs-sample-rate-vs-bit-depth/
