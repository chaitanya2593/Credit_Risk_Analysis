# Credit Risk Analysis


<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>  
    </li>
  <li><a href="#built-with">Built With</a></li>
    <li><a href="#code-usage">Code Usage</a>
      <ul>
        <li><a href="#DataScience">DataScience</a></li> 
      </ul>
    </li>
    <li><a href="#data-files">Data Files</a></li>
    <li><a href="#Deployment">Deployment</a>
      <ul>
        <li><a href="#Heroku-deployment">Heroku deployment</a></li>
        <li><a href="#app-Building ">App Building </a></li>
      </ul>
    </li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#reference">Reference</a></li>    

    
  </ol>
</details>


<!-- ABOUT THE PROJECT -->
## About The Project

![Product Name Screen Shot](https://github.com/chaitanya2593/Credit_Risk_Analysis/blob/main/overview.jpeg)

In this project explained how to implement the random forest on a credit risk data using jupyter notebook. Followed by deploying the model using the heroku.


<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Built With

* Python - 3x
  * Data science packages 
  * Dash
* Jupyter Notebooks  / google colabs
* HTML code 

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Code Usage  

Overall end-to-end process has been divided into 4 steps. The execution of the files should also be in the same order.
In individual the required input files are already mentioned in the code comments.

### DataScience
- 1_EDA.ipynb 
  - Performing teh exploratory data analysis on the credit risk data.    
- 2_Model_Buidling.ipynb
  - Building a Random forest model and saving the model as a file.  
- 3_Credit_Risk_Prediction.ipynb
  - Loading the model and predicting new data 
- 4 heroku deployment
  - The model is deployed as a app.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- DATA -->
## Data Files

The dataset for the project is extarcted from the kaggle competetion.
```sh
  https://www.kaggle.com/code/turanmehdiyeva/credit-risk-descriptive-statistical-analysis/data
  ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Deployment
- At first, during preprocessing the categorical variables label encoded and this encoding objects are stored by in label_dict.pkl and similar min_max_scaler.pkl file for the normalisation. 
- Then creating an account in heruko for free. Then created a dash python file named app.py(for convenience I used the generic name). As DASH uses flask, the app was built for a flask deployment and it doesn't support static files.
- As third step I have designed code to capture all the required fields for the model prediction.
- The model is tested locally just by invoking python file `python app.py`. 
- Now it is more of app deployment in heroku

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Heroku deployment
As a prerequsite, one should have the following things 
1. An account in the Heroku https://dashboard.heroku.com/


In the git folder one should below files
2. requirements.txt - with all the python packages required for app.
3. Procfile - an no extension file with command `web: gunicorn app:server` (if you are using different name for the main dash file please replace the same in the command)
4. Define which python runtime you want for your model in runtime.txt, Please also check if the runtime is compatible with heroku. 
5. Build the app.py with the required fields
6. Finally, push the code to the repo

 <p align="right">(<a href="#readme-top">back to top</a>)</p>

### App Building 
In this step it is more about deploying the app in heroku app. 

1. Login to Heroku and navigate to apps
2. create new app with the names available (be creative ).
3. Now navigate to the 'Deploy' tab and like your github under "Deployment method'"
4. Under Connect to Github -> please provide the repo name in which the app is placed
5. Under Manual Deploy -> please select tge branch and click "Deploy branch"
6. Once this is successfully done you should get the url to access the website. In my case it is - https://cr369.herokuapp.com/

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->
## License

Distributed under the GNU License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

Developed by Frankfurt School Data Science initiative members.

[LinkedIn](https://www.linkedin.com/company/fs-datascience/) | [Instagram](https://www.instagram.com/fs_datascience/)

Project Link: [https://github.com/chaitanya2593/CRA_pratice](https://github.com/chaitanya2593/CRA_pratice)

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## References:
- https://dash.plotly.com/deployment
- https://devcenter.heroku.com/articles/creating-apps



