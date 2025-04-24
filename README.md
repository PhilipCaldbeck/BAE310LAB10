# BAE310LAB10

Laboratory 10: Python and AI
By: Philip Caldbeck
23 April 2025
Summary:


Materials:

Assembly Procedure:
Part 1:


Part 2:

Part 3:

Test Procedures:

Results:
Part 1 -  Map It:

Below you will find the prompts used to generate the code for Part 1:

Prompt 1
Goal: Access a CSV in JupyterLab, filter for unique water quality site names, and map their locations.
Model: ChatGPT (GPT-4)
Prompt:
"I have a .csv file that i want to access in jupyterlab, a python IDE. Use your preferred LLM AI to generate a Python function that accesses the database, filters
for the names of water quality measurement sites, and displays the location information for
all sites without repetition.
3. Use your preferred LLM AI to create a map that pinpoints the location of every station in the
database.
can you write a code for this please, just leave the file name something universal that i can update in the code with my actual file name, which is station.csv"

Prompt 2
Goal: Provide all CSV column headers from station.csv for reference in processing/filtering.
Model: ChatGPT (GPT-4)
Prompt:
"the names of the headers in the csv file are the following:
OrganizationIdentifier OrganizationFormalName MonitoringLocationIdentifier MonitoringLocationName MonitoringLocationTypeName MonitoringLocationDescriptionText HUCEightDigitCode DrainageAreaMeasure/MeasureValue DrainageAreaMeasure/MeasureUnitCode ContributingDrainageAreaMeasure/MeasureValue ContributingDrainageAreaMeasure/MeasureUnitCode LatitudeMeasure LongitudeMeasure SourceMapScaleNumeric HorizontalAccuracyMeasure/MeasureValue HorizontalAccuracyMeasure/MeasureUnitCode HorizontalCollectionMethodName HorizontalCoordinateReferenceSystemDatumName VerticalMeasure/MeasureValue VerticalMeasure/MeasureUnitCode VerticalAccuracyMeasure/MeasureValue VerticalAccuracyMeasure/MeasureUnitCode VerticalCollectionMethodName VerticalCoordinateReferenceSystemDatumName CountryCode StateCode CountyCode AquiferName LocalAqfrName FormationTypeText AquiferTypeName ConstructionDateText WellDepthMeasure/MeasureValue WellDepthMeasure/MeasureUnitCode WellHoleDepthMeasure/MeasureValue WellHoleDepthMeasure/MeasureUnitCode ProviderName"

Prompt 3
Goal: Analyze and visualize water quality data from a CSV by filtering on a characteristic and plotting each site over time.
Model: ChatGPT (GPT-4)
Prompt:
"Understand the results database downloaded from USGS.
a. Download the file named narrowresult.csv from the Canvas assignment.
b. Open the file using Excel or Google Sheets to examine its contents.
c. Take note of the headers and the types of information available in the database.
d. If you are using a cloud service, upload the file to your cloud environment.
2. Use your preferred LLM AI to generate a Python function that accesses the database, filters
for a desired water quality characteristic, and plots the results. Each site should be
represented as a separate line with a different color, where the Y-axis represents the
measured values and the X-axis represents time.
3. Ask the LLM AI to modify the code such that you can ask for two characteristics at the same
time."

Prompt 4
Goal: Ask for help understanding why a graph isn't displaying in JupyterLab and how to view it.
Model: ChatGPT (GPT-4)
Prompt:
"it doesnt do anything, am i missing something? how do i see the graph in jupyter ide?"

Prompt 5
Goal: Provide column headers for narrowresult.csv to help with filtering and plotting based on water quality characteristics.
Model: ChatGPT (GPT-4)
Prompt:
"here is the name of the headers:
OrganizationIdentifier OrganizationFormalName ActivityIdentifier ActivityStartDate ActivityStartTime/Time ActivityStartTime/TimeZoneCode MonitoringLocationIdentifier ResultIdentifier DataLoggerLine ResultDetectionConditionText MethodSpecificationName CharacteristicName ResultSampleFractionText ResultMeasureValue ResultMeasure/MeasureUnitCode MeasureQualifierCode ResultStatusIdentifier StatisticalBaseCode ResultValueTypeName ResultWeightBasisText ResultTimeBasisText ResultTemperatureBasisText ResultParticleSizeBasisText PrecisionValue DataQuality/BiasValue ConfidenceIntervalValue UpperConfidenceLimitValue LowerConfidenceLimitValue ResultCommentText USGSPCode ResultDepthHeightMeasure/MeasureValue ResultDepthHeightMeasure/MeasureUnitCode ResultDepthAltitudeReferencePointText ResultSamplingPointName BiologicalIntentName BiologicalIndividualIdentifier SubjectTaxonomicName UnidentifiedSpeciesIdentifier SampleTissueAnatomyName GroupSummaryCountWeight/MeasureValue GroupSummaryCountWeight/MeasureUnitCode CellFormName CellShapeName HabitName VoltismName TaxonomicPollutionTolerance TaxonomicPollutionToleranceScaleText TrophicLevelName FunctionalFeedingGroupName TaxonomicDetailsCitation/ResourceTitleName TaxonomicDetailsCitation/ResourceCreatorName TaxonomicDetailsCitation/ResourceSubjectText TaxonomicDetailsCitation/ResourcePublisherName TaxonomicDetailsCitation/ResourceDate TaxonomicDetailsCitation/ResourceIdentifier FrequencyClassInformationUrl ResultAnalyticalMethod/MethodIdentifier ResultAnalyticalMethod/MethodIdentifierContext ResultAnalyticalMethod/MethodName ResultAnalyticalMethod/MethodUrl ResultAnalyticalMethod/MethodQualifierTypeName MethodDescriptionText LaboratoryName AnalysisStartDate AnalysisStartTime/Time AnalysisStartTime/TimeZoneCode AnalysisEndDate AnalysisEndTime/Time AnalysisEndTime/TimeZoneCode ResultLaboratoryCommentCode ResultLaboratoryCommentText ResultDetectionQuantitationLimitUrl LaboratoryAccreditationIndicator LaboratoryAccreditationAuthorityName TaxonomistAccreditationIndicator TaxonomistAccreditationAuthorityName LabSamplePreparationUrl ProviderName"

Part 2 - What's Trending:

Goal: Understand the structure of the USGS results dataset and begin building a plotting function for it.
Model: ChatGPT
Prompt:
Understand the results database downloaded from USGS.
a. Download the file named narrowresult.csv from the Canvas assignment.
b. Open the file using Excel or Google Sheets to examine its contents.
c. Take note of the headers and the types of information available in the database.
d. If you are using a cloud service, upload the file to your cloud environment.
2. Use your preferred LLM AI to generate a Python function that accesses the database, filters for a desired water quality characteristic, and plots the results. Each site should be represented as a separate line with a different color, where the Y-axis represents the measured values and the X-axis represents time.
here are the headers in my .csv:

Ask the LLM AI to modify the code such that you can ask for two characteristics at the same time.

Goal: Automatically adjust the scale based on the type of characteristic being plotted.
Model: ChatGPT
Prompt: I'm still getting this error for pH, can we adjust this value based upon the scale of what I type in?

Goal: Resolve an error involving the steps argument in MaxNLocator for pH.
Model: ChatGPT
Prompt: It pasted the graph, but I still got this error.

Goal: Avoid label overlap without fixing the step size to a specific value like 0.1.
Model: ChatGPT
Prompt: We don't have to set the scale to 0.1, it can be set to whatever makes sense for the variable we want (pH, nitrate, etc,) I just don't want the labels to blur together.

Goal: Plot two variables on the same time axis, and label both characteristics on the y-axis.
Model: ChatGPT
Prompt: What if I want to display two values at the same time. Can you prompt if I want 1 or 2 values, and then ask me to input the values I want. For example:

Goal: Ensure each y-axis is labeled correctly when two characteristics are plotted.
Model: ChatGPT
Prompt: On the y axis, when I input two values, it gives me "value". I want that axis to display the two variables that I input.

Goal: Display each of the two selected characteristics on separate y-axes for better scale readability.
Model: ChatGPT
Prompt: I actually want one input to plot on the left side of the graph, and one input to plot on the right side. That way, if I compare say arsenic to aluminum, their values might be vastly different but the graph is still able to be interpreted.

Part 3 - Streamlit

Goal: To generate a Streamlit app that allows the user to upload both databases, search for a contaminant in the databases, define the range of values and dates, and display a map and trend over time.

Model: ChatGPT-4

Prompt: "In this section your goal is to develop a Streamlit app that allows the user to upload both databases used in Part 1 and 2, to search for a contaminant in the databases. Once a contaminant has been selected you should be able to define the range of values and dates that you want to show. After modifying the ranges, update the map showing the location of the

stations with the contaminant within that range and measured during the time frame. It should also show you a trend over time of the contaminant in all the stations shown.

b. Ask your preferred LLM AI to help you generate the app for streamlit and copy and paste the result under the streamlit_app.py file. You will be able to run the app as soon as it is saved."

Goal: To ask for help in generating a Streamlit app to load, filter, and visualize data related to water contaminants.

Model: ChatGPT-4
Prompt: "can you generate a streamlit app for me? I need it to load the water quality datasets (station and narrowresult) and let me filter by a contaminant, date, and value range. Then display a map and a trend graph of the filtered data."
Goal: To ask how to set up and install dependencies for a Streamlit app when using GitHub online.

Model: ChatGPT-4
Prompt: "how do i install the dependencies if im using github. can i save the github to my computer manually?"
Goal: To get clarification on how to install dependencies for a Streamlit app while using GitHub directly.

Model: ChatGPT-4
Prompt: "can i type the dependencies into the .py file i created?"
Goal: To ask about installing dependencies in a GitHub repository through an online interface, and if dependencies need to be manually installed on a local machine.

Model: ChatGPT-4
Prompt: "im using github online"
Goal: To clarify how to install required Python packages using a requirements file for a Streamlit app in an online GitHub setup.

Model: ChatGPT-4
Prompt: "how do i type the dependencies into requirements.txt if im using github online?"
Goal: To verify whether the pip install -r requirements.txt command should be typed in Streamlit or somewhere else.

Model: ChatGPT-4
Prompt: "where do i type this? in streamlit? pip install -r requirements.txt"
Goal: To find a solution for installing dependencies when using GitHub and whether downloading the repository locally is necessary.

Model: ChatGPT-4
Prompt: "im using github online, where do i type this?"
Goal: To seek guidance on how to upload and access CSV files from GitHub in a Streamlit app.

Model: ChatGPT-4
Prompt: "should i upload the csv file to github?"
Goal: To troubleshoot the FileNotFoundError related to loading CSV files in the Streamlit app.

Model: ChatGPT-4
Prompt: "FileNotFoundError: [Errno 2] No such file or directory: 'path_to_database1.csv'"
Goal: To resolve the issue of loading CSV files correctly in the Streamlit app, with clarification on file paths and naming conventions.

Model: ChatGPT-4
Prompt: "this is the path: narrowresult.csv"
Goal: To update the Streamlit app's code for correct handling of file paths and Streamlit-specific caching.

Model: ChatGPT-4
Prompt: "can you provide a code with all of these changes"
Goal: To learn how to verify the location of CSV files used in the Streamlit app.

Model: ChatGPT-4
Prompt: "how do i verify where the .csv are located?"
Goal: To clarify where the CSV files should be located for correct app execution in a GitHub-based setup.

Model: ChatGPT-4
Prompt: "this is the path: narrowresult.csv"
Goal: To resolve an error related to deprecated Streamlit caching methods (st.cache) and switch to the updated caching system (st.cache_data).

Model: ChatGPT-4
Prompt: "st.cache is deprecated and will be removed soon. Please use one of Streamlit's new caching commands, st.cache_data or st.cache_resource."
Goal: To resolve the error of FileNotFoundError while loading the CSV file in the Streamlit app.

Model: ChatGPT-4
Prompt: "FileNotFoundError: [Errno 2] No such file or directory: 'path_to_database1.csv'"

Conclusion:
