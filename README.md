# libfdr
Jim Plank's libfdr. I just want to use CMake instead of classic Make to make integration easier.

Original Jim Plank's codes are not touched, and you are not supposed to do so.

Just use it as is.

--------------------------------------------------------------
# Các lệnh cơ bản của Red black tree

```
JRB jrb_insert_str(JRB tree, char *key, Jval val)   //chèn node mới
JRB jrb_insert_int(JRB tree, int key, Jval val)     //chèn node mới
JRB jrb_insert_dbl(JRB tree, double key, Jval val)
```
#### Chèn với kiểu jval
`JRB jrb_insert_gen(JRB tree, Jval key, Jval val, int (*func)(Jval, Jval))`
> Key với kiểu jval. Cần cung cấp `(*func)(Jval, Jval)` là một hàm so sánh lấy 2 Jval làm đối số và trả về
   - a negative integer if the first key is less than the second.
   - a positive integer if the first key is greater than the second.
   - zero if the keys are equal. 
