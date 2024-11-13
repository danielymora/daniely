# daniely
Daniely's personal website

## How To

### Edit components

If you wish to edit the contents of the website, find the component you want to edit and commit those changes to the main branch. this will kick off an Action that will automatically build the website and push to `gh-pages` branch. This will in turn kick off another Action that will publish the latest version of the website. 

For instance, if you want to edit the About Me section, edit the [AboutMe.vue component](daniely/src/components/AboutMe.vue)

To change the picture, add a new image at the daniely/src/assets location and then reference that file in [ProfileImage.vue](daniely/src/components/AboutMe.vue)