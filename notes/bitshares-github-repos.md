Hi,

I’ve asked before in this group and in the Core team about how to present BitShares documentation.

- Do we want to see all (BBF and developers) documents information in a website (HTML format)?
- Do we want to separate the developers’ documentation and move all files to wiki?
- Do we want to separate the developers’ documentation as .md type files and create the contents list pages (README.md) and connect the contents/pages?  

***

After I received replies, my impressions were; 

For users (not developers), create a normal (HTMLs) website. So, new users can read and learn about BitShares basic information.  

For developers, I had several thoughts and comments to consider. The below are observations and remarks.9

**Current situations**

- Developers use GitHub repositories to create wiki or other (normally new) technical information files to share with others (direct communication).    
- BitShares has doc.bitshares.org website that also posts the developers documentation, but users often find older information.  (They are not updated at the same time)
- The doc.bitshares.org website had been built by Sphinx (.rst files  HTML files)
- BitShares has been posting duplicated (but often not exactly the same) information to the public.

**Remarks**

- For the future management, avoid having duplicated information.  It would be better to integrate BitShares developers’ information, otherwise, we would have the same issue in the future. 
- Developers are more familiar with to use .md file, not .rst file. (They both use markup languages but not the same formats.) 
- If BitShares manages the developers’ documentation files as .md files, developers are easier to access and use. 
- The README.md files could be used as each folder topic group Contents list in the developers’ documentation repository.
- If BitShares use the .md file for the documentation, developers find a familiar format to fix or contribute to expand BitShares developers’ documentation. 
- (*Right now, I’ve asked limited access. I need to see what type of information are available and exist and can gather first. And I would like to find better contents structures.  Meanwhile, I think users could see good and bad points of the documentation. They can point out and submit a question or request. We can check and consider them)

**Processes and thoughts**

I would like to gather BitShares developers’ document information and put together in a certain (.md) layout.  And check the issues to update and add new contents to improve. 

I want to avoid creating TWO steps to provide the developers document information (e.g., .rst -> html or .md -> ? -> html) . It seems to me the second position seize some power. I don’t think BitShares needs that for the future expansion.  

AS a result, I reached to manage BitShares documentation files and repositories (dev.bitshares.works and how.bitshares.works) in that manner. 

***

**Example:**
Contents pages output differences in GitHub repositories

*.RST markup language file

<p align="center">
  <img src="/images/git-rst.png" width="400" title="Repo">
</p>

***

*.MD markup language file

<p align="center">
  <img src="/images/git-md.png" width="400"  title="Repo">
</p>

***
