<h1>InProt</h1>

<h3><i>A distributed C++ implemention of a method aimed to identify unique k-mers embedded in proteomes</i></h3>

<h2><b>Requirements</b></h2>
<ol>
  <li>C++ compiler compatible with version 14, including:</li>
    <ul>
      <li>GCC 5.0 or higher</li>
      <li>Intel C++ Compiler 17 or higher</li>
      <li>Clang 3.4 or higher</li>
      <li>Microsoft Visual C++ 2017 or higher</li>
    </ul>
  <li>CMake version 3.6 or higher and GNU Make</li>
  <li>Intel TBB library version 4.4 or higher</li>
  <li>Operating system: GNU/Linux, Unix (e.g., Mac OS, BSD) or Windows</li>
</ol>

<h2><b>Installation</b></h2>
If you just want to use the default settings, simply type:
<ul>
  <li>mkdir build</li>
  <li>cd build</li>
  <li>cmake -DCMAKE_BUILD_TYPE=Release x
  <li>make</li>
</ul>

Release x specifies the release version you may want to specify for your installation.

This will create a binary file named <i>inprot</i>.

If you prefer to have the <i>inprot</i> binary located at the /usr/local/ directory of yor system, you need to type the following set of instructions:
<ul>
  <li>mkdir build</li>
  <li>cd build</li>
  <li>cmake -DCMAKE_BUILD_TYPE=Release x
  <li>make PREFIX=/usr/local</li>
</ul>

<h2><b>Other installation variants</b></h2>
InProt includes 2 SVM trained algorithms to identify antimicrobial peptides (AMP). Both rendered very similar results, yet are provided for the users to play with them. The default SVM does not use the LibSVM implementation; if the user wants to use the LibSVM algorithm trained to identify AMP, the line 44 of the file "CMakeList.txt" has to state:

<ul>
  <li><b>set(USE_LIBSVM TRUE)</b></li>
</ul>

Another variant is to change the floting point type to use. By default, InProt uses <i>double</i> precision to calculate the 51 molecular descriptors of AMP. If your machine does not have enough resources, it may be recommended to change this default setting. To change this, in the file <i>main.cpp</i> change the MD_T = double for float, as follows:
<ul>
  <li>using MD_T = float;</li>
</ul>

After any of these changes, the code may be compiled as described above.


<h2><b>Executing InProt</b></h2>
To learn about the options available during the execution of InProt, please type the following command:
<ul>
  <li>inprot -h</li>
</ul>

This will display the following information:

<table border=0>
 <tr><td colspan=2>InProt - In silico Proteolysis</td></tr>
 <tr><td colspan=2>Usage: inprot [OPTIONS]</td></tr>
 <tr><td colspan=2><br></td></tr>
 <tr><td colspan=2><br></td></tr>
 <tr><td colspan=2>Options:</td></tr>
  <tr><td>-h, --help</td><td>Print this help message</td></tr>
  <tr><td>-i, --input TEXT</td><td>Proteome's file where to extract the k-mers</td></tr>
  <tr><td>-o, --output TEXT</td><td>Output's basename where to put the AMP-predicted k-mers</td></tr>
  <tr><td>-s, --scaling TEXT</td><td>SVM's scaling factors configuration file</td></tr>
  <tr><td>-m, --model TEXT</td><td>SVM's model file</td></tr>
  <tr><td>-l, --lower UINT</td><td>Lower k-mer size (minimum = 10)</td></tr>
  <tr><td>-u, --upper UINT</td><td>Upper k-mer size (maximum = 200)</td></tr>
  <tr><td>-t, --threads INT</td><td>Number of threads (0 = for automatic determination (default). Maximum = XXX)</td></tr>
  <tr><td>-w, --write UINT</td><td>Write predicted k-mers (0 = none, 1 = amps, 2 = namps, 3 = both, default = none)</td></tr>
  <tr><td>-a, --aware</td><td>Enable aware mode (low memory consumption; default false)</td></tr>
  <tr><td>-v, --verbose</td><td>Enable verbose mode (show extra information)</td></tr>
</table>


