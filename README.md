# CustomSlider-Android
Custom Slider showing a range in a bar and pin-pointing certain value with a thumbnail



# Gradle
Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
Step 2. Add the dependency

	dependencies {
	        implementation 'com.github.Rounak122:CustomSlider-Android:0.3.0'
	}
  
# Usage

1.a. XML (For Custom Slider without TextView):

	<com.example.customslider.CustomSlider
		android:id="@+id/customSlider"
		android:layout_width="300dp"
		android:layout_height="wrap_content"/>
		
1.b. XML (For Custom Slider with TextView):

	<com.example.customslider.CustomInfoSlider
		android:id="@+id/customInfoSlider"
		android:layout_width="300dp"
		android:layout_height="wrap_content"/>
		
In XML define a fixed width, it will be needed during initialization              

2.JAVA:

        //Slider with 3 regions (low, normal,high) | Use SetValues method for that
        customSlider1 = findViewById(R.id.customSlider1);
        customSlider1.setValues(0, 40000, 20000, 30000, 30000, 300);

        /* Slider with unlimited regions
         result will be set irrespective of weight, so it works only when all the weight are equal
         result = no. of block for res starting from 1 */

        customSlider2 = findViewById(R.id.customSlider2);
        customSlider2.setMultipleValues(4, new String[]{"#7596ff", "#7565ff", "#759685", "#829712", "#759325"}, new float[]{25, 25, 25, 25}, 3, 300);


        //CustomInfoSlider i.e. Textviews can be added mentioning range
        /* Slider with unlimited regions and their texts
         result will be set irrespective of weight, so it works only when all the weight are equal
         result = no. of block for res starting from 1 */

        customInfoSlider = findViewById(R.id.customInfoSlider);
        customInfoSlider.setMultipleInfoValues(5, new String[]{"#7596ff", "#7565ff", "#759685", "#829712", "#125625"}, new String[]{"(-) Negative", "(+-) 15 Cells/µl", "(+1) 70 Cells/µl", "(+2) 125 Cells/µl", "(+3) 500 Cells/µl"}, new float[]{20, 20, 20, 20, 20}, 3, 300);


