<div class="text">
                                                                <p dir="ltr"><span>Linux, often associated with being a complex operating system primarily used by developers, may not necessarily fit that description entirely. While it can initially appear challenging for beginners, once you immerse yourself in the Linux world, you may find it difficult to return to your previous Windows systems. The power of Linux commands in controlling your PC, coupled with their clean user interface, can make it hard to switch back to older operating systems. If you’re a developer, you can likely relate to the advantages and appeal of Linux.</span></p>
<p dir="ltr"><span>To support developers and beginners alike, we have created a comprehensive </span><b><strong>Linux/Unix command line cheat sheet</strong></b><span>. This cheat sheet covers all the basic and advanced commands, including file and directory commands, file permission commands, file compression and archiving, process management, system information, networking, and more with proper examples and descriptions. In addition to that we provide all the most used Linux Shortcut which includes Bash shortcuts, Nano shortcuts, VI &amp; Vim Shortcuts Commands. It provides a solid foundation on Linux OS commands, as well as insights into practical applications.</span></p><div id="GFG_AD_gfg_mobile_336x280"></div>
<p dir="ltr"><span>By the end of this cheat sheet, you will have a basic understanding of Linux/Unix Commands and how it makes development easy for developers.</span></p>
<div style="width: 810px" class="wp-caption alignnone"><img src="https://media.geeksforgeeks.org/wp-content/uploads/20230714151733/linux-Cheat-Sheet.png" alt="Linux Commands Cheat Sheet" srcset="https://media.geeksforgeeks.org/wp-content/uploads/20230714151733/linux-Cheat-Sheet.png 1000w, https://media.geeksforgeeks.org/wp-content/uploads/20230714151733/linux-Cheat-Sheet-100.png 100w, https://media.geeksforgeeks.org/wp-content/uploads/20230714151733/linux-Cheat-Sheet-200.png 200w, https://media.geeksforgeeks.org/wp-content/uploads/20230714151733/linux-Cheat-Sheet-300.png 300w, https://media.geeksforgeeks.org/wp-content/uploads/20230714151733/linux-Cheat-Sheet-660.png 660w, https://media.geeksforgeeks.org/wp-content/uploads/20230714151733/linux-Cheat-Sheet-768.png 768w, " sizes="100vw" width="1000"><p class="wp-caption-text">Linux Commands Cheat Sheet</p></div>
<p dir="ltr"><b><strong>What is Linux?</strong></b></p><div id="_GFG_ABP_Incontent_728x90" style="text-align:center;"><iframe src="https://aa.geeksforgeeks.org/iframe.html?code=GFG_ABP_Incontent_728x90" style="width: 748px; height: 110px;"></iframe></div><div id="GFG_AD_InContent_Desktop_728x280"></div>
<p dir="ltr"><span>Linux is an open-source UNIX-like operating system (OS). An operating system is a software that directly manages a system’s hardware and resources, like CPU, memory, and storage. OS acts as a GUI through which user can communicate with the computer. The OS sits between applications and hardware and makes the connections between all of your software and the physical resources that do the work.</span></p>
<blockquote><p>
   </p><center><p></p>
<h2><span>Linux Commands List – Table of Content</span></h2>
<p></p></center><p></p><div id="GFG_AD_Desktop_InContent_ATF_336x280"></div>
<ul>
<li value="1"><a href="#directory" rel="noopener"><span>File and Directory Operations Commands</span></a></li>
<li value="2"><a href="#permission" rel="noopener"><span>File Permission Commands</span></a></li>
<li value="3"><a href="#compression" rel="noopener"><span>File Compression and Archiving Commands</span></a></li>
<li value="4"><a href="#management" rel="noopener"><span>Process Management Commands</span></a></li>
<li value="5"><a href="#system" rel="noopener"><span>System Information Commands</span></a></li>
<li value="6"><a href="#networking" rel="noopener"><span>Networking Commands</span></a></li>
<li value="7"><a href="#IO" rel="noopener"><span>IO Redirection Commands</span></a></li>
<li value="8"><a href="#environment" rel="noopener"><span>Environment Variable Commands</span></a></li>
<li value="9"><a href="#user" rel="noopener"><span>User Management Commands</span></a></li>
<li value="10"><a href="#shortcuts" rel="noopener"><span>Shortcuts Commands List</span></a>
<ul>
<li value="1"><a href="#bash" rel="noopener"><span>Bash Shortcuts Commands</span></a></li>
<li value="2"><a href="#nano" rel="noopener"><span>Nano Shortcuts Commands</span></a></li>
<li value="3"><a href="#VI" rel="noopener"><span>VI Shortcuts Commands</span></a></li>
<li value="4"><a href="#vim" rel="noopener"><span>Vim Shortcuts Commands</span></a></li>
</ul>
</li>
<li value="10"><a href="#faqs" rel="noopener"><span>FAQs on Linux Commands Cheat Sheet</span></a></li>
</ul>
</blockquote>
<h2><span>Basic Linux Commands with Examples</span></h2>
<p dir="ltr"><span>In this Linux cheat sheet, we will cover all the most important Linux commands, from the basics to the advanced. We will also provide some tips on how to practice and learn Linux commands. This cheat sheet is useful for Beginners and Experience professionals.</span></p>
<h2 id="directory"><span>1. File and Directory Operations Commands</span></h2>
<p dir="ltr"><span>File and directory operations are fundamental in working with the Linux operating system. Here are some commonly used File and Directory Operations commands:</span></p>
<table class="GFGEditorTheme__table">
<colgroup>
<col>
<col>
<col>
<col>
    </colgroup>
<thead>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Command</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Description</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Options</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Examples</strong></b></p>
</th>
</tr>
</thead>
<tbody>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/ls-command-in-linux/"><span>ls</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>List files and directories.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-l</strong></b><span>: Long format listing.</span></li>
<li value="2"><b><strong>-a</strong></b><span>: Include hidden files hidden ones</span></li>
<li value="3"><b><strong>-h</strong></b><span>: Human-readable file sizes.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>ls -l&nbsp;</strong></b><br><span>displays files and directories with detailed information.</span></li>
<li value="2"><b><strong>ls -a&nbsp;</strong></b><br><span>shows all files and directories, including</span></li>
<li value="3"><b><strong>ls -lh</strong></b><span>&nbsp;</span><br><span>displays file sizes in a human-readable format.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/cd-command-in-linux-with-examples/"><span>cd</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Change directory.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>cd /path/to/directory</strong></b><br><span>changes the current directory to the specified path.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/pwd-command-in-linux-with-examples/"><span>pwd</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Print current working directory.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>pwd&nbsp;</strong></b><br><span>displays the current working directory.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/mkdir-command-in-linux-with-examples/"><span>mkdir</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Create a new directory.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>mkdir my_directory</strong></b><br><span>creates a new directory named “my_directory”.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/rm-command-linux-examples/"><span>rm</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Remove files and directories.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-r</strong></b><span>: Remove directories recursively.</span></li>
<li value="2"><b><strong>-f</strong></b><span>: Force removal without confirmation.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>rm file.txt</strong></b><br><span>deletes the file named “file.txt”.</span></li>
<li value="2"><b><strong>rm -r my_directory</strong></b><br><span>deletes the directory “my_directory” and its contents.</span></li>
<li value="3"><b><strong>rm -f file.txt</strong></b><br><span>forcefully deletes the file “file.txt” without confirmation.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/cp-command-linux-examples/"><span>cp</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Copy files and directories.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-r</strong></b><span>: Copy directories recursively.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>cp -r directory destination&nbsp;</strong></b><br><span>copies the directory “directory” and its contents to the specified destination.</span></li>
<li value="2"><b><strong>cp file.txt destination&nbsp;</strong></b><br><span>copies the file “file.txt” to the specified destination.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/mv-command-linux-examples/"><b><strong>mv</strong></b></a></th>
<td class="GFGEditorTheme__tableCell"><span>Move/rename files and directories.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>mv file.txt new_name.txt</strong></b><span>&nbsp;</span><br><span>renames the file “file.txt” to “new_name.txt”.</span></li>
<li value="2"><b><strong>mv file.txt directory&nbsp;</strong></b><br><span>moves the file “file.txt” to the specified directory.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/touch-command-in-linux-with-examples/"><span>touch</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Create an empty file or update file timestamps.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>touch file.txt</strong></b><span>&nbsp;</span><br><span>creates an empty file named “file.txt”.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/cat-command-in-linux-with-examples/"><span>cat</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>View the contents of a file.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>cat file.txt</strong></b><span>&nbsp;</span><br><span>displays the contents of the file “file.txt”.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/head-command-linux-examples/"><span>head</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;Display the first few lines of a file.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-n</strong></b><span>: Specify the number of lines to display.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>head file.txt</strong></b><span>&nbsp;</span><br><span>shows the first 10 lines of the file “file.txt”.</span></li>
<li value="2"><b><strong>&nbsp;head -n 5 file.txt</strong></b><span>&nbsp;</span><br><span>displays the first 5 lines of the file “file.txt”.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/tail-command-linux-examples/"><span>tail</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Display the last few lines of a file.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-n</strong></b><span>: Specify the number of lines to display.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>tail file.txt</strong></b><span>&nbsp;</span><br><span>shows the last 10 lines of the file “file.txt”.</span></li>
<li value="2"><b><strong>tail -n 5 file.txt&nbsp;</strong></b><br><span>displays the last 5 lines of the file “file.txt”.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/ln-command-in-linux-with-examples/"><span>ln</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Create links between files.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-s</strong></b><span>: Create symbolic (soft) links.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>ln -s source_file link_name</strong></b><span>&nbsp;</span><br><span>creates a symbolic link named “link_name” pointing to “source_file”.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/find-command-in-linux-with-examples/"><span>find</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Search for files and directories.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-name</strong></b><span>: Search by filename.</span></li>
<li value="2"><b><strong>-type</strong></b><span>: Search by file type.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>find /path/to/search -name “*.txt”</strong></b><span>&nbsp;</span><br><span>searches for all files with the extension “.txt” in the specified directory.</span></li>
</ul>
</td>
</tr>
</tbody>
</table>
<h2 id="permission"><span>2. File Permission Commands</span></h2>
<p dir="ltr"><span>File permissions on Linux and Unix systems control access to files and directories. There are three basic permissions: read, write, and execute. Each permission can be granted or denied to three different categories of users: the owner of the file, the members of the file’s group, and everyone else.</span></p>
<p dir="ltr"><span>Here are some file permission commands:</span></p>
<table class="GFGEditorTheme__table">
<colgroup>
<col>
<col>
<col>
<col>
    </colgroup>
<thead>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Command&nbsp;</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Description</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Options</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Examples</strong></b></p>
</th>
</tr>
</thead>
<tbody>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/chmod-command-linux/"><span>chmod</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Change file permissions.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>u</strong></b><span>: User/owner permissions.</span></li>
<li value="2"><b><strong>g</strong></b><span>: Group permissions.</span></li>
<li value="3"><b><strong>o</strong></b><span>: Other permissions.</span></li>
<li value="4"><b><strong>+</strong></b><span>: Add permissions.</span></li>
<li value="5"><b><strong>–</strong></b><span>: Remove permissions.</span></li>
<li value="6"><b><strong>=</strong></b><span>: Set permissions explicitly.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>chmod u+rwx file.txt</strong></b><span>&nbsp;</span><br><span>grants read, write, and execute permissions to the owner of the file.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/chown-command-in-linux-with-examples/"><span>chown</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Change file ownership.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>chown user file.txt&nbsp;</strong></b><br><span>changes the owner of “file.txt” to the specified user.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/chgrp-command-in-linux-with-examples/"><span>chgrp</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Change group ownership.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>chgrp group file.txt&nbsp;</strong></b><br><span>changes the group ownership of “file.txt” to the specified group.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/umask-command-in-linux-with-examples/"><span>umask</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;Set default file permissions.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>umask 022</strong></b><span>&nbsp;</span><br><span>sets the default file permissions to read and write for the owner, and read-only for group and others.</span></li>
</ul>
</td>
</tr>
</tbody>
</table>
<h2 id="compression"><span>3. File Compression and Archiving Commands</span></h2>
<p dir="ltr"><span>Here are some file compression and archiving commands in Linux:</span></p>
<table class="GFGEditorTheme__table">
<colgroup>
<col>
<col>
<col>
<col>
    </colgroup>
<thead>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Commands</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Description</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Options</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Examples</strong></b></p>
</th>
</tr>
</thead>
<tbody>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/tar-command-linux-examples/"><span>tar</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Create or extract archive files.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-c</strong></b><span>: Create a new archive.</span></li>
<li value="2"><b><strong>-x</strong></b><span>: Extract files from an archive.</span></li>
<li value="3"><b><strong>-f</strong></b><span>: Specify the archive file name.</span></li>
<li value="4"><b><strong>-v</strong></b><span>: Verbose mode.</span></li>
<li value="5"><b><strong>-z</strong></b><span>: Compress the archive with gzip.</span></li>
<li value="6"><b><strong>-j</strong></b><span>: Compress the archive with bzip2.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>tar -czvf archive.tar.gz files/</strong></b><span>&nbsp;</span><br><span>creates a compressed tar archive named “archive.tar.gz” containing the files in the “files/” directory.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/gzip-command-linux/"><span>gzip</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Compress files.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-d</strong></b><span>: Decompress files.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>gzip file.txt&nbsp;</strong></b><br><span>compresses the file “file.txt” and renames it as “file.txt.gz”.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/zip-command-in-linux-with-examples/"><span>zip</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Create compressed zip archives.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-r</strong></b><span>: Recursively include directories.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>zip archive.zip file1.txt file2.txt</strong></b><span>&nbsp;</span><br><span>creates a zip archive named “archive.zip” containing “file1.txt” and “file2.txt”.</span></li>
</ul>
</td>
</tr>
</tbody>
</table>
<h2 id="management"><span>4. Process Management Commands</span></h2>
<p dir="ltr"><span>In Linux, process management commands allow you to monitor and control running processes on the system. Here are some commonly used process management commands:</span></p><div id="GFG_AD_gfg_outstream_incontent"></div>
<table class="GFGEditorTheme__table">
<colgroup>
<col>
<col>
<col>
<col>
    </colgroup>
<thead>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Commands</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Description</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Options</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Examples</strong></b></p>
</th>
</tr>
</thead>
<tbody>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/ps-command-in-linux-with-examples/"><span>ps</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Display running processes.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-aux</strong></b><span>: Show all processes.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>ps aux</strong></b><span>&nbsp;</span><br><span>shows all running processes with detailed information.</span><br><span>&nbsp;</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/top-command-in-linux-with-examples/"><span>top</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Monitor system processes in real-time.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>top&nbsp;</strong></b><br><span>displays a dynamic view of system processes and their resource usage.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/kill-command-in-linux-with-examples/"><span>kill</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Terminate a process.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-9</strong></b><span>: Forcefully kill a process.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>kill PID</strong></b><span>&nbsp;</span><br><span>terminates the process with the specified process ID.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/kill-command-in-linux-with-examples/"><span>pkill</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Terminate processes based on their name.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>pkill process_name</strong></b><span>&nbsp;</span><br><span>terminates all processes with the specified name.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>pgrep</span></th>
<td class="GFGEditorTheme__tableCell"><span>List processes based on their name.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>pgrep process_name</strong></b><span>&nbsp;</span><br><span>lists all processes with the specified name.</span><br><span>&nbsp;</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/grep-command-in-unixlinux/"><span>grep</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>used to search for specific patterns or regular expressions in text files or streams and display matching lines.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-i</strong></b><span>: Ignore case distinctions while searching.</span></li>
<li value="2"><b><strong>-v</strong></b><span>: Invert the match, displaying non-matching lines.</span></li>
<li value="3"><b><strong>-r or -R</strong></b><span>: Recursively search directories for matching patterns.</span></li>
<li value="4"><b><strong>-l</strong></b><span>: Print only the names of files containing matches.</span></li>
<li value="5"><b><strong>-n</strong></b><span>: Display line numbers alongside matching lines.</span></li>
<li value="6"><b><strong>-w</strong></b><span>: Match whole words only, rather than partial matches.</span></li>
<li value="7"><b><strong>-c</strong></b><span>: Count the number of matching lines instead of displaying them.</span></li>
<li value="8"><b><strong>-e</strong></b><span>: Specify multiple patterns to search for.</span></li>
<li value="9"><b><strong>-A</strong></b><span>: Display lines after the matching line.</span></li>
<li value="10"><b><strong>-B</strong></b><span>: Display lines before the matching line.</span></li>
<li value="11"><b><strong>-C</strong></b><span>: Display lines both before and after the matching line.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>&nbsp;grep -i “hello” file.txt</strong></b></li>
<li value="2"><b><strong>grep -v “error” file.txt</strong></b></li>
<li value="3"><b><strong>grep -r “pattern” directory/</strong></b></li>
<li value="4"><b><strong>grep -l “keyword” file.txt</strong></b></li>
<li value="5"><b><strong>grep -n “pattern” file.txt</strong></b><br><span>In these examples we are extracting our desirec output from filename (file.txt)</span></li>
</ul>
</td>
</tr>
</tbody>
</table>
<h2 id="system"><span>5. System Information Commands</span></h2>
<p dir="ltr"><span>In Linux, there are several commands available to gather system information. Here are some commonly used system information commands:</span></p>
<table class="GFGEditorTheme__table">
<colgroup>
<col>
<col>
<col>
<col>
    </colgroup>
<thead>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>sudCommand</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Description</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Options</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Examples</strong></b></p>
</th>
</tr>
</thead>
<tbody>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/uname-command-in-linux-with-examples/"><span>uname</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Print system information.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-a</strong></b><span>: All system information.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>uname -a&nbsp;</strong></b><br><span>displays all system information.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/whoami-command-linux-example/"><span>whoami</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Display current username.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>whoami</strong></b><span>&nbsp;</span><br><span>shows the current username.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/df-command-in-linux-with-examples/"><span>df</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Show disk space usage.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-h</strong></b><span>: Human-readable sizes.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>df -h</strong></b><span>&nbsp;</span><br><span>displays disk space usage in a human-readable format.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/du-command-linux-examples/"><span>du</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Estimate file and directory sizes.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-h</strong></b><span>: Human-readable sizes.</span></li>
<li value="2"><b><strong>-s</strong></b><span>: Display total size only.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>du -sh directory/</strong></b><span>&nbsp;</span><br><span>provides the total size of the specified directory.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/free-command-linux-examples/"><span>free</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Display memory usage information.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>-h</strong></b><span>: Human-readable sizes.</span></li>
</ul>
</td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>free -h</strong></b><span>&nbsp;</span><br><span>displays memory usage in a human-readable format.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/linux-uptime-command-with-examples/"><span>uptime</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Show system uptime.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>uptime&nbsp;</strong></b><br><span>shows the current system uptime.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>lscpu</span></th>
<td class="GFGEditorTheme__tableCell"><span>Display CPU information.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>lscpu</strong></b><span>&nbsp;</span><br><span>provides detailed CPU information.</span><br><span>&nbsp;</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>lspci</span></th>
<td class="GFGEditorTheme__tableCell"><span>List PCI devices.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>lspci</strong></b><br><span>List PCI devices.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/lsusb-command-in-linux-with-examples/"><span>lsusb</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>List USB devices.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>lsusb</strong></b><span>&nbsp;</span><br><span>lists all connected USB devices.</span><br><span>&nbsp;</span></li>
</ul>
</td>
</tr>
</tbody>
</table>
<h2 id="networking"><span>6. Networking Commands</span></h2>
<p dir="ltr"><span>In Linux, there are several networking commands available to manage and troubleshoot network connections. Here are some commonly used networking commands:</span></p>
<table class="GFGEditorTheme__table">
<colgroup>
<col>
<col>
<col>
    </colgroup>
<thead>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Command</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Description</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Examples</strong></b></p>
</th>
</tr>
</thead>
<tbody>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/ifconfig-command-in-linux-with-examples/"><span>ifconfig</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Display network interface information.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>ifconfig</strong></b><span>&nbsp;</span><br><span>shows the details of all network interfaces.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/ping-command-in-linux-with-examples/"><span>ping</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Send ICMP echo requests to a host.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>ping google.com</strong></b><span>&nbsp;</span><br><span>sends ICMP echo requests to “google.com” to check connectivity.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/netstat-command-linux/"><span>netstat</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Display network connections and statistics.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>netstat -tuln</strong></b><span>&nbsp;</span><br><span>shows all listening TCP and UDP connections.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>ss</span></th>
<td class="GFGEditorTheme__tableCell"><span>Display network socket information.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>ss -tuln</strong></b><span>&nbsp;</span><br><span>shows all listening TCP and UDP connections.</span><br><span>&nbsp;</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/ssh-command-in-linux-with-examples/"><span>ssh</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Securely connect to a remote server.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>ssh user@hostname</strong></b><span>&nbsp;</span><br><span>initiates an SSH connection to the specified hostname.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/scp-command-in-linux-with-examples/"><span>scp</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Securely copy files between hosts.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>scp file.txt user@hostname:/path/to/destination</strong></b><span>&nbsp;</span><br><span>securely copies “file.txt” to the specified remote host.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/wget-command-in-linux-unix/"><span>wget</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;Download files from the web.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>&nbsp;wget http://example.com/file.txt</strong></b><span>&nbsp;</span><br><span>downloads “file.txt” from the specified URL.</span></li>
</ul>
</td>
</tr>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><a href="https://www.geeksforgeeks.org/curl-command-in-linux-with-examples/"><span>curl</span></a></th>
<td class="GFGEditorTheme__tableCell"><span>Transfer data to or from a server.</span></td>
<td class="GFGEditorTheme__tableCell">
<ul>
<li value="1"><b><strong>curl http://example.com</strong></b><span>&nbsp;</span><br><span>retrieves the content of a webpage from the specified URL.</span></li>
</ul>
</td>
</tr>
</tbody>
</table>
<h2 id="IO"><span>7. IO Redirection Commands&nbsp;</span></h2>
<p dir="ltr"><span>In Linux, IO (Input/Output) redirection commands are used to redirect the standard input, output, and error streams of commands and processes. Here are some commonly used IO redirection commands:</span></p>
<table class="GFGEditorTheme__table">
<colgroup>
<col>
<col>
    </colgroup>
<thead>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Command</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Description</strong></b></p>
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="GFGEditorTheme__tableCell"><span>cmd &lt; file</span></td>
<td class="GFGEditorTheme__tableCell"><span>Input of cmd is taken from file.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><span>cmd &gt; file</span></td>
<td class="GFGEditorTheme__tableCell"><span>Standard output (stdout) of cmd is redirected to file.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><span>cmd 2&gt; file</span></td>
<td class="GFGEditorTheme__tableCell"><span>Error output (stderr) of cmd is redirected to file.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><span>cmd 2&gt;&amp;1</span></td>
<td class="GFGEditorTheme__tableCell"><span>stderr is redirected to the same place as stdout.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><span>cmd1 &lt;(cmd2)</span></td>
<td class="GFGEditorTheme__tableCell"><span>Output of cmd2 is used as the input file for cmd1.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><span>cmd &gt; /dev/null</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;Discards the stdout of cmd by sending it to the null device.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><span>cmd &amp;&gt; file</span></td>
<td class="GFGEditorTheme__tableCell"><span>Every output of cmd is redirected to file.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><span>cmd 1&gt;&amp;2</span></td>
<td class="GFGEditorTheme__tableCell"><span>stdout is redirected to the same place as stderr.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><span>cmd &gt;&gt; file</span></td>
<td class="GFGEditorTheme__tableCell"><span>Appends the stdout of cmd to file.</span></td>
</tr>
</tbody>
</table>
<h2 id="environment"><span>8. Environment Variable Commands</span></h2>
<p dir="ltr"><span>In Linux, environment variables are used to store configuration settings, system information, and other variables that can be accessed by processes and shell scripts. Here are some commonly used environment variable commands:</span></p>
<table class="GFGEditorTheme__table">
<colgroup>
<col>
<col>
    </colgroup>
<thead>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Command</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Description</strong></b></p>
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>export VARIABLE_NAME=value</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Sets the value of an environment variable.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>echo $VARIABLE_NAME</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Displays the value of a specific environment variable.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>env</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Lists all environment variables currently set in the system.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>unset VARIABLE_NAME</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Unsets or removes an environment variable.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>export -p</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Shows a list of all currently exported environment variables.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>env VAR1=value COMMAND</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Sets the value of an environment variable for a specific command.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>printenv</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Displays the values of all environment variables.</span></td>
</tr>
</tbody>
</table>
<h2 id="user"><span>9. User Management Commands</span></h2>
<p dir="ltr"><span>In Linux, user management commands allow you to create, modify, and manage user accounts on the system. Here are some commonly used user management commands:</span></p>
<table class="GFGEditorTheme__table">
<colgroup>
<col>
<col>
    </colgroup>
<thead>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Command&nbsp;</strong></b></p>
</th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader">
<p dir="ltr" style="text-align: center;"><b><strong>Description</strong></b></p>
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>who</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Show who is currently logged in.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>sudo adduser username</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;Create a new user account on the system with the specified username.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>finger</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Display information about all the users currently logged into the system, including their usernames, login time, and terminal.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>sudo deluser USER GROUPNAME</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Remove the specified user from the specified group.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>last</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Show the recent login history of users.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>finger username</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Provide information about the specified user, including their username, real name, terminal, idle time, and login time.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>sudo userdel -r username</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Delete the specified user account from the system, including their home directory and associated files. The -r option ensures the removal of the user’s files.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>sudo passwd -l username</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Lock the password of the specified user account, preventing the user from logging in.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>su – username</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Switch to another user account with the user’s environment.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>sudo usermod -a -G GROUPNAME USERNAME</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;Add an existing user to the specified group. The user is added to the group without removing them from their current groups.</span></td>
</tr>
</tbody>
</table>
<h2 id="shortcuts"><span>10. Shortcuts Commands</span></h2>
<p dir="ltr"><span>There are many shortcuts commands in Linux that can help you be more productive. Here are a few of the most common ones:</span></p>
<h3 id="bash"><span>10.1: Bash Shortcuts Commands:</span></h3>
<table class="GFGEditorTheme__table">
<colgroup>
<col>
<col>
<col>
<col>
<col>
<col>
    </colgroup>
<thead>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Navigation</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Description</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Editing</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Description</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>History</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Description</span></th>
</tr>
</thead>
<tbody>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + A</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Move to the beginning of the line.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + U</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Cut/delete from the cursor position to the beginning of the line.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + R</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Search command history (reverse search).</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + E</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Move to the end of the line.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + K</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Cut/delete from the cursor position to the end of the line.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + G</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Escape from history search mode.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + B</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Move back one character.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + W</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Cut/delete the word before the cursor.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + P</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;Go to the previous command in history.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + F</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Move forward one character.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + Y</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Paste the last cut text.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + N</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Go to the next command in history.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>Alt + B</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Move back one word</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + L</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Clear the screen.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + C</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Terminate the current command.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>Alt + F</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Move forward one word.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
</tr>
</tbody>
</table>
<h3 id="nano"><span>10.2: Nano Shortcuts Commands:</span></h3>
<table class="GFGEditorTheme__table">
<colgroup>
<col>
<col>
<col>
<col>
<col>
<col>
<col>
<col>
    </colgroup>
<thead>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>File Operations</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Description</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Navigation</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Description</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Editing</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Description</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Search and Replace</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Description</span></th>
</tr>
</thead>
<tbody>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + O</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;Save the file.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + Y</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Scroll up one page.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + K</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Cut/delete from the cursor position to the end of the line.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + W</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Search for a string in the text.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + X</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Exit Nano (prompt to save if modified).</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + V</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Scroll down one page.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + U</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Uncut/restore the last cut text.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Alt + W</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Search and replace a string in the text.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + R</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Read a file into the current buffer.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Alt + \</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Go to a specific line number.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + 6</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Mark a block of text for copying or cutting.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Alt + R</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Repeat the last search.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + J</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Justify the current paragraph.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Alt + ,</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;Go to the beginning of the current line.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + K</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Cut/delete the marked block of text.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Alt + .</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Go to the end of the current line.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>Alt + 6</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Copy the marked block of text.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
</tr>
</tbody>
</table>
<h3 id="VI"><span>10.3: VI Shortcuts Commands:</span></h3>
<table class="GFGEditorTheme__table">
<colgroup>
<col>
<col>
    </colgroup>
<thead>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><b><strong>Command</strong></b></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><b><strong>Description</strong></b></th>
</tr>
</thead>
<tbody>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>cw</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Change the current word. Deletes from the cursor position to the end of the current word and switches to insert mode.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>dd</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Delete the current line.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>x</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Delete the character under the cursor.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>R</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Enter replace mode. Overwrites characters starting from the cursor position until you press the Escape key.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>o</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Insert a new line below the current line and switch to insert mode.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>u</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Undo the last change.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>s</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Substitute the character under the cursor and switch to insert mode.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>dw</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Delete from the cursor position to the beginning of the next word.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>D</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Delete from the cursor position to the end of the line.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>4dw</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Delete the next four words from the cursor position.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>A</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Switch to insert mode at the end of the current line.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>S</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Delete the current line and switch to insert mode.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>r</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Replace the character under the cursor with a new character entered from the keyboard.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>i</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Switch to insert mode before the cursor.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>3dd</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Delete the current line and the two lines below it.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>ESC</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Exit from insert or command-line mode and return to command mode.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>U</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Restore the current line to its original state before any changes were made.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>~</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Switch the case of the character under the cursor.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>a</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Switch to insert mode after the cursor.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>C</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Delete from the cursor position to the end of the line and switch to insert mode.</span></td>
</tr>
</tbody>
</table>
<h3 id="vim"><span>10.4: Vim Shortcuts Commands:</span></h3>
<table class="GFGEditorTheme__table">
<colgroup>
<col>
<col>
<col>
<col>
<col>
<col>
    </colgroup>
<thead>
<tr>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Normal Mode</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Description</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Command Mode</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Description</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Visual Mode</span></th>
<th class="GFGEditorTheme__tableCell GFGEditorTheme__tableCellHeader"><span>Description</span></th>
</tr>
</thead>
<tbody>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>i</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Enter insert mode at the current cursor position.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>:w</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Save the file.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>v</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Enter visual mode to select text.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>x</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Delete the character under the cursor.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>:q</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Quit Vim.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>y</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Copy the selected text.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>dd</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Delete the current line.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>:q!</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Quit Vim without saving changes.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>d</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Delete the selected text.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>yy</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Copy the current line.</span></td>
<td class="GFGEditorTheme__tableCell">
<p dir="ltr"><b><strong>:wq</strong></b></p>
<p dir="ltr"><span>or</span></p>
<p dir="ltr"><b><strong><img draggable="false" class="emoji" alt="😡" src="https://s.w.org/images/core/emoji/11/svg/1f621.svg"></strong></b></p>
</td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;Save and quit Vim.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>p</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Paste the copied or deleted text.</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>p</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Paste the copied or deleted text below the current line.</span></td>
<td class="GFGEditorTheme__tableCell"><b><strong>:s/old/new/g</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Replace all occurrences of “old” with “new” in the file.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>u</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Undo the last change.</span></td>
<td class="GFGEditorTheme__tableCell">
<p dir="ltr"><b><strong>:set nu</strong></b></p>
<p dir="ltr"><span>or</span></p>
<p dir="ltr"><b><strong>:set number</strong></b></p>
</td>
<td class="GFGEditorTheme__tableCell"><span>Display line numbers.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
</tr>
<tr>
<td class="GFGEditorTheme__tableCell"><b><strong>Ctrl + R</strong></b></td>
<td class="GFGEditorTheme__tableCell"><span>Redo the last undo.</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
<td class="GFGEditorTheme__tableCell"><span>&nbsp;</span></td>
</tr>
</tbody>
</table>
<h2><span>Conclusion</span></h2>
<p dir="ltr"><span>In conclusion, Linux is a widely used operating system for development, and as a developer, you should have knowledge of Linux and its basic commands. In this Cheat Sheet, we covered all commands like creating directories, file compression and archiving, process management, system information, networking and more. In addition to that, this Linux Cheat Sheet is organized and categorized, making it easy for developers to quickly find the commands they need for specific use cases. By utilizing this resource, developers can enhance their productivity and efficiency in working with Linux, leading to smoother and more successful development projects.</span></p>
<p dir="ltr"><b></b></p><b>
</b><blockquote><b></b><p><b><strong>PS.</strong></b><span>&nbsp;Don’t miss our other Python cheat sheet for data science that covers&nbsp;</span><a href="https://www.geeksforgeeks.org/learning-model-building-scikit-learn-python-machine-learning-library/"><span>Scikit-Learn</span></a><span>,&nbsp;</span><a href="https://www.geeksforgeeks.org/python-data-visualization-using-bokeh/"><span>Bokeh</span></a><span>,&nbsp;</span><a href="https://www.geeksforgeeks.org/pandas-tutorial/"><span>Pandas</span></a><span>&nbsp;and </span><a href="https://www.geeksforgeeks.org/python-programming-language/"><span>Python basics</span></a><span>.</span></p>
</blockquote>
<h2 id="faqs"><span>FAQs on Linux Commands Cheat Sheet</span></h2>
<h3><span>1. What is Linux Cheat Sheet?</span></h3>
<blockquote>
<p dir="ltr"><span>When your memory fails or you prefer not to rely on “linux </span><b><strong>–help</strong></b><span>?” in the Terminal, this linux cheat sheet comes to the rescue. It is hard to memorize all the important linux Commandsby heart, so print this out or save it to your desktop to resort to when you get stuck.</span></p>
</blockquote>
<h3><span>2.What are the basics of Linux?</span></h3>
<blockquote>
<ul>
<li value="1"><b><strong>Kernel</strong></b><span>. The base component of the OS. Without it, the OS doesn’t work. …</span></li>
<li value="2"><b><strong>System user space</strong></b><span>. The administrative layer for system-level tasks like configuration and software install. …</span></li>
<li value="3"><b><strong>Applications</strong></b><span>. A type of software that lets you perform a task.</span></li>
</ul>
</blockquote>
<h3><span>3. What is 777 in Linux command?</span></h3>
<blockquote>
<p dir="ltr"><span>You might have heard of chmod 777. This command will&nbsp;</span><b><strong>give read, write and execute permission to the owner, group and public</strong></b><span>.</span></p>
</blockquote>
<h3><span>4. How do I see what users are doing in Linux?</span></h3>
<blockquote>
<p dir="ltr"><b><strong>Using the w Command, </strong></b><span>w command in Linux shows logged-in users and their activities.</span></p>
</blockquote>
<br><div id="AP_G4GR_6"></div><div class="article_bottom_text"><p>Learn to code easily with our course <a href="https://www.geeksforgeeks.org/courses/coding-for-everyone?utm_source=geeksforgeeks&amp;utm_medium=article_bottom_text&amp;utm_campaign=courses" target="_blank" rel="noopener">Coding for Everyone</a>. This course is accessible and designed for everyone, even if you're new to coding. Start today and join millions on a journey to improve your skills!</p>
<p>Whether you're preparing for your first job interview or aiming to upskill in this ever-evolving tech landscape, <a href="https://www.geeksforgeeks.org/courses?utm_source=geeksforgeeks&amp;utm_medium=article_bottom_text&amp;utm_campaign=courses" target="_blank" rel="noopener">GeeksforGeeks Courses</a> are your key to success. We provide top-quality content at affordable prices, all geared towards accelerating your growth in a time-bound manner. Join the millions we've already empowered, and we're here to do the same for you. Don't miss out - <a href="https://www.geeksforgeeks.org/courses?utm_source=geeksforgeeks&amp;utm_medium=article_bottom_text&amp;utm_campaign=courses" target="_blank" rel="noopener">check it out now</a>!</p></div><br>                                    <style>
                                    .three90cta{
                                        background:#fffdd0; color:#000 !important; text-decoration:none !important; text-align:center;padding:0px 5px;
                                        line-height: 1.5;
                                        font-size: 17px;
                                        font-family: var(--font-secondary);
                                    }
                                    .three90cta:hover{
                                        text-decoration:underline !important;
                                    }
                                    </style>
                                    <a href="https://www.geeksforgeeks.org/courses?itm_source=geeksforgeeks&amp;itm_medium=article&amp;itm_campaign=three90" class="three90cta">Commit to GfG's Three-90 Challenge! Purchase a course, complete 90% in 90 days, and save 90% cost <span style="text-decoration:underline;">click here</span> to explore.</a>
                                    
                            <div class="article-bottom-buttons" style="margin-top:15px; margin-bottom: 0.5%;display:flex;">
                                                                    <div style="font-family:var(--font-primary);color:var(--gfg-color-lg);font-size:16px;">
                                        <span class="strong">Last Updated : </span>
                                        <span>24 Aug, 2023</span>
                                    </div>
                                                                <div pid="1034924" class="article--viewer_like tooltip tooltipBottom" style="margin-left:auto;">
                                    <span class="tooltiptext likeTooltipBottom">Like Article</span>
                                    <button aria-label="like article" data-gfg-action="like-article" data-bookmark-value="0">
                                        <i class="gfg-icon gfg-icon_thumbs"></i>
                                        <figure style="margin-left: 3px;" class="favoriteText">10</figure>
                                    </button>
                                </div>
                                <div pid="1034924" class="article--viewer_bookmark tooltip tooltipBottom">
                                    <span class="tooltiptext">Save Article</span>
                                    <button aria-label="bookmark article" data-gfg-action="bookmark-article" data-bookmark-value="0">
                                        <i class="gfg-icon gfg-icon_bookmark"></i>
                                    </button>
                                </div>
                            </div>

                            <div class="d-row content-bw article-pgnavi v-divider-gfg" style="margin-top: 20px;">
                                                            <div class="article-pgnavi_prev">
                                    <a href="https://www.geeksforgeeks.org/numpy-cheat-sheet/?ref=lbp" class="pg-head">
                                        <span class="gfg-icon gfg-icon_previous"></span>
                                        <span style="margin-left: 5px;">Previous</span>
                                    </a>
                                    <!-- <div class="pg-meta">8 Min Read&ensp;|&ensp;<a href="#">Java</a></div> -->
                                    <div class="pg-main">
                                        <a href="https://www.geeksforgeeks.org/numpy-cheat-sheet/?ref=lbp">NumPy Cheat Sheet: Beginner to Advanced (PDF)</a>
                                    </div>
                                </div>
                                                            <div class="article-pgnavi_next">
                                    <a href="https://www.geeksforgeeks.org/pandas-cheat-sheet/?ref=lbp" class="pg-head">
                                        <span style="margin-right: 5px; margin-left: auto;">Next</span>
                                        <span class="gfg-icon gfg-icon_next"></span>
                                    </a>
                                    <!-- <div class="pg-meta">8 Min Read&ensp;|&ensp;<a href="#">Java</a></div> -->
                                    <div class="pg-main">
                                        <a href="https://www.geeksforgeeks.org/pandas-cheat-sheet/?ref=lbp">Pandas Cheat Sheet for Data Science in Python</a>
                                    </div>
                                </div>
                                                        </div>
                            
    <div class="discussion_panel">
        <div>
            <span id="discussion_message">Share your thoughts in the comments</span>
        </div>
        <button class="discussion_button" data-gfg-action="loadComments">
                <span>Add Your Comment</span>
        </button>
    </div>                            <div class="onopen-discussion-panel">
            <div class="discussion-tab">
                <div class="discussion_heading">
                    <div></div>
                    <i class="gfg-icon close-tab-icon"></i>
                </div> 
                <div class="discussion_content">    <div id="login-link" style="text-align: center; padding: 10px 0px 20px 16px; display: none;"> <h3>Please <u><span class="login-modal-btn" style="cursor:pointer;color: #308d46;">Login</span></u> to comment...</h3></div>
                            <div style="height:100%">
                                <div style="height:100%" id="comment-system"></div>
                            </div>

                            
</div>
            </div>
        </div> 
                        </div>