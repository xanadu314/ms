---


---

<h2 id="proteome-discoverer-for-proteinpeptide-identification"><em>Proteome Discoverer</em> for protein/peptide identification</h2>
<h3 id="proprietary-formats">Proprietary formats</h3>

<table>
<thead>
<tr>
<th>company</th>
<th>extension</th>
<th>file type</th>
<th>location in HAZU</th>
</tr>
</thead>
<tbody>
<tr>
<td>Thermo</td>
<td>.raw</td>
<td>Thermo Xcalibur</td>
<td>第二综合楼A123</td>
</tr>
<tr>
<td>ABI/Sciex</td>
<td>.wiff</td>
<td>ABI/Sciex</td>
<td>二综A123/三综</td>
</tr>
<tr>
<td>Agilent/Bruker</td>
<td>.yep</td>
<td>instrument data format</td>
<td>食科5楼</td>
</tr>
</tbody>
</table><h3 id="formats-conversion">Formats conversion</h3>
<p>In the Mascot generic <em>format</em>, (<em>MGF</em>), each MS/MS dataset is a list of pairs of mass and intensity values, delimited by BEGIN IONS and END IONS statements.<br>
MGF is general format without compression.</p>
<ul>
<li>Conversion by equiped software(PeakView®, PEAKS etc.)</li>
<li>Conversion by general software ([ProteoWizard ](</li>
</ul>
<h4 id="operation-example">operation example</h4>
<p><img src="https://i.bmp.ovh/imgs/2020/03/de6a26138886848e.png" alt="ProteoWizard "><br>
delete 0.0000 intensity in mgf file(not requirement）<br>
./delete_0_in_mgf.sh 转换后mgf格式质谱文件<br>
delete_0_in_mgf.sh文件内容：</p>
<pre class=" language-undefined"><code class="prism language-{bash} language-undefined">##~~~ hyx 13/01/2020
# !/bin/bash
echo "运行方式：./delete_0_in_mgf.sh 文件名"
sed -i '/0.0000/d' $1
                    
</code></pre>
<h3 id="database-prepared">Database prepared</h3>
<h4 id="download-species-protein-database">Download species protein database</h4>
<p>from uniprot(<a href="http://www.uniprot.com">www.uniprot.com</a>) or other database.<br>
<img src="https://i.bmp.ovh/imgs/2020/03/66c79d161f5f453b.png" alt="enter image description here"></p>
<h4 id="select-protein-modification">Select protein modification</h4>
<p>Obtain monoisotopic mass of protein modification form unimod website(<a href="http://www.unimod.org/">http://www.unimod.org/</a>)</p>
<h3 id="pd-workflow">PD workflow</h3>
<h4 id="add-protein-database-to-pd-software">Add protein database to PD software</h4>
<p><img src="https://i.bmp.ovh/imgs/2020/03/2b2e627598fa757f.png" alt="enter image description here"></p>
<h4 id="add-protein-modification-to-pd-software">Add protein modification to PD software</h4>
<p>蛋白质修饰主要来源于氨基酸的氧化和加工过程中的修饰<br>
<img src="https://i.bmp.ovh/imgs/2020/03/f5dbedd46c9d32dc.png" alt="enter image description here"></p>
<h4 id="processing-workflow">Processing workflow</h4>
<p><img src="https://i.bmp.ovh/imgs/2020/03/47d6c8e2704b0a75.png" alt="enter image description here"></p>
<h3 id="reference">Reference</h3>
<ul>
<li>A cross-platform toolkit for mass spectrometry and proteomics. Chambers, M.C., MacLean, B., Burke, R., Amode, D., Ruderman, D.L., Neumann, S., Gatto, L., Fischer, B., Pratt, B., Egertson, J., Hoff, K., Kessner, D., Tasman, N., Shulman, N., Frewen, B., Baker, T.A., Brusniak, M.-Y., Paulse, C., Creasy, D., Flashner, L., Kani, K., Moulding, C., Seymour, S.L., Nuwaysir, L.M., Lefebvre, B., Kuhlmann, F., Roark, J., Rainer, P., Detlev, S., Hemenway, T., Huhmer, A., Langridge, J., Connolly, B., Chadick, T., Holly, K., Eckels, J., Deutsch, E.W., Moritz, R.L., Katz, J.E., Agus, D.B., MacCoss, M., Tabb, D.L. &amp; Mallick, P. Nature Biotechnology 30, 918-920</li>
</ul>

