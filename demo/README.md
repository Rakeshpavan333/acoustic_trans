# Acoustic Texture Transfer using Neural Network and Short Time Fourier Transformation

This is a TensorFlow implementation of style transfer algorithm for audio. 

### How to run
- Open `nstf.ipynb` in Jupyter.
- In case you want to use your own audio files as inputs, first cut them to 10s length with:
```
ffmpeg -i yourfile.mp3 -ss 00:00:00 -t 10 yourfile_10s.mp3
```
- Set `CONTENT_FILENAME` and `STYLE_FILENAME` in the third cell of Jupyter notebook to your input files.
- Run all cells.

The most frequent problem is domination of either content or style in the output. To tackle this problem, adjust `ALPHA` parameter. Larger `ALPHA` means more content in the output, and `ALPHA=0` means no content, which reduces stylization to texture generation.

### References
- Original paper on style transfer:
[A Neural Algorithm of Artistic Style](https://arxiv.org/abs/1508.06576)
- [Neural style TensorFlow implementation](https://github.com/anishathalye/neural-style)
- Publications on texture generation with random convolutions:
 - [Extreme Style Machines](https://nucl.ai/blog/extreme-style-machines/)
 - [Texture Synthesis Using Shallow Convolutional Networks with Random Filters](https://arxiv.org/abs/1606.00021)
 - [A Powerful Generative Model Using Random Weights for the Deep Image Representation](https://arxiv.org/pdf/1606.04801)
