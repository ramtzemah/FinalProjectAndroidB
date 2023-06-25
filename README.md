# FinalProjectAndroidB

## Progress Bar Horizontal

### first stage:

add this lines to gandle:

	dependencies {
	        implementation 'com.github.ramtzemah:FinalProjectAndroidB:1.0.0'
	}

and

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}

or

	buildscript {
		repositories {
			...
                    mavenCentral()
			maven { url 'https://jitpack.io' }
		}
	}

and

	pluginManagement {
    repositories {
        ...
        mavenCentral()
        maven { url 'https://jitpack.io' }
      }
    }

    dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        google()
        mavenCentral()
        maven { url 'https://jitpack.io' }
      }
    }

### second stage:
add a CardView to your layout

     <androidx.cardview.widget.CardView
          android:id="@+id/cardView"
          android:layout_width="match_parent"
          android:layout_height="wrap_content"
          app:layout_constraintEnd_toEndOf="parent"
          app:layout_constraintStart_toStartOf="parent"
          app:layout_constraintTop_toTopOf="parent"
          app:layout_constraintBottom_toBottomOf="parent"/> 

<img width="285" alt="Screenshot 2023-06-24 at 10 48 28" src="https://github.com/ramtzemah/FinalProjectAndroidB/assets/65961116/48595a9b-3262-4c63-b4c8-00e4f096783e">

### third stage:
add this line:<br>
``` ProgressBarHorizontal.progressBar(this, cardView, currentProgress, max) ```<br>

**this**: the activity<br>
**cardView**: the CardView you add in the first stage<br>
**currentProgress**: the progress of the progress bar (Integer)<br>
**max**: the maximum value of the progress bar (Integer)<br>

![Screenshot 2023-06-23 at 22 51 17](https://github.com/ramtzemah/FinalProjectAndroidB/assets/65961116/debbfb5b-b5d3-4a1c-b17c-11bf6aaf7497)

![Screenshot 2023-06-23 at 22 51 39](https://github.com/ramtzemah/FinalProjectAndroidB/assets/65961116/b48f9643-3e91-44e4-817b-672b95323bc1)

<img width="285" alt="Screenshot 2023-06-24 at 11 01 10" src="https://github.com/ramtzemah/FinalProjectAndroidB/assets/65961116/9497ee5c-32dd-4f51-b71f-4ae0866e4922">


### * colors of progress bar
color can be changed by this values

    <color name="background_progress">#000000</color>
    <color name="progress">#FFEB3B</color>

<img width="285" alt="Screenshot 2023-06-24 at 11 48 54" src="https://github.com/ramtzemah/FinalProjectAndroidB/assets/65961116/2a608f05-a032-45fb-bd47-827ce1722f22">
<img width="285" alt="Screenshot 2023-06-24 at 11 49 35" src="https://github.com/ramtzemah/FinalProjectAndroidB/assets/65961116/ea3c376d-a3a0-42a0-9515-b58e42acc05d">
<img width="285" alt="Screenshot 2023-06-24 at 11 51 14" src="https://github.com/ramtzemah/FinalProjectAndroidB/assets/65961116/f354807a-08dc-44dc-b06a-267d86edbffc">

### VIDEO:

https://github.com/ramtzemah/FinalProjectAndroidB/assets/65961116/303f993f-0f64-488a-be1b-99f90af02edd


