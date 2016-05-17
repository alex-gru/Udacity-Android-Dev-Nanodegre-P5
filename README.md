**[← back to project list](https://github.com/alex-gru/android_dev_nanodegree_udacity/blob/master/README.md)**

##P5 - Make Your App Material <img style="position: center;" src="https://github.com/alex-gru/Udacity-Android-Dev-Nanodegre-P5/blob/master/XYZReader/src/main/res/mipmap-xxxhdpi/ic_launcher.png" width="50"> 
***Included Udacity course: [Material Design for Android Developers](https://www.udacity.com/course/material-design-for-android-developers--ud862)***

This projects goal is to get familiar with the Material Guidelines, which is Google's design guideline introduced with Android Lollipop. Starting with a functionally working source code, design principles should be taken in account and applied. 

###Starting Code and Design Flaws
The app is called "XYZ Reader", which serves as an RSS feed reader. Items are shown in a list, selected items are shown in a detail view. As the screenshots clearly show, the design has really some design issues. The color is chosen in a way, that reduces contrast and therefore leads to a very bad user experience. Also the basic style of the app is inconsistent, with different shades of grey and a rather depressing look. Moreover, images are not scaled corretly and introduce misplaced margins and white spaces. Also the text font style needs some enhancements. 

<img style="position: center;" src="https://github.com/alex-gru/Udacity-Android-Dev-Nanodegre-P5/blob/master/static/screenshots/P5%20-%20Make%20Your%20App%20Material_1.png" width="250">
<img style="position: center;" src="https://github.com/alex-gru/Udacity-Android-Dev-Nanodegre-P5/blob/master/static/screenshots/P5%20-%20Make%20Your%20App%20Material_2.png" width="250">

### Enhancements

#### Consistent style and colors
The provided app icon already used an orange tone, so I introduced a color style, which is the nearest in the Material color guideline, i.e. the following shades:

    <color name="theme_primary">#FF5722</color>
    <color name="theme_primary_dark">#E64A19</color>
    <color name="theme_accent">#00B286</color>
    
The colors were chosen using [Adobe's Color Wheel Tool](https://color.adobe.com/create/color-wheel/). 

### Coordinator Layout and Floating Action Button (FAB)
Layouts were modified in a way to support downwards-compatibility (before Material was introduced), so the "support"-widgets CoordinatorLayout and FloatingActionButton are used. 

### Image Scaling Fixes
Several minor fixes are applied, to fix image views in the app. 

### Collapsable Toolbar
To achieve a rich user experience, a collapsable toolbar is built. The toolbar is shown in the detail view, and contains the high resolution image of the feed. When the user scrolls the detail view, the toolbar collapses, until the standard toolbar height is reached and now simply the title of the article is shown. 

<img style="position: center;" src="https://github.com/alex-gru/Udacity-Android-Dev-Nanodegre-P5/blob/master/static/screenshots/P5%20-%20Make%20Your%20App%20Material_7.gif" width="250">

### Text fixes
Instead of strange contrast-lacking text colors, better colors are chosen to improve readability. 

### User experience on different devices
A very important aspect is to provide the best user experience across all devices. This means, that serveral compatibility issues must be addressed. Android's Support library (and all it's features like AppCompat, Toolbar, FAB, Snackbar) are used to deal with this challenge. 


<img style="position: center;" src="https://github.com/alex-gru/Udacity-Android-Dev-Nanodegre-P5/blob/master/static/screenshots/P5%20-%20Make%20Your%20App%20Material_3.png" width="250">
<img style="position: center;" src="https://github.com/alex-gru/Udacity-Android-Dev-Nanodegre-P5/blob/master/static/screenshots/P5%20-%20Make%20Your%20App%20Material_4.png" width="250">
<img style="position: center;" src="https://github.com/alex-gru/Udacity-Android-Dev-Nanodegre-P5/blob/master/static/screenshots/P5%20-%20Make%20Your%20App%20Material_5.png" width="250">
<img style="position: center;" src="https://github.com/alex-gru/Udacity-Android-Dev-Nanodegre-P5/blob/master/static/screenshots/P5%20-%20Make%20Your%20App%20Material_6.png" width="250">
