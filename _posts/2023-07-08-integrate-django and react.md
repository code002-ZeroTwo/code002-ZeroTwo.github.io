---
layout: post
title: Integrate Django Project with React app
date: 2023-07-08 17:25:06+0545
description: Simple way to integrate Django project and React app
categories: django-project react-app web-app
giscus_comments: true
related_posts: false
toc:
  sidebar: left
---

To integrate **django project** and **react app**. You can follow following steps:

<br>

### **Create a Django project**

create a django project with:

```
django-admin startproject projectname
```

Then cd to your project with:

```
cd projectname
```

<br>

### **Create a React project**

Now create a new folder inside root directory of your django project.you can call it `frontend` for example.

After creating new folder for your react app, initilize new React Project with:

```
npx create-react-app .
```

In the terminal, run the following command to install the necessary dependencies:

```
npm install
```

This will install the required dependencies based on the package.json file.

Run the following command to build the React app

```
npm run build
```

Start the development server for your React app by running the following command:

```
npm start
```


<br>

### **Configure Django project**

In `settings.py` of your django project:

#### **Configure Template**

import the os module with:
```
import os
```

Search and find the TEMPLATES in `settings.py`. and change the following.
```   
'DIRS': [os.path.join(BASE_DIR, 'frontend/build')]
```

<br>

#### **Configure Static Files**

Add the following lines of code in `settings.py` to configure static files:

```
STATICFILES_DIRS = [
    os.path.join(BASE_DIR,'frontend/build/static')
]  
```


<br>

### **Conclusion**

With these simple steps now you can integrate react and django project and work with them accordingly.
