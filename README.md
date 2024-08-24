# Matchminds-
Tinder Like Dating App
MatchmindApp
Table of Contents
1. Features
2. Requirements
3. Installation
4. Usage
5. Matching Algorithm
6. Database Structure and Generation
7. Libraries Used
8. Contributing
9. License
10. Contact
Features
- User Profiles: Create and edit your profile with personal information such as age, gender, location, interests, and more.
- Matchmaking: Browse recommended matches based on your preferences and interact by liking or disliking profiles.
- Dynamic Updates: User matches are dynamically updated in the database, ensuring accurate matchmaking and user interactions.
- Password Protection: Secure your profile with a password during the signup process.
Requirements
- Python 3.6 or higher
- Tkinter (usually included with Python installations)
- SQLite (included with Python's standard library)
Installation
1. Clone the repository:
git clone https://github.com/yourusername/MatchmindApp.git
cd MatchmindApp
2. Install dependencies:
Since this app primarily uses Python's standard libraries, there are no additional dependencies. However, ensure Python and Tkinter are properly installed.
3. Run the application:
python main.py
Usage
1. Starting the Application: Launch the app using the instructions above. You'll be greeted with a login page that allows you to either log in with existing credentials or sign up for a new account.
2. Creating a Profile: Fill in your details on the signup page, including personal information and preferences. Set a secure password to protect your profile.
3. Browsing Matches: Once logged in, navigate to the main page to view recommended matches. You can like or dislike profiles, and the app will dynamically update your matches.
4. Editing Your Profile: Access your profile settings to make any updates to your information or preferences.
Matching Algorithm
MatchmindApp uses a combination of filtering and similarity scoring to generate match recommendations.

- Filtering by User Preferences: The app filters potential matches based on the user’s gender preference, age range, and location preference. This initial filtering ensures that users see profiles that align with their basic preferences.
- Cosine Similarity: After filtering, the app calculates the cosine similarity between user profiles based on shared interests. The cosine similarity measures how similar two users are in terms of their interests, ranging from 0 (no similarity) to 1 (perfect similarity). This score helps rank the filtered profiles, showing users those who are most similar to them first.
- Dynamic Updating: Once a user likes another user’s profile, the system checks if the feeling is mutual. If both users like each other, they are added to each other's match list. The matches are dynamically updated, ensuring real-time synchronization across profiles.
Database Structure and Generation
Database Structure
MatchmindApp uses an SQLite database to store user information and match data. The key tables and columns include:
- Users:
 - user_id (Primary Key)
 - name
 - age
 - gender
 - location
 - interests
 - password
 - and more...

- Matches:
 - Stores information about user matches, likes, and dislikes.
For more details on the database schema, refer to the `database.py` file in the repository.
Random Database Generation
To facilitate testing and development, MatchmindApp includes a feature for generating random user data. This process helps populate the database with diverse user profiles, allowing developers to test the app’s functionality under various scenarios.

- Data Generation: The app uses predefined lists of names, interests, jobs, and other attributes to randomly generate user profiles. Each profile is assigned a unique user_id, and other attributes are filled with random selections from these lists.
- Ensuring Matches: The random data generation process also includes logic to ensure some users have matches. The algorithm selects random pairs of users and adds them to each other’s liked list if they are compatible based on their preferences.
Libraries Used
MatchmindApp relies on several Python libraries for its functionality:

- **Tkinter**: Used for creating the graphical user interface (GUI).
- **SQLite**: A lightweight, disk-based database that doesn’t require a separate server process and allows access using a nonstandard variant of the SQL query language.
- **random**: Used to generate random data for populating the database with user profiles.
- **math**: Utilized for mathematical functions such as calculating cosine similarity.
Contributing
We welcome contributions to MatchmindApp! To contribute:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes and push to your fork.
4. Submit a pull request with a description of your changes.

