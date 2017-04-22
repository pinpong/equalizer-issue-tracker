```java
/**
 * Notify other apps like equalizer apps that a new audio session was opened.
 * Apps can use the linked audio session ID to attach audio effects or display a visualizer.
 *
 * @param context The application context the media player is running on.
 * @param player The associated media player instance.
 */
public static void openAudioSession(Context context, MediaPlayer player) {
    Intent intent = new Intent(AudioEffect.ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION);
    intent.putExtra(AudioEffect.EXTRA_AUDIO_SESSION, player.getAudioSessionId());
    intent.putExtra(AudioEffect.EXTRA_PACKAGE_NAME, context.getPackageName());
    intent.putExtra(AudioEffect.EXTRA_CONTENT_TYPE,AudioEffect.CONTENT_TYPE_MUSIC);
    context.sendBroadcast(intent);
}
```

```java
/**
 * Notify other apps like equalizer apps that a audio session was closed
 * and isn't active anymore.
 * Apps can use the linked audio session ID to detach audio effects.
 *
 * @param context The application context the media player is running on.
 * @param player The associated media player instance.
 */
public static void closeAudioSession(Context context, MediaPlayer player) {
    Intent intent = new Intent(AudioEffect.ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION);
    intent.putExtra(AudioEffect.EXTRA_AUDIO_SESSION, player.getAudioSessionId());
    intent.putExtra(AudioEffect.EXTRA_PACKAGE_NAME, context.getPackageName());
    context.sendBroadcast(intent);
}
```

```java
/**
 * Open the default equalizer app for a audio session.
 * If no Equalizer app is installed on the device the Google Play store is opened instead
 * with search results for equalizer apps instead.
 *
 * @param activity The activity from which to start the default equalizer app.
 * @param player The associated media player instance.
 */
public static void openEqualizerApp(Activity activity, MediaPlayer player) {
    final String KEYWORD = "equalizer";
    
    int sessionId = player.getAudioSessionId();
    if (sessionId != AudioEffect.ERROR_BAD_VALUE) {
        Intent intent = new Intent(AudioEffect.ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL);
        intent.putExtra(AudioEffect.EXTRA_AUDIO_SESSION, sessionId);
        intent.putExtra(AudioEffect.EXTRA_CONTENT_TYPE, AudioEffect.CONTENT_TYPE_MUSIC);
        try {
            activity.startActivityForResult(intent, 0);
        } catch (ActivityNotFoundException e1) {
            // No equalizer found. Opening Play Store.
            Intent searchIntent = new Intent(Intent.ACTION_VIEW).setData(
                    Uri.parse("market://search?q=" + KEYWORD));
            try {
                activity.startActivity(searchIntent);
            } catch (ActivityNotFoundException e2) {
                Intent webIntent = new Intent(Intent.ACTION_VIEW).setData(
                        Uri.parse("https://play.google.com/store/search?q=" + KEYWORD));
                try {
                    activity.startActivity(webIntent);
                } catch (ActivityNotFoundException e3) {
                    Log.w(TAG, "Error: Cannot find web browser.", e3);
                }
            }
        }
    }
}
```
