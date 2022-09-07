`ORG.SGF:`
![GitHub release (latest by date)](https://img.shields.io/github/v/release/Special-graphic-formats/itw)
![GitHub Release Date](https://img.shields.io/github/release-date/Special-graphic-formats/itw)
![GitHub repo size](https://img.shields.io/github/repo-size/Special-graphic-formats/itw)
![GitHub all releases](https://img.shields.io/github/downloads/Special-graphic-formats/itw/total)
![GitHub](https://img.shields.io/github/license/Special-graphic-formats/itw)  

# ITW

### Playing with lossy image compression based on tile prediction and the discrete wavelet transformation

Quick start:

Encode [PNM](https://en.wikipedia.org/wiki/Netpbm) picture file to ```encoded.itw```:

```
./itwenc smpte.ppm encoded.itw
```

Decode ```encoded.itw``` file to ```decoded.ppm``` picture file:

```
./itwdec encoded.itw decoded.ppm
```

Watch ```decoded.ppm``` picture file in [feh](https://feh.finalrewind.org/):

```
feh decoded.ppm
```

### Adjusting quantization

Use quantization values instead of the default ```128 32 32``` values:

```
./itwenc smpte.ppm encoded.itw 64 32 16
```

### Use different wavelet

Use the reversible integer [Haar wavelet](https://en.wikipedia.org/wiki/Haar_wavelet) instead of the default ```0``` [CDF](https://en.wikipedia.org/wiki/Cohen%E2%80%93Daubechies%E2%80%93Feauveau_wavelet) 9/7 wavelet for lossless compression:

```
./itwenc smpte.ppm encoded.itw 128 32 32 1
```
