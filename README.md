To use the theme.

1.Create a new app in Frappe-bench(If no custom app exists)
    bench create new-app <app-name>

2. Install the app in your site
    bench --site your-site-name install-app your-app-name

3. Go to the CSS folder in your your app and create a new file
    your-app
        -your-app
            -public
                -CSS
                    -newfile.css

4. Paste the code in the newly created file.

5. Go to the hooks.py file in your app and add the following lines
    app_include_css = [
    "/assets/<your-app-name>/css/newfile.css"
]

6. Now run the below commands
    bench migrate
    bench --site your-site-name clear-cache
    bench --site your-site-name clear-website-cache
    bench --site your-site-name build
    bench restart / kill and start the running bench

7. Or just clone and follow the steps.
