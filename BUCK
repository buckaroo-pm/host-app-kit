xcode_developer_dir = read_config('apple', 'xcode_developer_dir', '/Applications/Xcode.app/Contents/Developer')

genrule(
  name = 'app-kit-framework', 
  out = 'AppKit.framework', 
  cmd = 'cp -r ' + xcode_developer_dir + '/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework $OUT', 
)

prebuilt_apple_framework(
  name = 'app-kit', 
  framework = ':app-kit-framework', 
  preferred_linkage = 'static', 
  visibility = [
    'PUBLIC', 
  ], 
)
