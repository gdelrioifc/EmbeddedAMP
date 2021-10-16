<h1>CAMPred</h1>

<h3><i>A distributed GO implementation to remotely run predictions from <a href="http://www.camp.bicnirrh.res.in/predict/">CAMP website</a></i></h3>

<h2><b>Requirements</b></h2>
<ol>
  <li><a href="https://golang.org">Go</a> binary distribution</li>
</ol>

<h2><b>Installation</b></h2>
If you just want to use the default settings, simply type:
<ul>
  <li>go build</li>
</ul>

This will create a binary file named <i>campred</i>.

If you prefer to have the <i>inprot</i> binary located at the /usr/local/ directory of yor system, you need to copy it to the desired location.

<h2><b>Executing CAMPred</b></h2>
To learn about the options available during the execution of CAMPred, please type the following command:
<ul>
  <li>campred -h</li>
</ul>

This will display the following information:

<table border=0>
 <tr><td colspan=2>Usage: campred FLAGS ARGUMENTS</td></tr>
 <tr><td colspan=2>CAMPRED - CAMP AMP PREDictions v0.1</td></tr>
 <tr><td colspan=2><br></td></tr>
 <tr><td colspan=2><br></td></tr>
 <tr><td colspan=2>Flags:</td></tr>
  <tr><td>-h, --help</td><td>Print this help message</td></tr>
  <tr><td>-i, --input string</td><td>Input filename</td></tr>
  <tr><td>-k, --keep</td><td>Keep intermediate file (default true)</td></tr>
  <tr><td>-n, --nseqs n</td><td>Split in multiple parts each one (default 1)</td></tr>
  <tr><td>-o, --output string</td><td>Output filename</td></tr>
  <tr><td>-s, --send int</td><td>Max number of times to send each request (max. 10) (default 10)</td></tr>
  <tr><td>-t, --threads int</td><td>Number of threads (default "XXX")</td></tr>
  <tr><td>-v, --verbose</td><td>Show extra information</td></tr>
  <tr><td colspan=2><br></td></tr>
  <tr><td colspan=2><br></td></tr>
  <tr><td colspan=2>Arguments:</td></tr>
  <tr><td colspan=2><br></td></tr>
  <tr><td>svm</td><td>Support Vector Machine</td></tr>
  <tr><td>ann</td><td>Artificial Neural Network</td></tr>
  <tr><td>rf</td><td>Random Forest</td></tr>
  <tr><td>da</td><td>Discriminant Analysis</td></tr>
  <tr><td>all</td><td>All the algorithm above</td></tr>
</table>

