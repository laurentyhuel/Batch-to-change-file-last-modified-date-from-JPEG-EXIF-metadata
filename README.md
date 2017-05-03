# Batch to change file last modified date from JPEG EXIF metadata

## Description
When you moved your pictures for instance with scp or ftp, you loose picture date. This command help you to use date saved in JPG EXIF set by camera, as last modified date of file.

## Exiv2
The EXIF handling tool exiv2 has a builtin option for this

## Script

In command-line, go to root folder of your images.

Install exiv2:
```bash
sudo apt install exiv2
```

Find all your images with extension JPG and replace last modified date with JPG EXIF medadata:
```bash
find -name '*.JPG' -exec exiv2 -T rename {} \;
```
