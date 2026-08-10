# Experiment 1: Evidence Acquisition Using AccessData FTK Imager

## Aim

To acquire a forensic disk image from a physical storage device using AccessData FTK Imager and verify the integrity of the acquired image using MD5 and SHA1 hash values.

## Software Used

- AccessData FTK Imager 4.7.1.2
- Windows

## Introduction

FTK Imager is a computer forensic tool developed by AccessData. It is used for acquiring and analyzing digital forensic evidence.

FTK Imager can acquire:

- Volatile memory (RAM)
- Non-volatile memory such as hard disks and USB drives
- Physical drives
- Logical drives
- Image files
- Contents of folders
- CDs/DVDs

In this experiment, a physical USB storage device was acquired and converted into a forensic disk image.

## Procedure

### Step 1: Open FTK Imager

Open **AccessData FTK Imager 4.7.1.2**.

Navigate to the option for creating a disk image.


### Step 2: Select Evidence Source

Select **Physical Drive** and click **Next**.


### Step 3: Select Physical Drive

Select the physical drive that needs to be acquired.

The device used in this experiment was:

**SanDisk Cruzer Blade USB Device**

Click **Finish**.


### Step 4: Select Image Type

Select **Raw (dd)** and click **Next**.


### Step 5: Enter Evidence Information

The following evidence information was entered:

- Case Number: 1
- Evidence Number: 1
- Unique Description: DF
- Examiner: SAI RAM
- Notes: EXP 1

Click **Next**.


### Step 6: Select Image Destination

The image was saved in the following destination:

`D:\3-1\Digital Forensics`

Image Filename:

`diskimage`

Image Fragment Size:

`0 MB`


### Step 7: Create Image

The source and destination information were displayed.

The option **Verify images after they are created** was selected.

Click **Start** to begin the acquisition.


### Step 8: Image Acquisition

FTK Imager started creating the forensic image from the physical drive.


### Step 9: Image Verification

After acquisition, FTK Imager verified the created forensic image.

The verification process checks the integrity of the acquired image using hash values.


### Step 10: Verification Result

The verification result showed:

- MD5 Verify Result: **Match**
- SHA1 Verify Result: **Match**
- Bad Blocks: **No bad blocks found in image**


### Step 11: Image Summary

The image summary provided details about the acquired physical drive.

Important information included:

- Source Type: Physical
- Drive Model: SanDisk Cruzer Blade USB Device
- Drive Interface Type: USB
- Source Data Size: 59112 MB
- Sector Count: 121061376
- Bytes per Sector: 512


### Step 12: Hash Verification

The image summary showed that the computed and reported hash values matched.

**MD5:**

`9f1f7659712cde7bc536dd82f341b5ce`

**SHA1:**

`abaca319c85c310078f410c02f6b11951af63334`

Both verification results were **Match**.

![Hash Verification]

## Result

The physical USB drive was successfully acquired using **AccessData FTK Imager 4.7.1.2** and converted into a **Raw (dd) forensic image**.

The acquired image was successfully verified using MD5 and SHA1 hash values.

## Verification Results

| Parameter | Result |
|---|---|
| Image Type | Raw (dd) |
| Source | Physical Drive |
| Device | SanDisk Cruzer Blade USB Device |
| Source Size | 59112 MB |
| MD5 Verification | Match |
| SHA1 Verification | Match |
| Bad Blocks | No bad blocks found |

<img width="694" height="493" alt="image" src="https://github.com/user-attachments/assets/38caed7d-fd82-42ab-89ec-bdd41abc8608" />
<img width="685" height="492" alt="image" src="https://github.com/user-attachments/assets/10464b38-7710-4ea9-a726-ddab35dd5b52" />
<img width="679" height="550" alt="image" src="https://github.com/user-attachments/assets/926e125b-f7bd-4676-93a8-8ea0407a1c7b" />
<img width="342" height="241" alt="image" src="https://github.com/user-attachments/assets/b1d2741e-1ae7-4e6e-acd3-0641ad8f99ea" />
<img width="619" height="643" alt="image" src="https://github.com/user-attachments/assets/0b5dfafb-5af8-4acd-b113-922fd89aff98" />
<img width="702" height="598" alt="image" src="https://github.com/user-attachments/assets/e77752db-599f-4728-8a8c-a8361d855f1d" />
<img width="1280" height="942" alt="image" src="https://github.com/user-attachments/assets/940fe7af-d36c-4833-ad0c-99270a818ea1" />


<img width="679" height="543" alt="image" src="https://github.com/user-attachments/assets/8feeb81e-3a6b-4161-8cb9-74af59c68797" />

