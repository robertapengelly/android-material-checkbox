# MaterialButton

Backported material styled CheckBox for use on pre-lollipop devices. Supports Android 2.3 API 9 (GINGERBREAD) and up.<br /><br />
Also check out https://github.com/robertapengelly/android-material-compoundbutton as MaterialCheckBox extends MaterialCompoundButton.

Preview

![materialcheckboxexample](https://cloud.githubusercontent.com/assets/5245027/22631391/1f3975fe-ec04-11e6-94ec-c594f3995a83.gif)

# Installation

    Step 1. Add the JitPack repository to your build file
    
    Add it in your root build.gradle at the end of repositories:
    
    allprojects {
        repositories {
            ...
            maven { url 'https://jitpack.io' }
         }
    }
    
    Step 2. Add the dependency
    
    dependencies {
        compile 'com.github.robertapengelly:android-material-checkbox:1.0.0'
    }

# Usage

    Styling
    
    The following style attributes are lollipop defaults for the theme. Change the values to better suit your app.
    
    Pre-Honycomb devices (values/styles.xml)
    
        <style name="AppTheme" parent="@android:style/Theme.NoTitleBar">
            <!-- Text colors -->
            <item name="android:textColorPrimaryDisableOnly">@color/primary_text_disable_only_material_dark</item>
            <item name="android:textColorSecondary">@color/secondary_text_material_dark</item>
            
            <!-- Text styles -->
            <item name="android:textAppearance">@style/TextAppearance.Material</item>
            
            <item name="android:listChoiceIndicatorMultiple">@drawable/btn_check_material_anim</item>
            
            <!-- Widget styles -->
            <item name="android:checkboxStyle">@style/Widget.Material.CompoundButton.CheckBox</item>
            
            <!-- Color palette -->
            <item name="colorAccent">@color/accent_material_dark</item>
            <item name="colorControlNormal">?android:attr/textColorSecondary</item>
            <item name="colorControlActivated">?attr/colorAccent</item>
            <item name="colorControlHighlight">@color/ripple_material_dark</item>
        </style>
    
    Honycomb and newer (values-v11/styles.xml)
    
        <style name="AppTheme" parent="@android:style/Theme.Holo.NoActionBar">
            <!-- Text colors -->
            <item name="android:textColorPrimaryDisableOnly">@color/primary_text_disable_only_material_dark</item>
            <item name="android:textColorSecondary">@color/secondary_text_material_dark</item>
            
            <!-- Text styles -->
            <item name="android:textAppearance">@style/TextAppearance.Material</item>
            
            <item name="android:listChoiceIndicatorMultiple">@drawable/btn_check_material_anim</item>
            
            <!-- Widget styles -->
            <item name="android:checkboxStyle">@style/Widget.Material.CompoundButton.CheckBox</item>
            
            <!-- Color palette -->
            <item name="colorAccent">@color/accent_material_dark</item>
            <item name="colorControlNormal">?android:attr/textColorSecondary</item>
            <item name="colorControlActivated">?attr/colorAccent</item>
            <item name="colorControlHighlight">@color/ripple_material_dark</item>
        </style>
    
    Lollipop and newer (values-v21/styles.xml)
    
        <style name="AppTheme" parent="@android:style/Theme.Material.NoActionBar">
            <!-- Text colors -->
            <item name="android:textColorPrimaryDisableOnly">@color/primary_text_disable_only_material_dark</item>
            <item name="android:textColorSecondary">@color/secondary_text_material_dark</item>
            
            <!-- Text styles -->
            <item name="android:textAppearance">@style/TextAppearance.Material</item>
            
            <item name="android:listChoiceIndicatorMultiple">@drawable/btn_check_material_anim</item>
            
            <!-- Widget styles -->
            <item name="android:checkboxStyle">@style/Widget.Material.CompoundButton.CheckBox</item>
            
            <!-- Color palette -->
            <item name="android:colorAccent">@color/accent_material_dark</item>
            <item name="android:colorControlNormal">?android:attr/textColorSecondary</item>
            <item name="android:colorControlActivated">?android:attr/colorAccent</item>
            <item name="android:colorControlHighlight">@color/ripple_material_dark</item>
        </style>
    
    Adding a MaterialButton widget (layout/activity_main.xml)
    
    If you use android:buttonTint it will be replaced with app:buttonTint.
    If you use android:buttonTintMode it will be replaced with app:buttonTintMode.
    
        <?xml version="1.0" encoding="utf-8" ?>
        <LinearLayout
            xmlns:android="http://schemas.android.com/apk/res/android"
            xmlns:app="http://schemas.android.com/apk/res-auto"
            android:layout_height="match_parent"
            android:layout_width="match_parent"
            android:orientation="vertical">
            
            <robertapengelly.support.widget.MaterialCheckBox
                android:layout_height="wrap_content"
                android:layout_width="match_parent"
                android:text="MaterialCheckBox"
                app:buttonTint="#0000ff" />
        
        </LinearLayout>
