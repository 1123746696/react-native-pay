##React-Native-Pay
����΢�ţ�֧����֧��

###��ΰ�װ

1.���Ȱ�װnpm��

	npm install react-native-paysdk --save
2.link

	rnpm link react-native-paysdk
�ֶ�link~��������ܹ��Զ�link��

####Android

	// file: android/settings.gradle
		...
 
		include ':react-native-wx'
		project(':react-native-wx').projectDir = new File(settingsDir, '../node_modules/react-native-wx/android')


	// file: android/app/build.gradle
	...
	 
	dependencies {
	    ...
	    compile project(':react-native-wx')
	}

android/app/src/main/java/<��İ���>/MainApplication.java������������У�


	...
	import cn.reactnativepay.payment.PayPackage;  // ��public class MainApplication֮ǰimport 
	 
	public class MainApplication extends Application implements ReactApplication {
	 
	  private final ReactNativeHost mReactNativeHost = new ReactNativeHost(this) {
	    @Override
	    protected boolean getUseDeveloperSupport() {
	      return BuildConfig.DEBUG;
	    }
	 
	    @Override
	    protected List<ReactPackage> getPackages() {
	      return Arrays.<ReactPackage>asList(
	          new PayPackage(), // Ȼ�������һ�� 
	          new MainReactPackage()
	      );
	    }
	  };
	 
	  @Override
	  public ReactNativeHost getReactNativeHost() {
	      return mReactNativeHost;
	  }
	}