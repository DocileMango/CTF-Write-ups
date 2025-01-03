# Web Exploitation - Trickster

Flag: picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_9ae8fb17}

## Write up

This is the challenge:

![](./Images/image.png)

Accessing the webpage, this is what we see

![](./Images/image2.png)

I ran `gobuster` to see for any additional web pages that I can access.

![](./Images/image3.png)

If we access robots.txt, we see that we can access another webpage `instructions.txt`

![](./Images/image4.png)

These are the contents of that webpage

![](./Images/image5.png)

With these information, I decided to this ![PHP webshell](https://github.com/WhiteWinterWolf/wwwolf-php-webshell)

I added the word PNG into the top of the file to ensure the first few bytes of the file is PNG

![](./Images/image6.png)

I then renamed the file to have the .png extension

![](./Images/image7.png)

Uploading the file shows that it passed

![](./Images/image8.png)

Now we access our uploaded file through `/uploads/`

![](./Images/image9.png)

After looking around using our webshell, we find the flag

![](./Images/image10.png)

And that's the challenge solved!