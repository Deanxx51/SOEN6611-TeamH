# SOEN6611-TeamH

## Team members:
Hannan li  ID:40047659 
Tongwei Zhang ID:40044711 
Xiang Xie ID:40070841 
Yuhang Gao ID:40070438 

## Structure:
### "Commands" folder
contains the commands we used to run the tools for collecting the data.

### "Configurations" folder 
contains two folders, it contains the configurations of Code Coverage and Mutation Testing respectively.

### "Data_After_re-processing" folder 
contains 5 different folders named after 5 projects, in each of these folders it has the data after re-processing, which is used to do the data analysis.

### "Raw_Data" folder 
contains 5 different folders named after 5 projects, in each of these folders it has the raw data we got from the project.In "Metric(1,2,4)" folder, you can find the index.html in the folder, which you can see the raw data of code coverage and complexity from it.In "Metric3" folder, you can do the same way as above to see the raw data of Mutation Testing. For the Metric5, we provide with the screenshot to record our raw data. For the Metric6, because we manually detected the post-release bugs of different versions so we can only provide with the table which is used to record Metric6.

## Requirements:
1. For the collections of Metric 1,2 and 4, the jacoco plugin need to be added to pom.xml file.  
    > &lt;groupId&gt;org.apache.maven.plugins&lt;/groupId&gt;  
      &lt;artifactId&gt;maven-jar-plugin&lt;/artifactId&gt;  
      &lt;version&gt;0.8.2&lt;/version&gt;
   Also designed the output dictory and execution phase in plugin.
2. For the collections of Metrics 3, the pitest plugin need to be added to pom.xml file.
    > &lt;groupId&gt;org.pitest&lt;/groupId&gt;  
      &lt;artifactId&gt;pitest-maven&lt;/artifactId&gt;  
      &lt;version&gt;1.4.7&lt;/version&gt;
   Running the "mvn org.pitest:pitest-maven:mutationCoverage" could get the mutation report.
3. For Metric 5, the git command can get the Delta line of code of java file  
   "git diff --shortstat versionName1 versionName2 '*.java'"
4. For getting the LOC of java file, checkout to the version and running command  
   "git ls-files | grep "\.java$" | xargs cat | wc -l"   
For the script used to do the data analysis, you need to download R Console to do the work.
