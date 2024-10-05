# CTF-Reverse-Foreign-memory

## Describtion 
A foreign memory, like honey, always tastes better.
## Writeup

### Let's open open file in IDA
As we can see, there is a primitive defense against debugging here. Also notepad.exe should be open

![изображение](https://github.com/user-attachments/assets/d748d2a3-416f-4703-976e-710475468a47)


Bypass this in any way possible, I'll just remove the goto construct.
 
We can see an array of bytes with some arithmetic calculations going on, let's see what happens to it

![изображение](https://github.com/user-attachments/assets/2863bcab-e974-441e-b04f-64b9845dde53)

![изображение](https://github.com/user-attachments/assets/c4a073e8-402d-4af8-9427-f446efb433c7)

Let's convert this into code 

We can see that the value 0x80 is subtracted from these bytes

![изображение](https://github.com/user-attachments/assets/de8d89ec-906c-479b-851f-78c83a3d48e9)


Let's write a simple script and start it

![изображение](https://github.com/user-attachments/assets/856cff40-6edd-4f93-9e79-ca5a83394b88)


Success 

### Answer 

**This is our flag: CODEBY{S0meonE_el$e_s_m2morY_1s_swe2t_@s_hOn2y}**


