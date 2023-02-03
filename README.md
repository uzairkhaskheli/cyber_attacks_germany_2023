# cyber_attacks_germany_2023
Cyber Attacks Germany 2023 Data Cleaning
𝐂𝐘𝐁𝐄𝐑 𝐀𝐓𝐓𝐀𝐂𝐊𝐒 𝐈𝐍 𝐆𝐄𝐑𝐌𝐀𝐍𝐘 𝐈𝐍 2022-23

In recent times I came across lot of news about cyber attacks (including our hostel whose server was hacked for several months halting all the payment and email system) in Germany so I though to create a visualisation based on some data.
Thanks to Bert Kondruss for collecting and providing me with the data.

𝐃𝐀𝐓𝐀 𝐂𝐋𝐄𝐀𝐍𝐈𝐍𝐆:
I started this project with the aim of using web scraping technique to acquire data but then I found out this pandas html method to directly grab the table.
df = pd.read_html(url)[0]


The problem that I faced while reading this data was with null values. So I had to drop some of the entries from city column and then also replace some

#dropping rows where city and place are empty df = df.dropna(subset=['city', 'place'])

There is also another special method where you can fill the values of previous column to the next one if its value is empty . it was the case of city and state (some German city and state names are same). If you remove axis = 1 it will be true for rows.
df.fillna(method='ffill', axis = 1)

𝐏𝐫𝐞𝐩𝐚𝐫𝐢𝐧𝐠 𝐂𝐒𝐕:
The problem I faced here when I was reading the csv in excel it was giving me some errors due to german text present. The solution to produce the correct result I had to import the file using Data function in excel where you can use UTF-8 encoding and the text would be converted in right format.

Link to Github code of Python: https://lnkd.in/eXEu2U_j

𝐃𝐀𝐓𝐀 𝐕𝐢𝐬𝐮𝐚𝐥𝐢𝐳𝐚𝐭𝐢𝐨𝐧:
After making the dashboard I came to see that NRW is the state with most cyber attacks followed by Bavaria on the second and Baden-Württemberg on the third place.
Similarly Berlin ranks the city where the most cyber attacks have happened amounting to 11 attacks. Hamburg second the list followed by Frankfurt am Main and Essen.

Link to Tableau Dashboard:
https://lnkd.in/emF5ydhQ
