# Synthetic Image Data Downloader
This tool generates synthetic image data based on the specified seed value. The downloaded data contains images with 0-30% of red, green, and blue pixels, 0-20% noise represented as non-white pixels, and the undefined rest is represented as white pixels.

## Usage
```data_downloader.exe [--compression COMPRESSION] [--dataID DATAID] [--output_folder OUTPUT_FOLDER] [--no_metadata]```

## Arguments
`--compression`: (Optional) Image compression factor (0-50). Default is 0.
`--dataID`: (Optional) Seed value for random image generation. Default is 0.
`--output_folder`: (Optional) Path to the output folder where the generated data will be stored. Default is "./data".
`--no_metadata`: (Optional) If specified, metadata for each image will not be generated.

## Output
The script generates 20 PNG format images in the specified output folder. The filename format is `data_xxx.png`, where `xxx` is a zero-padded three-digit number.

## Metadata
If `--no_metadata` option is not specified, the script generates a text file for each image containing metadata. The filename format is `data_xxx_metadata.txt`, where `xxx` is a zero-padded three-digit number. The metadata includes the following information:

- `Image_size`: The size of the generated image.
- `Compression_factor`: The image compression factor specified by the user.
- `Data_ID`: The seed value specified by the user.
- `Noise_level`: The percentage of non-white pixels in the generated image.

## Example
To generate synthetic image data with compression factor 20, data ID 123, and output folder "./dowloaded_data", run the following command:

```data_downloader.exe --compression 20 --dataID 123 --output_folder "./dowloaded_data"```