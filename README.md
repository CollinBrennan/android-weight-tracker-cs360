# Android Weight Tracker App

**Briefly summarize the requirements and goals of the app you developed. What user needs was this app designed to address?**
This app allows the user to set a goal for a weight they would like to reach and log their weight every day.

**What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?**
The app has 3 main screens which are the login screen, the home screen, and the settings screen. The home screen contains the number input where the user logs their weight for the day, as well as a table displaying past logs. The setting screen allows the user to adjust their weight goal as well as if they would like to recieve SMS notifications when they hit their goal. I believe my designs were successful by creating a simple and intuitive user interface.

**How did you approach the process of coding your app? What techniques or strategies did you use? How could those techniques or strategies be applied in the future?**
The process of my app usually began with outlining the feature I would like to implement, researching a solution, and then attempt to actually implement it. Research was usually a mix of reading the Android documentation or looking at posts on StackOverflow if I had a specific bug that I did not know how to fix. This wound up being a really good workflow and I will probably use it going forward.

**How did you test to ensure your code was functional? Why is this process important, and what did it reveal?**
To ensure the code was functional, I made heavy use of Logcat which allowed me to see the output of the app in the console. I also used the Android emulator to test UI functionality like pressing buttons, navigation, and receiving notifications.

**Consider the full app design and development process from initial planning to finalization. Where did you have to innovate to overcome a challenge?**
One challenge that I had to overcome was working with multiple threads. Because most processes run on the main thread by default, I had to be careful about not blocking the UI from updating. Since the app makes a lot of calls to a local database, using the Room library made sense since it ensures no database calls are ever accessed on the main thread.

**In what specific component of your mobile app were you particularly successful in demonstrating your knowledge, skills, and experience?**
A component I found great success with is the calls to the local database using the Room library and updating the UI automatically using LiveData. This can be seen on the home screen of the app where after the user logs their weight for the day, the database is updated and then a callback function fires which updates the logs table in real time.
