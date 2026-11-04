# Mi-CAT Pages

Mi-CAT is a machine-learning-integrated catastrophe modelling stack built on three layers. First, it learns asset-level vulnerability functions from observed damage data, capturing factors that conventional archetype-based functions ignore. Second, it fuses fragmented multi-source data, such as Earth observation from Google Earth Engine, infrastructure layers and governmental loss databases, into harmonised hazard, exposure and loss bases at the asset and sub-national level. Third, it couples these outputs with macro-fiscal stress-testing models to support budget planning and the prioritisation of prevention. Work so far has focused on the first layer for earthquakes: predicting building damage grades from observed damage data with classical and deep tabular models, including XGBoost, random forests, CatBoost, SAINT and TabNet, combined through ensembling.

Governments use catastrophe models to estimate how much damage a disaster could cause and to plan their budgets for it. A key ingredient is the vulnerability function, which describes how much damage a building suffers at a given intensity of earthquake, flood or storm. Conventional models assume that all buildings of a broad type respond the same way. Mi-CAT instead learns these relationships from damage observed in past disasters and links the results to the financial planning tools governments rely on.

This repository contains the source files for the public Mi-CAT website:

https://ai4drr.github.io/Mi-CAT/

## How It Works

Changes committed to the `main` branch are automatically deployed to the `pages/` directory of the main Mi-CAT repository.

Deployment flow:

    AI4DRR/Mi-CAT-pages
            ↓
      GitHub Actions
            ↓
    AI4DRR/Mi-CAT/pages
            ↓
       GitHub Pages
            ↓
    https://ai4drr.github.io/Mi-CAT/

There is no need to manually copy website files to the main Mi-CAT repository.

## Editing the Website

Website pages and assets can be created and edited directly in this repository.

For example, you can add:

    index.html
    about.html
    contact.html
    css/
    js/
    images/

After the changes are committed to `main`, they will be automatically deployed to the public website.

## Adding a New Page

For example, create:

    about.html

Commit the file to `main`.

Once deployment completes, the page will be available at:

    https://ai4drr.github.io/Mi-CAT/about.html

The same process applies to HTML pages, stylesheets, JavaScript, images, and other static website assets.

## Example Structure

The website structure is flexible. The example below shows one possible way to organize the files:

    Mi-CAT-pages/
    ├── .github/
    │   └── workflows/
    │       └── deploy.yml    # Automatic deployment - do not modify
    ├── index.html
    ├── about.html
    ├── css/
    │   └── style.css
    ├── js/
    │   └── main.js
    └── images/
        └── logo.png

This is only an example. Website files and directories can be organized as needed.

## Important

Do **not** modify or delete:

    .github/workflows/deploy.yml

This workflow handles the automatic deployment from this repository to the main Mi-CAT repository.

Also, do not commit passwords, API keys, access tokens, or other secrets to this repository.

## Deleting or Renaming Files

The deployment mirrors the website files in this repository to the published `pages/` directory.

If a website file is deleted or renamed here, the corresponding published file will also be deleted or renamed during the next deployment.

## Deployment

Deployment is automatic whenever website files are committed to the `main` branch.

To check the deployment status, open the **Actions** tab in this repository.

Public website:

https://ai4drr.github.io/Mi-CAT/
