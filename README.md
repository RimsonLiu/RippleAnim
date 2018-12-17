# RippleAnim
波纹点击效果

## 使用方法
### Step 1. Add the JitPack repository to your build file
```
allprojects {
  repositories {
    ...
    maven { url 'https://jitpack.io' }
  }
}
```

### Step 2. Add the dependency
```
dependencies {
  implementation 'com.github.RimsonLiu:RippleAnim:v1.0'
}
```

### API
方法|描述
-|-|
create(view: View)|创建动画对象
setDuration(duration: Long)|设置动画时长
setOnAnimationEndListener(listener: Listener)|设置动画播放完毕监听器
start()|开始播放

### 使用实例
```
button.setOnClickListener{ view: View ->
  val onAnimationEndListener = object : RippleAnimation.OnAnimationEndListener {
				override fun onAnimationEnd() {
					// 动画播放完毕要做的事情
                    ...
				}
			}
  RippleAnimation.create(view).setDuration(1000).setOnAnimationEndListener(onAnimationEndListener).start()
  // 完成波纹效果（例如更换背景颜色）
  ...
}
```
## Demo
https://github.com/RimsonLiu/RipplePreferenceScreen

## 参考
https://github.com/wuyr/RippleAnimation
