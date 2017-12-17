## TalkLibs简介
对讲功能封装
### 使用方法：

#### 使用Gradle构建时添加一下依赖即可:
```
compile 'com.daryun:talkLibs:0.0.2'
```
#### 初始化
```

// 在application的onCreate中初始化
@Override
public void onCreate() {
    super.onCreate();
    TalkLibs.getInstance().init(this,this);
    ...
}
```
#### 配置信息

```

/**
     * 视频对讲的配置，切换小区需要重新配置
     *
     * @param sid
     * @param userId
     * @param communityId
     * @param companyCode
     * @param areaId
     * @param appBindId
     */
TalkLibs.getInstance().config(Context context, String sid, String userId, final int communityId, final String companyCode, final int areaId, final int appBindId);
```
#### 呼叫
```
   /**
     * 呼出
     * @param activity
     * @param account
     * @param avChatType
     * @param callTypeEnum
     */
TalkLibs.getInstance().call(Activity activity, String account, AVChatType avChatType, CallTypeEnum callTypeEnum)
```
#### 退出
```
 /**
     * 登录对讲帐号
     */
TalkLibs.getInstance().loginOut();
```
