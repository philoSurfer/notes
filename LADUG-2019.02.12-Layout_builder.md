# Notes from LADUG 2019.02.12 # 

- Install Layout Builder! Start playing with it now, it will very much be the foundation and future of site building for Drupal.
- join #layouts in drupal.slack.com if you want to start contributing or stay current on the conversations 
- Modules you should have included in your Layout Builder recipe:
    - __layouts__ - A usable library of pre configured layouts types.  Start here if you are considering custom layout building.  Everything you need to know about custom layouts is in the code. 
    - __layout_builder_restrictions__ - Gives you the options to restrict entity types for layout building per content type
   
- Installation tips:
    - You should be working with the latest Drupal 8.7 release (currently in dev at this time) to get all of the latest patches and features for layout_builder. I am running nightly composer update builds in our dev branch to keep our feature development on track for 8.7 GA release.  
    - Patches to be tracking at this time:
        - Some third party block settings will not appear unless you apply the patch in this issue
            - https://www.drupal.org/project/drupal/issues/2942661
        -  If you are planning on using zurb_foundation theme, you are going to need this patch: 
            - https://www.drupal.org/project/zurb_foundation/issues/3032594

        ##### You can quickly add the following to your composer.json
        
        ```json
        "patches": {
            "drupal/core":{
                "sections should have third party settings": "https://www.drupal.org/files/issues/2019-02-11/2942661-tps-54.patch"
            },
            "drupal/zurb_foundation": {
                "layout_builder compatibility": "https://www.drupal.org/files/issues/2019-02-13/layout_builder-compatibility-3032594.patch"
            }
        },
        ```


