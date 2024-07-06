# Shopper's Compass
<p>This project is a Django-based Tiktok recommendation system that utilizes a dataset scraped from Amazon to provide users with product recommendations. Below is a breakdown of the project's key components and functionalities:</p>

<ol>
  <li><strong>Project Structure:</strong> The Django project is divided into two apps: 'recommendationSystem' (the main app) and 'myApp'.</li>
  <li><strong>Data Scraping:</strong> Data was collected from Amazon to create a dataset containing various product details such as titles, categories, sub-categories, prices, ratings, and more. </li>
  <li><strong>Data Preprocessing:</strong> The scikit-learn library was used for data preprocessing, including feature transformation and computing the cosine similarity matrix.</li>
  <li><strong>Machine Learning Models:</strong> Trained models for clustering (K-Means) and DBSCAN were loaded using joblib for use in the recommendation system.</li>
  <li><strong>Recommendation Algorithm:</strong> The recommendation system uses K-Means clustering and cosine similarity. When a user inputs a product title, the system identifies the product's cluster and recommends other products within the same cluster based on cosine similarity scores.</li>
  <li><strong>Django Views:</strong> The 'myApp/views.py' file contains Django view functions to handle user requests. The 'home' view renders the main page, and the 'get_recommendations' function generates product recommendations. The 'recommend_products' view processes POST requests when a user submits a product title and displays the recommendations.</li>
  <li><strong>User Interface:</strong> HTML templates (index.html) were created for the user interface, featuring input fields for product titles and a section for displaying recommendations. Bootstrap is used for styling.</li>
  <li><strong>Routing and URLs:</strong> URL patterns are defined in the 'urls.py' files to route user requests to the appropriate views.</li>
  <li><strong>Data Display:</strong> Recommended products are shown in a responsive card layout, displaying details like title, category, sub-category, price, ratings, and total ratings.</li>
  <li><strong>Static Files:</strong> Static files, such as CSS, are loaded using {% static %} template tags.</li>
  <li><strong>Database:</strong> The project uses a pre-built dataset (data.pkl) and machine learning models loaded from joblib files instead of a traditional database for storing and retrieving product information.</li>
</ol>

<p>This Django E-commerce recommendation system employs machine learning to provide product recommendations based on user input and similarity scores, offering an interactive and user-friendly interface. Users can input a product title, and the system will suggest similar products based on clustering and similarity calculations.</p>

<h3> Follow these steps to run the Django-based E-commerce recommendation project:</h3>

<ol>
  <li><strong>Navigate to Project Directory:</strong> Open the command prompt or terminal and navigate to the project's root directory using the cd command. 
  <ul>
    <li>cd path/to/this/project</li>
  </ul>
  </li>
  <li><strong>Create a Virtual Environment:</strong> Create a virtual environment to manage the project's dependencies:
  <ul>
    <li>python -m venv myenv</li>
  </ul>
  </li>
  <li><strong>Activate the Virtual Environment:</strong> Activate the virtual environment:
  <ul>
    <li>myenv\Scripts\activate   (Windows)</li>
    <li>source myenv/bin/activate   (macOS/Linux)</li>
  </ul>
  </li>
  <li><strong>Upgrade Pip:</strong> Ensure you have the latest version of pip:
  <ul>
    <li>python.exe -m pip install --upgrade pip</li>
  </ul>
  </li>
  <li><strong>Install Django and Required Packages:</strong> Install Django and other necessary Python packages:
  <ul>
    <li>pip install django</li>
    <li>pip install numpy==1.23.5</li>
    <li>pip install pandas</li>
    <li>pip install joblib</li>
    <li>pip install scikit-learn==1.2.2</li>
  </ul>
  </li>
  <li><strong>Database Setup:</strong> Set up the database for the Django project by running:
  <ul>
    <li>python manage.py makemigrations</li>
    <li>python manage.py migrate</li>
  </ul>
  </li>
  <li><strong>Run the Development Server:</strong> Start the Django development server:
  <ul>
    <li>python manage.py runserver</li>
  </ul>
  </li>
  <li><strong>Access This Project:</strong> Open a web browser and go to http://localhost:8000/ to see the E-commerce recommendation system's home page.</li>
  <li><strong>Interact with the Recommendation System:</strong> On the home page, enter a product title and click the "Recommend" button to get product recommendations based on your input.</li>
</ol>

<p>Now, the Django Tiktok recommendation project should be running locally. Users can access the recommendation system through their web browsers and receive product recommendations based on their input.</p>
