## 3D volume generation from DICOM images
This code describes different ways of reading DICOM images.

#### Using 'ImagePositionPatient' attribute
* Function `get_dcm` reads dicom files from a directory
* It first checks if the DICOM images have `ImagePositionPatient` attribute. If it has, it stores slices according to the `ImagePositionPatient`. Otherwise, it sorts by name.
* Input parameter:
    `dcm_path`: location of dcm data
    
* Output:
    Returns -   
     `dcm_data`: dicom data in a single array <br>
     `pix_spacing`: spacing of pixel/voxel <br>
     `intensity`: min and max intensity <br>


#### Using 'SliceLocation' attribute
* Function `get_dcm` reads dicom files from a directory
* It first checks if the DICOM images have `SliceLocation` attribute. If it has, it stores slices according to the `SliceLocation`. Otherwise, it sorts by name.
* Input parameter:
    `dcm_path`: location of dcm data
    
* Output:
    Returns -   
     `dcm_data`: dicom data in a single array <br>
     `pix_spacing`: spacing of pixel/voxel <br>
     `intensity`: min and max intensity <br>

Author @ Mrinal Kanti Dhar

#### Requirements
* `numpy`
* `pydicom`