source 'https://github.com/CocoaPods/Specs.git'

platform :osx, '10.8'
xcodeproj 'CotEditor/CotEditor.xcodeproj'
inhibit_all_warnings!


# shared pods
def shared_pods
    pod 'OgreKit',
        :git => 'https://github.com/coteditor/OgreKit.git',
        :branch => 'coteditor-mod-nofindpanel'
    pod 'YAML-Framework',
        :git => 'https://github.com/coteditor/YAML.framework.git',
        :branch => 'coteditor-mod'
    pod 'NSHash'
    pod 'WFColorCode'
end

# non-AppStore target
shared_pods
pod 'Sparkle', '1.11.1'

# AppStore target
target :appstore, :exclusive => true do
    link_with 'CotEditor (AppStore)'
    shared_pods
end
