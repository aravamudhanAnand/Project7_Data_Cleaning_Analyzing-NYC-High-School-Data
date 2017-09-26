For the purposes of this project, we will be using data about New York City public schools.

<h3>INTRODUCTION of the DATASET: </h3><br/>

One of the most controversial issues in the U.S. educational system is the efficacy of standardized tests, and whether they're unfair to certain groups. <br/>
The SAT, or Scholastic Aptitude Test, is an exam that U.S. high school students take before applying to college. Colleges take the test scores into account when deciding who to admit, so it's fairly important to perform well on it.

The test consists of three sections, each of which has 800 possible points. The combined score is out of 2,400 possible points (while this number has changed a few times, the data set for our project is based on 2,400 total points). Organizations often rank high schools by their average SAT scores. The scores are also considered a measure of overall school district quality.
We'll need to supplement our data with other sources to do our full analysis.

The same website has several related data sets covering demographic information and test scores.<br/>
Here are the links to all of the data sets we'll be using:

- SAT scores by school - SAT scores for each high school in New York City
- School attendance - Attendance information for each school in New York City
- Class size - Information on class size for each school
- AP test results - Advanced Placement (AP) exam results for each high school (passing an optional AP exam in a particular subject can earn a student college credit in that subject)
- Graduation outcomes - The percentage of students who graduated, and other outcome information
- Demographics - Demographic information for each school
- School survey - Surveys of parents, teachers, and students at each school

All of these data sets are interrelated. We'll need to combine them into a single data set before we can find correlations.

<h5> Note </h5><br/>
1. Only high school students take the SAT, so we'll want to focus on high schools.
2. New York City is made up of five boroughs, which are essentially distinct regions.
3. New York City schools fall within several different school districts, each of which can contains dozens of schools.
4. Our data sets include several different types of schools. We'll need to clean them so that we can focus on high schools only.
5. Each school in New York City has a unique code called a DBN, or district borough number.
Source: Dataquest.io

Steps:
1. Reading all csv and survey txt data files.
2. Making sure all datasets have a unique DBN.
if not, generate DBN code by concatenating two fields (eg. class_size dataset requires a DBN column by concatenating CSD and School code columns)
3. Create one column called SAT_SCORE to add ["SAT Math Avg. Score", "SAT Critical Reading Avg. Score", "SAT Writing Avg. Score"] column values.
4. Parse the latitude and longitude coordinates for each school. This will enable us to map the schools and uncover any geographic patterns in the data. 
5. Condense the class_size, graduation, and demographics data sets so that each DBN is unique.
6. Merge all datasets into one "Combined" dataset for further analysis.
