# NeoNutrilife website.

mail management: https://privateemail.com/

domain management: https://www.namecheap.com/


# Publishing to gcloud

The site is hosted in Google Cloud in a public bucket with a load balancer in front of it. To publish updates to site for now I am using command line gsutil but in the future I might introduce a github action, for now use the following command to sync the full contents of the site: 

`gsutil rsync -R NeoNutrilife gs://www.neonutrilife.com`

the downiside of this is that it also synchronize the .git folder which is not necessary so we have to remove it later.

To send a single file one can use the gsutil cp command:

`gsutil cp app-ads.txt gs://www.neonutrilife.com`
