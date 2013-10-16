OSX:

Add to Run Script

	cp -R ../../../addons/ofxNI2/libs/OpenNI2/lib/osx/ "$TARGET_BUILD_DIR/$PRODUCT_NAME.app/Contents/MacOS/";
	cp -R ../../../addons/ofxNI2/libs/NiTE2/lib/osx/ "$TARGET_BUILD_DIR/$PRODUCT_NAME.app/Contents/MacOS/";

Windows (VS 2012):

Add to Post-build Script
	
	xcopy /e /i /y "$(ProjectDir)..\..\..\export\vs\*.dll" "$(ProjectDir)bin"
	xcopy /e /i /y "$(ProjectDir)..\..\..\addons\ofxNI2\libs\OpenNI2\lib\win32\*" "$(ProjectDir)bin"
	xcopy /e /i /y "$(ProjectDir)..\..\..\addons\ofxNI2\libs\NiTE2\lib\win32\*" "$(ProjectDir)bin"
