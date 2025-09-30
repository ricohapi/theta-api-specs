# camera.\_getMetadata

### Overview

Shows the meta information for the specified still image.

### Support model

| X | Z1 | V | SC | S |
|:--|:--|:--|:--|:--|
| All | All | v2.00.2 and later | --- | --- |

### Parameters

| Name | Type | Description |
|:--|:--|:--|
| fileUrl | String | JPEG file ID |

### Results

| Name | Type | Description |
|:--|:--|:--|
| exif | Object | EXIF information in JSON format |
| xmp | Object | Photo Sphere XMP information in JSON format |

### exif

| Name | Type | Description |
|:--|:--|:--|
| ExifVersion | String | EXIF Support version |
| ImageDescription | String | Title or name |
| DateTime | String | Time created or updated |
| ImageWidth | Number | Width (px)<br>RICOH THETA X is not supported |
| ImageLength | Number | Height (px)<br>RICOH THETA X is not supported |
| ColorSpace | Number | Color space |
| Compression | Number | Compression format<br>RICOH THETA X is not supported |
| Orientation | Number | Image orientation |
| Flash | Number | Flash exposure |
| FocalLength | Number | Focal length |
| WhiteBalance | Number | White balance |
| ExposureTime | Number | Exposure time |
| FNumber | Number | F number |
| ExposureProgram | Number | Exposure program |
| PhotographicSensitivity | Number | Shooting sensitivity |
| ApertureValue | Number | Aperture value |
| BrightnessValue | Number | Brightness value |
| ExposureBiasValue | Number | Exposure compensation value |
| GPSLatitudeRef | String | Latitudinal direction of movement |
| GPSLatitude | Number | Latitude |
| GPSLongitudeRef | String | Longitudinal direction of movement |
| GPSLongitude | Number | Longitude |
| Make | String | Camera manufacturer |
| Model | String | Camera model |
| Software | String | Firmware software name |
| Copyright | String | Copyright |

### xmp

See [Photo Sphere XMP Metadata](https://developers.google.com/streetview/spherical-metadata/) for details on XMP.

| Name | Type | Description |
|:--|:--|:--|
| ProjectionType | Open Choice of Text | Projection type. Google currently only supports equirectangular. |
| UsePanoramaViewer | Boolean | Whether to display using the panorama viewer |
| CroppedAreaImageWidthPixels | Integer | Width of actual image (px) |
| CroppedAreaImageHeightPixels | Integer | Height of actual image (px) |
| FullPanoWidthPixels | Integer | Width (px) when the actual image size is based on a panoramic image |
| FullPanoHeightPixels | Integer | Height (px) when the actual image size is based on a panoramic image |
| CroppedAreaLeftPixels | Integer | Width (px) from the panoramic image of the actual image |
| CroppedAreaTopPixels | Integer | Height (px) from the panoramic image of the actual image |

### Restriction

This command cannot be executed during video recording.
