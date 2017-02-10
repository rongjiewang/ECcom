# ECcom
Error Correction compression

The compression algorithm have three steps:


Step 1: Using ECcom_Bloocoo for correcting the reads errors in minimizers.
              ECcom_Bloocoo -file reads.fastq -o reads_corrected.fastq

Step 2: Using ECcom_orcom_bin for distributing corrected reads and error infor into buckets.
              ECcom_orcom_bin <e|d> -i reads_corrected.fastq -o reads_corrected
            
Step 3: Using ECcom_orcom_pack for compressing within buckets.
              ECcom_orcom_pack <e|d> -i reads_corrected -o reads_corrected
