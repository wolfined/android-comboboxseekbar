 [ ![Download](https://api.bintray.com/packages/techwolf12/android/comboboxseekbar/images/download.svg) ](https://bintray.com/techwolf12/android/comboboxseekbar/_latestVersion)
android-comboboxseekbar
======
android-comboboxseekbar is a mix between a seekbar/combobox.

![Example](../master/promo/example.png?raw=true)

Import using gradle

```gradle
dependencies {
    compile 'nl.techwolf12.android:comboboxseekbar:1.0.1'
}

```


XML:
```xml
<nl.techwolf12.comboboxseekbar.ComboSeekBar
    android:id="@+id/comboSeekBar"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_margin="5dp"
    android:progress="2"
    custom:color="#000"
    custom:multiline="false"
    custom:textSize="12sp" />
```
Java usage:

```java
public class ExampleFragment extends Fragment implements ComboSeekBar.OnValueChangeListener {

....

@Override
public View onCreateView(LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState) {

List<String> seekBarStep = Arrays.asList("0", "-50", "-52", "-56", "-62", "-78", "-110", "-174", "-302", "-∞");
seekBar = (ComboSeekBar) fragmentView.findViewById(R.id.comboSeekBar);
seekBar.setOnValueChangeListener(this);
seekBar.setAdapter(seekBarStep);
}

....

@Override
public void onValueChanged(SeekBar seekBar, int position, String value, boolean userInitiated) {
   Log.d(TAG, "onValueChanged: " + position + " with value: " + value);
}
```
