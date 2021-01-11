So thank you for Joonik providing this converted source.
It helped me so much.

When I ran th code, I found error like "You cannot combine custom titles with other custome title".
I browsed and found the solution at https://stackoverflow.com/a/17860085/7966613 (thank you).

The point is, you need to create a new or edit res/values/style.xml and add this style:
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <style name="CustomTheme" parent="android:Theme">
    </style>
</resources>

Then in your AndroidManifest:
< application
   ...
   ...
   android:theme="@style/CustomTheme" >

The annoying thing is when you change (refactor) package name, it got new error.

Well, Good luck!
