# EditTextAllCapsException
Exception thrown by an edittext with textAllCaps=true
On Nexus 5 android 5.1 and emulator with android 5.0
``` 
java.lang.IndexOutOfBoundsException
            at android.graphics.Paint.getTextRunAdvances(Paint.java:1899)
            at android.text.TextLine.handleText(TextLine.java:749)
            at android.text.TextLine.handleRun(TextLine.java:900)
            at android.text.TextLine.measureRun(TextLine.java:417)
            at android.text.TextLine.measure(TextLine.java:296)
            at android.text.TextLine.metrics(TextLine.java:270)
            at android.text.Layout.getLineExtent(Layout.java:977)
            at android.text.Layout.getLineWidth(Layout.java:943)
            at android.widget.TextView.desired(TextView.java:6507)
            at android.widget.TextView.onMeasure(TextView.java:6573)
            at android.view.View.measure(View.java:17547)
            at android.widget.RelativeLayout.measureChildHorizontal(RelativeLayout.java:727)
            at android.widget.RelativeLayout.onMeasure(RelativeLayout.java:463)
            at android.view.View.measure(View.java:17547)
            at android.view.ViewGroup.measureChildWithMargins(ViewGroup.java:5535)
            at android.widget.FrameLayout.onMeasure(FrameLayout.java:436)
            at android.support.v7.internal.widget.ContentFrameLayout.onMeasure(ContentFrameLayout.java:124)
            at android.view.View.measure(View.java:17547)
            at android.view.ViewGroup.measureChildWithMargins(ViewGroup.java:5535)
            at android.support.v7.internal.widget.ActionBarOverlayLayout.onMeasure(ActionBarOverlayLayout.java:444)
            at android.view.View.measure(View.java:17547)
            at android.view.ViewGroup.measureChildWithMargins(ViewGroup.java:5535)
            at android.widget.FrameLayout.onMeasure(FrameLayout.java:436)
            at android.view.View.measure(View.java:17547)
            at android.view.ViewGroup.measureChildWithMargins(ViewGroup.java:5535)
            at android.widget.LinearLayout.measureChildBeforeLayout(LinearLayout.java:1436)
            at android.widget.LinearLayout.measureVertical(LinearLayout.java:722)
            at android.widget.LinearLayout.onMeasure(LinearLayout.java:613)
            at android.view.View.measure(View.java:17547)
            at android.view.ViewGroup.measureChildWithMargins(ViewGroup.java:5535)
            at android.widget.FrameLayout.onMeasure(FrameLayout.java:436)
            at com.android.internal.policy.impl.PhoneWindow$DecorView.onMeasure(PhoneWindow.java:2615)
            at android.view.View.measure(View.java:17547)
            at android.view.ViewRootImpl.performMeasure(ViewRootImpl.java:2015)
            at android.view.ViewRootImpl.measureHierarchy(ViewRootImpl.java:1173)
            at android.view.ViewRootImpl.performTraversals(ViewRootImpl.java:1379)
            at android.view.ViewRootImpl.doTraversal(ViewRootImpl.java:1061)
            at android.view.ViewRootImpl$TraversalRunnable.run(ViewRootImpl.java:5885)
            at android.view.Choreographer$CallbackRecord.run(Choreographer.java:767)
            at android.view.Choreographer.doCallbacks(Choreographer.java:580)
            at android.view.Choreographer.doFrame(Choreographer.java:550)
            at android.view.Choreographer$FrameDisplayEventReceiver.run(Choreographer.java:753)
            at android.os.Handler.handleCallback(Handler.java:739)
            at android.os.Handler.dispatchMessage(Handler.java:95)
            at android.os.Looper.loop(Looper.java:135)
            at android.app.ActivityThread.main(ActivityThread.java:5254)
            at java.lang.reflect.Method.invoke(Native Method)
            at java.lang.reflect.Method.invoke(Method.java:372)
            at com.android.internal.os.ZygoteInit$MethodAndArgsCaller.run(ZygoteInit.java:903)
            at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:698)
```
I fixed adding inputType="textCapCharacters"
