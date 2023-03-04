# Image Cruncher
## Motivation
Using input photos or images, the application Image Cruncher analyzes them. It counts how many pixels of each color there are in one or more input image files, saving the results to a JSON file or printing them to the command line.

## Usage
```
image_cruncher.exe -i input_path [-it input_type] [-rgbo] [-o output_path]
```

## Arguments
|short|full|description|optional|
|-|-|-|-|
|`-i`|`--input`|The location of the input file or folder. All files of the chosen input type are loaded if folder is supplied rather than file.|NO|
|`-it`|`--input_type`|The type of input file(s). Supported types are: JPG, JPEG, GIF, PDF, PNG, TIFF, WebP.|YES|
|`-rgbo`|`--rgb_only`|Only counts pixels that are entirely red, green, and blue, if this option is selected. For instance, (254, 0, 0) counts as other category but (255, 0, 0) counts as red.|YES|
|`-h`|`--help`|Show help.|YES|


## Usage Examples
Read all of the JPG files in the "./input/ folder, analyze them using the RGB only mode, then output the results to the command line.

```image_cruncher.exe -i ./input -it jpg -rgbo```

Image input.png is read, examined, and the output is saved to output.json.

```image_cruncher.exe -i input.png -o output.json```

## Output
The output format for the results when printed or saved to a JSON file is as follows:
```
{
    "image_filename": {
        "color_1": count_1,
        "color_2": count_2,
        ...
    },
    "image_filename": {
        "color_1": count_1,
        "color_2": count_2,
        ...
    },
    ...
}
```