# Cookies

So in this challenge we are given a website which generates a response in relation to the name of a cookie, on inspecting the page and checking for cookies, we find out that for each type of cookie there is a value given in response. '-1' is the value for an error and returns us to home screen, rest all values respond to a cookie.
Here either we can change values manually and see the response or we can use burpsuite.

![DevTools - mercury picoctf net_6418_check 05-06-2024 11_20_48](https://github.com/nAYANko/picoCTF/assets/147973815/5acbba83-810a-448b-bee7-93f32277045b)


![Burp Suite Community Edition v2024 4 5 - Temporary Project 05-06-2024 11_19_21](https://github.com/nAYANko/picoCTF/assets/147973815/37a5ef47-4e6d-42ce-9614-56bb4b79ffbb)


In proxy tab, open browser, enter the url, then enter some cookie type for it to generate a response, open the http history tab, find the get request, and send it to intruder, usually it identifies what payload or value may generate a different response from the website, else just select the value under name and send to intruder,
now in the payloads tab, use these settings,

![Burp Suite Community Edition v2024 4 5 - Temporary Project 05-06-2024 11_18_42](https://github.com/nAYANko/picoCTF/assets/147973815/d2874a78-8881-4f06-b0c1-31389cc8f735)


Start the attack, and u will see results of similar size except one whicg is for payload 18, checking the response for this by clicking on it and searching through the code gives us the flag.
The difference is size is due to absence of the line saying ' this is a cookie but not a special one'.

![Result 19 _ Intruder attack  05-06-2024 11_18_03](https://github.com/nAYANko/picoCTF/assets/147973815/21c82685-5b25-46e5-809a-4e36d50be26e)


Flag : picoCTF{3v3ry1_l0v3s_c00k135_88acab36}
