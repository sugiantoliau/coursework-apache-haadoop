### Set up Single-Node Hadoop


Download hadoop-3.2.3.tar.gz to your theia environment by running the following command.
'''
curl https://dlcdn.apache.org/hadoop/common/hadoop-3.3.6/hadoop-3.3.6.tar.gz --output hadoop-3.3.6.tar.gz
'''


Extract the tar file in the currently directory.
'''
tar -xvf hadoop-3.3.6.tar.gz
'''


Navigate to the hadoop-3.3.6 directory.
'''
cd hadoop-3.3.6
'''


Check the hadoop command to see if it is setup. This will display the usage documentation for the hadoop script.
```
bin/hadoop
'''

Run the following command to download data.txt to your current directory.
'''
curl https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-BD0225EN-SkillsNetwork/labs/data/data.txt --output data.txt
'''


Run the Map reduce application for wordcount on data.txt and store the output in /user/root/output
'''
bin/hadoop jar share/hadoop/mapreduce/hadoop-mapreduce-examples-3.3.6.jar wordcount data.txt output
'''


Once the word count runs successfully, you can run the following command to see the output file it has generated.

You should see part-r-00000 with _SUCCESS indicating that the wordcount has been done.

'''
ls output
'''


Run the following command to see the word count output.
'''
cat  output/part-r-00000
'''
