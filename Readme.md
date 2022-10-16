# Credit Risk Analysis


<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#code-usage">Code Usage</a></li>
    <li><a href="#data-files">Data Files</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#reference">Reference</a></li>    

    
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

![Product Name Screen Shot](https://github.com/chaitanya2593/Credit_Risk_Analysis/blob/main/overview.jpeg)


## Deployment
- At first, during preprocessing the categorical variables label encoded and this encoding objects are stored by in label_dict.pkl and similar min_max_scaler.pkl file for the normalisation. 
- Then creating an account in heruko for free. Then created a dash python file named app.py(for convenience I used the generic name). As DASH uses flask, the app was built for a flask deployment and it doesn't support static files.
- As third step I have designed code to capture all the required fields for the model prediction.
- The model is tested locally just by invoking python file `python app.py`. 
- Now it is more of app deployment in heroku

### Heroku deployment
As a prerequsite, one should have the following things 
1. An account in the Heroku https://dashboard.heroku.com/
2. Create an app in the Heroku with available name

In the git folder one should below files
3. requirements.txt - with all the python packages required for app.
4. Procfile - an no extension file with command `web: gunicorn app:server` (if you are using different name for the main dash file please replace the same in the command)

#### Initialize  heroku
In this step it is more about deploying the app in heroku app. 


> heroku create my-dash-app # change my-dash-app to a unique name<br>
> git add . # add all files to git<br>
> git commit -m 'Initial app boilerplate'<br>
> git push heroku master # deploy code to heroku<br>

Once this is successfully done you should get the url to access the website. In my case it is - `https://hdapp2593.herokuapp.com/`

## References:
- https://dash.plotly.com/deployment
- https://devcenter.heroku.com/articles/creating-apps



