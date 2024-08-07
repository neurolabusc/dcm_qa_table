
## About

dcm_qa_table is a simple DICOM to NIfTI validator script and dataset for the [TablePosition](https://github.com/rordenlab/dcm2niix/issues/726). For each manufacturer, At a minimum, two series are acquired. The position of the dataset is moved between series.

## DataSets

* Siemens/
  * source: Alexandre DAstous, Institut universitaire de gériatrie de Montréal (IUGM)
  * model: (0008,1090) Prisma fit
  * version: (0018,1020) syngo MR E1

* Philips/
  * source: Alexandre DAstous, Le Centre hospitalier de l'Université de Montréal (CHUM) 
  * model: (0008,1090) Achieva dStream
  * version: (0018,1020) 5.7.1\5.7.1.3

 * GE/
   * source: Jaemin Shin and Sagar Mandava, Emory Sports Performance & Research Center (SPARC)
   * model: (0008,1090) SIGNA Premier
   * version:  (0018,1020) 29\LX\RX29.1_R01_2111.a

   * Two exams collected with GE phantom landmarked via laser at 794 mm (exam1486) and 711 mm (exam1487) while the location of phantom unchanged in world coordinates. Note that the table landmarked at 794 mm moved further inside bore.
   * Each exam consists of two sets of 1 localizer and 3 fMRI in both feet-first (FFS) and head-first (HFS) (total 8 series) as below. Phantom & landmark remains unchanged between FFS and HFS.
   ```
      1. Localizer FFS 
      2. fMRI FFS - the SI coverage I11.1 – S15.9
      3. fMRI FFS - the SI coverage I21.1 – S10.9
      4. fMRI FFS - the SI coverage I01.1 – S25.9
      5. Localizer HFS
      6. fMRI HFS - the SI coverage I11.1 – S15.9
      7. fMRI HFS - the SI coverage I21.1 – S10.9
      8. fMRI HFS - the SI coverage I01.1 – S25.9
   ```
   * See [GEHC_BIDS_TablePosition_validation.pdf](https://github.com/mr-jaemin/ge-mri/blob/main/doc/GEHC_BIDS_TablePosition_validation.pdf) for details experiment setup, DICOM tags, and results.
    
