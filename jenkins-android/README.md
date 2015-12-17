download:
	gradle:
		url:https://downloads.gradle.org/distributions/gradle-2.9-bin.zip

	SDK Tools:
		url:http://tools.android-studio.org/index.php/sdk
config env:
	gradle:
		$:echo "export GRADLE_HOME=/opt/gradle-2.9">>~/.bashrc
		$:echo "export PATH=$PATH:$GRADLE_HOME/bin">>~/.bashrc
		$:source ~/.bashrc
	sdk tools:
		$:echo "export SDK_PATH=/opt/android-sdk-linux/tools">>~/.bashrc
		$:echo "export PATH=$PATH:$SDK_PATH">>~/.bashrc
		$:source ~/.bashrc
		
	

