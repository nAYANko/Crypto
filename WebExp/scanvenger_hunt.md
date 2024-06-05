# Scavenger Hunt

Just like Insp3t0r, we can find 2 parts of the code in the index and css file, now looking further into this challenge i see that it requires a lot of pre-requisite knowledge, first open the .js file and it says 'How can I keep Google from indexing my website?', so search engines read all sites so that they can index its information to be availaible on search, we can stop them from indexing some information by adding it to a 'robots.txt' file, hence opening 'http://mercury.picoctf.net:27278/robots.txt' gives us the 3rd part of the flag.

Now this page says 'I think this is an apache server... can you Access the next flag?', the Access keyword gives the hint of an access file, on searching i find out that there's an ' .htaccess ' file and searching for it gives the 4th part, the new page says 'I love making websites on my Mac, I can Store a lot of information there.', on searching i found out that there is a ' .DS_Store ' file in Mac which is kind of a tracking file, opening it gives the last part.


Flag: picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k _a69684fd}
