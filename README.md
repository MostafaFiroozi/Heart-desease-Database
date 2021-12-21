# Heart_desease_Database
**The first page:**

The first form that the user can see, is the one related to choose his role. If the user has not signed up yet, he can use the button &quot;Register Now&quot;, which brings the new user to the part where he can enter his data to sign up.

![image](https://user-images.githubusercontent.com/73081215/146919819-ec53bdcf-9881-495a-ab84-043c80ab9eb8.png)

**Patient Login:**

For example, if the user choose &quot;PATIENT&quot;, a login page like this will be shown, in which he should enter his username and password. If it is not correct, the system will want him to enter the re-enter data with correct information, otherwise, a &quot;Correct Username And Password&quot; massage will appear, after which he will see his homepage.

![image](https://user-images.githubusercontent.com/73081215/146919849-4743e93e-ca0c-4739-925e-ce580b7f8701.png)

![image](https://user-images.githubusercontent.com/73081215/146919867-8f29ce0f-ef96-4377-afa3-cc2b057ef291.png)

As the VBA code depicts, after entering the login data, the the system search the table User\_info to check whether this is correct or not. For that we used DLookup function.

In the case of correct login info, a page like the below image will appear, in which the patient can choose between the different options that he can choose. With DoCmd.RunSQL, we run to sql codes to add the log data (the peron who logged in the sytem and the time of the login) to the table System\_logs. Thechnical addministrative then can use this data to visualize the system logs.

![image](https://user-images.githubusercontent.com/73081215/146919891-9d01a75f-3e9b-4245-b163-c56dbe2209fd.png)

**Statistics:**

In the statistics form, the patient or the doctor can choose a time period in which they want to visualize a specific statistic. In this example, we wanted to see the systolic value of the blood pressure for patient number zero. As you can see, the temporal trend as well as the minimum, maximum, and the average of that parameter is shown in the table. If they click on &quot;Show Abnormalities&quot;, it will go to the the form related to the abnormalities.

![image](https://user-images.githubusercontent.com/73081215/146919918-8bdea0bb-846a-4e42-9937-5ae7351c4303.png)

In the query for the statistics, we receive the data with specified attributes from the parameters table. Then we feed a chart with the output data of this query to visualize the temporal trend of the parameters.

![image](https://user-images.githubusercontent.com/73081215/146919933-9219a8d0-15fa-490e-9c6c-570cc7110456.png)

![image](https://user-images.githubusercontent.com/73081215/146919963-4013c76e-b69d-4f5a-a940-c707ecbf8234.png)

In the query for calculation of the min, max, and average. We received data with same attributes, and we have calculated the required values using SQL functions.

**Abnormalities:**

In the form related to the abnormalities, we can show all the parameters greater than the threshold set by the doctor for them, with the date at which they have been inserted.

![image](https://user-images.githubusercontent.com/73081215/146919975-65d19eea-3d76-4984-8c16-39402b5d70b1.png)
