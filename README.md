# doinput
an extention to dopixels that allows the user to take input

doinput adds one function and a supporting enum:
```C
enum _special_keys { //keys that cannot be represented by a single char
  KEY_SPACE, KEY_SHIFT, KEY_ESCAPE, KEY_CTRL, KEY_ALT, KEY_LEFT_ARROW, KEY_RIGHT_ARROW,
  KEY_UP_ARROW, KEY_DOWN_ARROW
};
int _inp_is_key_pressed(struct screen screen, int key, int up);
```
as an extention to dopixels, doinput naturally requires it to build.

* screen is your dopixels screen struct you should already have
* key is either a char of a letter/number or a \_special\_key of the required key
* up is a boolean 1 to check if the button is released, 0 to check if it is pressed

\_inp\_is\_key\_pressed returns 1 if the key is pressed, and 0 if it is not
