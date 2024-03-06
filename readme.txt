A simple ghost template, with the philosophy that content is what matters most, and side functions can come later if you want/need them.
There's not much here; just a simple menu setup with talk rate adjustment. The ghost will take your username from what you have in the SSP preferences, and it will base your pronouns on what you have the "sex" option set to ("Undefined" will use they). It will also figure out your birthday from there.
Note that just about everything in this template, aside from the files in the yaya_base folder, is optional! If you don't want that particular thing in your ghost, you can probably just erase it or comment it out! Don't be afraid to try stuff.

My eternal thanks to Ayakamtka for translating the config.dic to English!



——— Three very important notes ———

1: If you are using github to host your network updates, DO NOT use a github.io url with this template. The _loading_order.txt file in the yaya_base directory will cause a 404 error because of the underscore at the start of its name. Use a raw.githubusercontent link instead, it's better for multiple reasons.

2: This template has a simple Emergency Mode set up. This means that if there is an error in your dic files, it will load *just* the files in yaya_base and emerg.dic, and nothing else. This is so that errors can be output to the error log without necessarily needing the debugger Tama! I do recommend Tama, but this makes life a little easier. If you want to customize which files load, you can do that in yaya_emerg.txt

3: This template does NOT use Select.options! Instead, if you click on a menu choice and the linked function's name doesn't start with On, it'll direct to OnChoiceSelect. See Ukadoc for more details. https://ukagakadreamteam.github.io/ukadoc/manual/list_sakura_script.html#_q_title,ID_
https://ukagakadreamteam.github.io/ukadoc/manual/list_shiori_event.html#OnChoiceSelect

If you want to use Select.options, add this snip of code somewhere:

//This bit of code is what makes menu options that don't start with On direct to Select.options instead. Remove or comment it if you prefer!
OnChoiceSelect
{
    EVAL("Select.%(reference0)")
}



——— If you are completely new to this ———

A quick rundown so you have the gist of how to read these files. This is what a SHIORI event looks like:

OnMouseDoubleClick
{
	//Some code in here
}

There is a name, then some brackets, and code inside of it. You'll see also that the name starts with "On". If the name does NOT start with "On", it's probably a normal function. But if it has "On", you should look it up on Ukadoc to see what it does! Here's the page for SHIORI events:
https://ukagakadreamteam.github.io/ukadoc/manual/list_shiori_event.html

Ctrl + F is your friend here. If you can't find the name on that page, then it is very likely to be a custom SHIORI event. In that case, you should use Ctrl + F in NotePad++ (or whatever editor you're using) to try and find other instances of the name in the ghost's files. If using NotePad++, the "Find in Files" option is really handy for this, especially if you set it to only search through .dic files.

In this case, you are likely to find the name of the SHIORI event inside of Sakura Script tags, such as menu choices like \q[Settings,OnConfigMenu], or raise tags like \![raise,OnSomeEvent]. You can read more about Sakura Script tags here:
https://ukagakadreamteam.github.io/ukadoc/manual/list_sakura_script.html

Ukadoc will take you far. It is the official documentation for SSP. For official YAYA documentation, see the AYAYA wiki. Specifically, this page is a list of all the built in functions:
https://emily.shillest.net/ayaya/index.php?%E3%83%9E%E3%83%8B%E3%83%A5%E3%82%A2%E3%83%AB/%E9%96%A2%E6%95%B0%E7%94%A8%E9%80%94%E5%88%A5%E4%B8%80%E8%A6%A7

If you'd like to learn to code in YAYA, there is an in-depth English guide here, which starts with the very basics:
https://zichqec.github.io/YAYA_Fundamentals/

There is also a general walkthrough for making ghosts that you may find helpful, but note that it is made with a different (and much larger) template in mind:
http://ashido.com/ukagaka/



This template is free to use to create whatever ghost you like, no need to credit me for it. If you'd like to see more by me, I can be found here:
https://ukagaka.zichqec.com/

That's it, have fun!

Simplicity Template v1.0.8 https://github.com/Zichqec/simplicity_template
Using YAYA Tc571-5 https://github.com/yaya-shiori/