# RunTime_Permission_Demo
  Read and write External Storage android 10+
  In this project i have simply captured image from defaul camera and stored in External Storage 
![7151463c-8e8a-4d61-9714-a58771735125](https://user-images.githubusercontent.com/26364962/97279339-b359d980-185c-11eb-8b96-941112c1b7c7.jpg)
![7151463c-8e8a-4d61-9714-a58771735125](https://user-images.githubusercontent.com/26364962/97279470-ddab9700-185c-11eb-9cca-876567585aa8.jpg)

# Add these line of code in your AndroidManifest.xml
     <provider
                android:name="androidx.core.content.FileProvider"
                android:authorities="${applicationId}.provider"
                android:exported="false"
                android:grantUriPermissions="true">
                <meta-data
                    android:name="android.support.FILE_PROVIDER_PATHS"
                    android:resource="@xml/file_list" />
      </provider>
  
# And then create xml file for storage path like this

    <?xml version="1.0" encoding="utf-8"?>
    <paths xmlns:android="http://schemas.android.com/apk/res/android">
        <external-path name="external_files" path="."/>
    </paths>
