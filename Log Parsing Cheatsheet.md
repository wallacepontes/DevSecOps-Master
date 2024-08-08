# Log Parsing

In the IT industry, the fundamental skill of log parsing remains as vital as ever. 

It's the backbone of troubleshooting, security analysis, and system monitoring. 

To aid in this crucial task, I've compiled a comprehensive Log Parsing Cheatsheet that is perfect for IT professionals of all stripes.

Here’s a breakdown of each command and how you can use it:

🔎 𝗛𝗘𝗔𝗗: 𝚑𝚎𝚊𝚍 𝚏𝚒𝚕𝚎.𝚕𝚘𝚐 gives you the top ten lines of a file, which is often where critical recent error logs can be found. For instance, 𝚑𝚎𝚊𝚍 -𝚗 𝟸𝟶 𝚏𝚒𝚕𝚎.𝚕𝚘𝚐 displays the first 20 lines.

🔍 𝗧𝗔𝗜𝗟: 𝚝𝚊𝚒𝚕 𝚏𝚒𝚕𝚎.𝚕𝚘𝚐 does the opposite, showing you the last ten lines of a file — where the most recent events are logged. Try 𝚝𝚊𝚒𝚕 -𝚏 𝚏𝚒𝚕𝚎.𝚕𝚘𝚐 to get a real-time stream of log updates.

🔄 𝗖𝗢𝗠𝗠: 𝚌𝚘𝚖𝚖 𝚏𝚒𝚕𝚎𝟷.𝚕𝚘𝚐 𝚏𝚒𝚕𝚎𝟸.𝚕𝚘𝚐 helps you compare two sorted files. It's perfect for finding discrepancies between log versions, like 𝚌𝚘𝚖𝚖 -𝟹 𝚜𝚎𝚛𝚟𝚎𝚛𝟷.𝚕𝚘𝚐 𝚜𝚎𝚛𝚟𝚎𝚛𝟸.𝚕𝚘𝚐 to see lines unique to each.

🔣 𝗟𝗘𝗦𝗦: 𝚕𝚎𝚜𝚜 𝚏𝚒𝚕𝚎.𝚕𝚘𝚐 allows for on-the-fly viewing of large log files. Navigate with 𝙶, 𝚐𝚐, and /𝚜𝚎𝚊𝚛𝚌𝚑_𝚝𝚎𝚛𝚖.

📊 𝗖𝗦𝗩𝗞𝗜𝗧: 𝚌𝚜𝚟𝚌𝚞𝚝 -𝚌 𝟹 𝚍𝚊𝚝𝚊.𝚌𝚜𝚟 can extract columns from CSVs. For example, 𝚌𝚜𝚟𝚌𝚞𝚝 -𝚗 𝚍𝚊𝚝𝚊.𝚌𝚜𝚟 lists column names.

📑 𝗝𝗤: 𝚓𝚚 .𝚏𝚘𝚘 𝚍𝚊𝚝𝚊.𝚓𝚜𝚘𝚗 is for JSON parsing — invaluable for modern web app logs. Use 𝚓𝚚 '.[] | .𝚗𝚊𝚖𝚎' 𝚞𝚜𝚎𝚛𝚜.𝚓𝚜𝚘𝚗 to extract user names from a list.

🔍 𝗚𝗥𝗘𝗣: 𝚐𝚛𝚎𝚙 '𝚎𝚛𝚛𝚘𝚛' 𝚏𝚒𝚕𝚎.𝚕𝚘𝚐 finds all occurrences of 'error' in a file. Advanced usage like 𝚐𝚛𝚎𝚙 -𝙴 "𝟺[𝟶-𝟿]{𝟸}" 𝚏𝚒𝚕𝚎.𝚕𝚘𝚐 finds all 400-level errors in HTTP logs.

📡 𝗡𝗚𝗥𝗘𝗣: 𝚗𝚐𝚛𝚎𝚙 -𝚍 𝚎𝚝𝚑𝟶 '𝟺𝟶𝟺' 𝚙𝚘𝚛𝚝 𝟾𝟶 listens on the network for specific data, useful for real-time traffic analysis.

🔧 𝗧𝗥: 𝚝𝚛 '[:𝚕𝚘𝚠𝚎𝚛:]' '[:𝚞𝚙𝚙𝚎𝚛:]' < 𝚏𝚒𝚕𝚎.𝚝𝚡𝚝 transforms lowercase to uppercase. Remove duplicates with 𝚝𝚛 -𝚜 '\𝚗'.

🔪 𝗖𝗨𝗧: 𝚌𝚞𝚝 -𝚍 ',' -𝚏 𝟸 𝚏𝚒𝚕𝚎.𝚕𝚘𝚐 can parse fields from delimited logs, making it simple to see specific data columns.

🔨 𝗦𝗘𝗗: 𝚜𝚎𝚍 '𝚜/𝚘𝚕𝚍/𝚗𝚎𝚠/𝚐' 𝚏𝚒𝚕𝚎.𝚕𝚘𝚐 finds and replaces text — 𝚜𝚎𝚍 '/^$/𝚍' 𝚏𝚒𝚕𝚎.𝚕𝚘𝚐 removes empty lines.

🔢 𝗦𝗢𝗥𝗧: 𝚜𝚘𝚛𝚝 𝚏𝚒𝚕𝚎.𝚝𝚡𝚝 sorts text files line by line. For numeric sort, use 𝚜𝚘𝚛𝚝 -𝚗 𝚏𝚒𝚕𝚎.𝚝𝚡𝚝.

🌟 𝗨𝗡𝗜𝗤: 𝚞𝚗𝚒𝚚 -𝚌 𝚏𝚒𝚕𝚎.𝚝𝚡𝚝 counts and removes duplicates. Case-insensitive search can be done using 𝚞𝚗𝚒𝚚 -𝚒 𝚏𝚒𝚕𝚎.𝚝𝚡𝚝.

📃 𝗗𝗜𝗙𝗙: 𝚍𝚒𝚏𝚏 𝚏𝚒𝚕𝚎𝟷.𝚕𝚘𝚐 𝚏𝚒𝚕𝚎𝟸.𝚕𝚘𝚐 compares files line by line, crucial for version differences.

🖋️ 𝗔𝗪𝗞: 𝚊𝚠𝚔 '{𝚙𝚛𝚒𝚗𝚝 $𝟸}' 𝚏𝚒𝚕𝚎.𝚕𝚘𝚐 prints the second word in each line. It’s perfect for text processing scripts, like summarizing logs.

Keep it handy, and you'll find that these commands become second nature as you navigate through your daily tasks.

![Log Parsing](./img/x/Brij%20kishore%20Pandey/Log%20Parsing%20Cheatsheet.gif)