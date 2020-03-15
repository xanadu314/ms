---


---

<h2 id="英国“躺平”了！群体免疫为什么需要60的感染比例？最终的结果又将如何？">英国“躺平”了！群体免疫为什么需要60%的感染比例？最终的结果又将如何？</h2>
<h3 id="将在失去所爱的人之前先失去他们自己">将在失去所爱的人之前先失去他们自己</h3>
<blockquote>
<p>Boris Johnson has warned that many more British families ‘are going to<br>
lose loved ones before their time’ as he addressed the global<br>
coronavirus pandemic.   Johnson said the UK has now officially moved<br>
from the ‘containment’ phase of dealing with the pandemic, to the<br>
‘delay’ phase, which aims to hold-up the spread of the virus and<br>
‘thereby minimise the suffering’.<a href="#ref_1">[1]</a></p>
</blockquote>
<p>英国首相鲍里斯·约翰森在3月12日发表讲话表示，英国将采取群体免疫的策略，更多的英国家庭“ 将在失去所爱的人之前失去他们自己”。</p>
<h3 id="群体免疫（herd-immunity）">群体免疫（Herd Immunity）</h3>
<p>群体免疫（Herd Immunity）是一种间接保护免受传染病的形式，这种传染病是在大部分人口已经对感染免疫后发生的，从而保护没有免疫力的人。<a href="#2">2</a><br>
张文宏医生在日前采访中也提到，人群中疫苗接种达到一定比例，就能形成群体免疫，从而保护那些没有打疫苗的人。<a href="#3">[3]</a><br>
简单来说，如果除了你以外，其他人都打了某种传染病的疫苗，那么其他人都不会被传染，你自己虽然对该疾病没有免疫力，但也是安全的。</p>
<h3 id="群体免疫比例的计算">群体免疫比例的计算</h3>
<p>很多同学都见过这样一张图：<br>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f5/Herd_immunity.svg/495px-Herd_immunity.svg.png" alt="群体免疫"><br>
看图我们能大致明白，当绝大多数人获得了免疫，那么易感人群也安全了，但是这个绝大多数的比例该如何计算呢？<br>
这里要引入第一个概念，也是我们熟悉的概念R<sub>0</sub><br>
<strong>基本传染数（Basic reproduction number）</strong> 是在流行病学上，指在没有外力介入，同时所有人都没有免疫力的情况下，一个感染到某种传染病的人，会把疾病<strong>传染</strong>给其他多少个人的<strong>平均数</strong>。记为R<sub>0</sub><br>
简单来说就是一个人能传染多少人，但值得注意这里的R<sub>0</sub>是一个统计学概念上的平均数，个例不具有代表性。<br>
第二个概念是临界接种水平(Critical vaccination level)简称 V<sub>c</sub>，简单来说就是多大比例的人群获得了免疫后，传染病才会逐渐停止传播。<br>
其实，根据这两个指标就可以计算出英国政府首席科学顾问，帕特里克·瓦朗斯爵士（Patrick Vallance）说的大约60%这个值了。<br>
先来看一个比较简单的模型：<br>
当R<sub>0</sub>=4时，一个传播者可以传给4个易感者，4个感染者可以再传给16个易感者。<br>
<img src="https://i.bmp.ovh/imgs/2020/03/06a59e8f0cb6b101.png" alt="enter image description here"><br>
当人群中刚好有75%的人获得了完美的免疫能力，则出现了一个有意思的现象：<br>
<img src="https://i.bmp.ovh/imgs/2020/03/146b9eb8f33c9777.png" alt="enter image description here"><br>
可以发现一个有意思的现象，即传染病刚好只能一个人传一个人。可以想象，当人群中的免疫者比例大于75%时，传染病的传播能力就会越来越弱[4]，因此，R<sub>0</sub>=4时，V<sub>c</sub>=75%，基本传播系数和非免疫人群比例的乘积为1时，刚好是临界接种水平，我们可以得到公式</p>
<p>R<sub>0</sub>*(1-V<sub>c</sub>)=1</p>
<p>针对新冠肺炎，世界卫生组织和香港大学的研究者总结了自2019年底疫情成熟开始的两个个月内的确诊病例数据，将R<sub>0</sub>系数提升至2.68，95%置信区间则被缩小到2.47-2.86[5]. 用R<sub>0</sub>=2.68计算V<sub>c</sub>=(2.68-1)/2.68=0.63，大约就是60%。<br>
<img src="https://i.bmp.ovh/imgs/2020/03/4599c74583c263cf.png" alt="enter image description here"><br>
以上预测的前提是感染后的幸存者获得完美的免疫力，事实往往是不尽如人意的，我们还要加上一个参数E(Vaccine effectiveness against transmission),来表达免疫的效果。<br>
完整公式为<br>
R<sub>0</sub>*(1-V<sub>c</sub>*E)=1<br>
V<sub>c</sub>=(1-1/R<sub>0</sub>)/E<br>
可以发现，当E&lt;1时，需要更大的V<sub>c</sub>, 也就是更大比例的免疫者，才能阻止疾病的传播。</p>
<h3 id="英国会发生什么？">英国会发生什么？</h3>
<p>疫情的发展是随着时间而变化的。<br>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c5/Covid-19-curves-graphic-social-v3.gif/1200px-Covid-19-curves-graphic-social-v3.gif" alt="enter image description here"><br>
英国希望通过管控，拉长疫情的发展时间，降低单位时间累计患者的数量。那么，疫情究竟会如何发展呢？我们考虑2个极端的情况：<br>
基于SIR模型的模拟<br>
<img src="https://ftp.bmp.ovh/imgs/2020/03/e7cf7c350a9323bf.png" alt="enter image description here"></p>
<ul>
<li>1 英国政府严加管控，让R<sub>0</sub>长时间保持较小值（略大于1），大约要花13个月的时间“实现”感染60%的国民，最高峰为单天感染60万人。</li>
<li>2 英国政府的管控力度一直很弱，病例增速先快后慢，英国人口的60%约为40，000，000，大约5个月的时间，英国会“实现”感染60%国民的目标，最高峰为单天感染610万人。<br>
再考虑医疗资源和致死率，没有疫苗的条件下，通过感染病毒实现群体免疫的情况是十分可怕的。<br>
你有可能会问，为什么感染者不可能是线性增长呢？即使通过神乎其神的管控，使病例线性增长，如果每天增长10000人，那么也需要4000天也就是11年的时间才能实现感染60%的国民，形成群体免疫。这对英国来说，是不可接受的。</li>
</ul>
<h3 id="最坏的情况">最坏的情况</h3>
<p>以上预测都是基于病毒的传染力不会增强、抗体始终存在且有效的情况。实际上，随着疾病的蔓延，毒力较强，传播能力较弱的病毒会自然的减少，留下的是传播能力强但毒力弱的毒株。R<sub>0</sub>的估值还会有改变。与此同时，E值也不一定为1，随着病毒的变异和人类抗体的减少，二次感染的概率也会变大。当(1-1/R<sub>0</sub>)&gt;E 时，群体免疫永远也不会实现。</p>
<h3 id="我们能做什么？">我们能做什么？</h3>
<p>群体面对的情况是危急的，作为个人，依然可以做很多事来保证自己的安全。</p>
<ul>
<li>戴口罩，口罩能有效降低病毒的呼吸道传播概率</li>
<li>不参加集会，少去人多的地方，对于自身来说，即降低了R<sub>0</sub>的值</li>
<li>保证营养的饮食和充足的睡眠，自身免疫力的提高才是战胜病毒的根本之法</li>
</ul>
<h2 id="reference">Reference:</h2>
<p>[1] <a href="https://metro.co.uk/2020/03/12/many-families-will-lose-loved-ones-time-coronavirus-says-pm-12390071/">https://metro.co.uk/2020/03/12/many-families-will-lose-loved-ones-time-coronavirus-says-pm-12390071/</a><br>
[2] Fine, P.; Eames, K.; Heymann, D. L. (1 April 2011). <a href="http://cid.oxfordjournals.org/content/52/7/911.full">“‘Herd immunity’: A rough guide”</a>. <em>Clinical Infectious Diseases</em>. <strong>52</strong> (7): 911–16.<br>
[3] <a href="https://www.bilibili.com/video/av87896793">https://www.bilibili.com/video/av87896793</a><br>
[4] Fine, P., Eames, K., &amp; Heymann, D. L. (2011). “Herd immunity”: A rough guide. <em>Clinical Infectious Diseases</em>, <em>52</em>(7), 911–916.<br>
[5] Wu, Joseph T.; Leung, Kathy; Leung, Gabriel M. <a href="https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(20)30260-9/fulltext">Nowcasting and forecasting the potential domestic and international spread of the 2019-nCoV outbreak originating in Wuhan, China: a modelling study</a>. The Lancet. 2020-01-31</p>

