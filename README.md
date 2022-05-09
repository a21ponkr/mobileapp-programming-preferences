
This project has two activities components.
As well as code for jumping between the two

```
 openActivity2(); // for calling the second activity
 
```

```
 public void openActivity2(){
        Intent intent = new Intent(this, SecondActivity.class);
        startActivity(intent);
    }


```

The Text box was made in the second activity that will transfer its edited text to a text view in the first activity.
A button was link to the text box to save the edit.
Return button will return us to the main page and update the edited text
```
public void onResume() {
        super.onResume();
        SharedPreferences sp = getApplicationContext().getSharedPreferences("MyPrefs", Context.MODE_PRIVATE);

        TextView t1;
        t1 = findViewById(R.id.editThisText);
        t1.setText(sp.getString("TextEdit","idk"));


```
