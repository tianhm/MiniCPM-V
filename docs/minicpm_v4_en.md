## MiniCPM-V 4.0

> Archieve at: 2026-05-09

**MiniCPM-V 4.0** is an efficient model in the MiniCPM-V series. The model is built based on SigLIP2-400M and MiniCPM4-3B with a total of 4.1B parameters. It inherits the strong single-image, multi-image and video understanding performance of MiniCPM-V 2.6 with largely improved efficiency. Notable features of MiniCPM-V 4.0 include:

- 🔥 **Leading Visual Capability.**
   With only 4.1B parameters, MiniCPM-V 4.0 achieves an average score of 69.0 on OpenCompass, a comprehensive evaluation of 8 popular benchmarks, **outperforming GPT-4.1-mini-20250414, MiniCPM-V 2.6 (8.1B params, OpenCompass 65.2) and Qwen2.5-VL-3B-Instruct (3.8B params, OpenCompass 64.5)**. It also shows good performance in multi-image understanding and video understanding.

- 🚀 **Superior Efficiency.**
  Designed for on-device deployment, MiniCPM-V 4.0 runs smoothly on end devices. For example, it delivers **less than 2s first token delay and more than 17 token/s decoding on iPhone 16 Pro Max**, without heating problems. It also shows superior throughput under concurrent requests.

-  💫  **Easy Usage.**
  MiniCPM-V 4.0 can be easily used in various ways including **llama.cpp, Ollama, vLLM, SGLang, LLaMA-Factory and local web demo** etc. We also open-source iOS App that can run on iPhone and iPad. Get started easily with our well-structured [Cookbook](https://github.com/OpenSQZ/MiniCPM-V-CookBook), featuring detailed instructions and practical examples.


<details>
<summary> Click to view evaluation results and examples of MiniCPM-V 4.0. </summary>

### Evaluation  <!-- omit in toc -->

<details>
<summary>Click to view single image results on OpenCompass. </summary>
<div align="center">
<table style="margin: 0px auto;">
    <thead>
        <tr>
            <th nowrap="nowrap" align="left">model</th>
            <th nowrap="nowrap">Size</th>
            <th nowrap="nowrap">Opencompass</th>
            <th nowrap="nowrap">OCRBench</th>
            <th nowrap="nowrap">MathVista</th>
            <th nowrap="nowrap">HallusionBench</th>
            <th nowrap="nowrap">MMMU</th>
            <th nowrap="nowrap">MMVet</th>
            <th nowrap="nowrap">MMBench V1.1</th>
            <th nowrap="nowrap">MMStar</th>
            <th nowrap="nowrap">AI2D</th>
        </tr>
    </thead>
    <tbody align="center">
        <tr>
            <td colspan="11" align="left"><strong>Proprietary</strong></td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">GPT-4v-20240409</td>
            <td align="center">-</td>
            <td align="center">63.5</td>
            <td align="center">656</td>
            <td align="center">55.2</td>
            <td align="center">43.9</td>
            <td align="center">61.7</td>
            <td align="center">67.5</td>
            <td align="center">79.8</td>
            <td align="center">56.0</td>
            <td align="center">78.6</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">Gemini-1.5-Pro</td>
            <td align="center">-</td>
            <td align="center">64.5</td>
            <td align="center">754</td>
            <td align="center">58.3</td>
            <td align="center">45.6</td>
            <td align="center">60.6</td>
            <td align="center">64.0</td>
            <td align="center">73.9</td>
            <td align="center">59.1</td>
            <td align="center">79.1</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">GPT-4.1-mini-20250414</td>
            <td align="center">-</td>
            <td align="center">68.9</td>
            <td align="center">840</td>
            <td align="center">70.9</td>
            <td align="center">49.3</td>
            <td align="center">55.0</td>
            <td align="center">74.3</td>
            <td align="center">80.9</td>
            <td align="center">60.9</td>
            <td align="center">76.0</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">Claude 3.5 Sonnet-20241022</td>
            <td align="center">-</td>
            <td align="center">70.6</td>
            <td align="center">798</td>
            <td align="center">65.3</td>
            <td align="center">55.5</td>
            <td align="center">66.4</td>
            <td align="center">70.1</td>
            <td align="center">81.7</td>
            <td align="center">65.1</td>
            <td align="center">81.2</td>
        </tr>
        <tr>
            <td colspan="11" align="left"><strong>Open-source</strong></td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">Qwen2.5-VL-3B-Instruct</td>
            <td align="center">3.8B</td>
            <td align="center">64.5</td>
            <td align="center">828</td>
            <td align="center">61.2</td>
            <td align="center">46.6</td>
            <td align="center">51.2</td>
            <td align="center">60.0</td>
            <td align="center">76.8</td>
            <td align="center">56.3</td>
            <td align="center">81.4</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">InternVL2.5-4B</td>
            <td align="center">3.7B</td>
            <td align="center">65.1</td>
            <td align="center">820</td>
            <td align="center">60.8</td>
            <td align="center">46.6</td>
            <td align="center">51.8</td>
            <td align="center">61.5</td>
            <td align="center">78.2</td>
            <td align="center">58.7</td>
            <td align="center">81.4</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">Qwen2.5-VL-7B-Instruct</td>
            <td align="center">8.3B</td>
            <td align="center">70.9</td>
            <td align="center">888</td>
            <td align="center">68.1</td>
            <td align="center">51.9</td>
            <td align="center">58.0</td>
            <td align="center">69.7</td>
            <td align="center">82.2</td>
            <td align="center">64.1</td>
            <td align="center">84.3</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">InternVL2.5-8B</td>
            <td align="center">8.1B</td>
            <td align="center">68.1</td>
            <td align="center">821</td>
            <td align="center">64.5</td>
            <td align="center">49.0</td>
            <td align="center">56.2</td>
            <td align="center">62.8</td>
            <td align="center">82.5</td>
            <td align="center">63.2</td>
            <td align="center">84.6</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">MiniCPM-V-2.6</td>
            <td align="center">8.1B</td>
            <td align="center">65.2</td>
            <td align="center">852</td>
            <td align="center">60.8</td>
            <td align="center">48.1</td>
            <td align="center">49.8</td>
            <td align="center">60.0</td>
            <td align="center">78.0</td>
            <td align="center">57.5</td>
            <td align="center">82.1</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">MiniCPM-o-2.6</td>
            <td align="center">8.7B</td>
            <td align="center">70.2</td>
            <td align="center">889</td>
            <td align="center">73.3</td>
            <td align="center">51.1</td>
            <td align="center">50.9</td>
            <td align="center">67.2</td>
            <td align="center">80.6</td>
            <td align="center">63.3</td>
            <td align="center">86.1</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">MiniCPM-V-4.0</td>
            <td align="center">4.1B</td>
            <td align="center">69.0</td>
            <td align="center">894</td>
            <td align="center">66.9</td>
            <td align="center">50.8</td>
            <td align="center">51.2</td>
            <td align="center">68.0</td>
            <td align="center">79.7</td>
            <td align="center">62.8</td>
            <td align="center">82.9</td>
        </tr>
    </tbody>
</table>
</div>

</details>

<details>
<summary>Click to view single image results on ChartQA, MME, RealWorldQA, TextVQA, DocVQA, MathVision, DynaMath, WeMath, Object HalBench and MM Halbench. </summary>

<div align="center">
<table style="margin: 0px auto;">
    <thead>
        <tr>
            <th nowrap="nowrap" align="left">model</th>
            <th nowrap="nowrap">Size</th>
            <th nowrap="nowrap">ChartQA</th>
            <th nowrap="nowrap">MME</th>
            <th nowrap="nowrap">RealWorldQA</th>
            <th nowrap="nowrap">TextVQA</th>
            <th nowrap="nowrap">DocVQA</th>
            <th nowrap="nowrap">MathVision</th>
            <th nowrap="nowrap">DynaMath</th>
            <th nowrap="nowrap">WeMath</th>
            <th nowrap="nowrap" colspan="2">Obj Hal</th>
            <th nowrap="nowrap" colspan="2">MM Hal</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center"></td>
            <td align="center"></td>
            <td align="center"></td>
            <td align="center"></td>
            <td align="center"></td>
            <td align="center"></td>
            <td align="center"></td>
            <td align="center"></td>
            <td align="center"></td>
            <td align="center"></td>
            <td align="center">CHAIRs↓</td>
            <td align="center">CHAIRi↓</td>
            <td nowrap="nowrap" align="center">score avg@3↑</td>
            <td nowrap="nowrap" align="center">hall rate avg@3↓</td>
        </tr>
        <tbody align="center">
        <tr>
            <td colspan="14" align="left"><strong>Proprietary</strong></td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">GPT-4v-20240409</td>
            <td align="center">-</td>
            <td align="center">78.5</td>
            <td align="center">1927</td>
            <td align="center">61.4</td>
            <td align="center">78.0</td>
            <td align="center">88.4</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">Gemini-1.5-Pro</td>
            <td align="center">-</td>
            <td align="center">87.2</td>
            <td align="center">-</td>
            <td align="center">67.5</td>
            <td align="center">78.8</td>
            <td align="center">93.1</td>
            <td align="center">41.0</td>
            <td align="center">31.5</td>
            <td align="center">50.5</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">GPT-4.1-mini-20250414</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">45.3</td>
            <td align="center">47.7</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">Claude 3.5 Sonnet-20241022</td>
            <td align="center">-</td>
            <td align="center">90.8</td>
            <td align="center">-</td>
            <td align="center">60.1</td>
            <td align="center">74.1</td>
            <td align="center">95.2</td>
            <td align="center">35.6</td>
            <td align="center">35.7</td>
            <td align="center">44.0</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">-</td>
        </tr>
        <tr>
            <td colspan="14" align="left"><strong>Open-source</strong></td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">Qwen2.5-VL-3B-Instruct</td>
            <td align="center">3.8B</td>
            <td align="center">84.0</td>
            <td align="center">2157</td>
            <td align="center">65.4</td>
            <td align="center">79.3</td>
            <td align="center">93.9</td>
            <td align="center">21.9</td>
            <td align="center">13.2</td>
            <td align="center">22.9</td>
            <td align="center">18.3</td>
            <td align="center">10.8</td>
            <td align="center">3.9 </td>
            <td align="center">33.3 </td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">InternVL2.5-4B</td>
            <td align="center">3.7B</td>
            <td align="center">84.0</td>
            <td align="center">2338</td>
            <td align="center">64.3</td>
            <td align="center">76.8</td>
            <td align="center">91.6</td>
            <td align="center">18.4</td>
            <td align="center">15.2</td>
            <td align="center">21.2</td>
            <td align="center">13.7</td>
            <td align="center">8.7</td>
            <td align="center">3.2 </td>
            <td align="center">46.5 </td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">Qwen2.5-VL-7B-Instruct</td>
            <td align="center">8.3B</td>
            <td align="center">87.3</td>
            <td align="center">2347</td>
            <td align="center">68.5</td>
            <td align="center">84.9</td>
            <td align="center">95.7</td>
            <td align="center">25.4</td>
            <td align="center">21.8</td>
            <td align="center">36.2</td>
            <td align="center">13.3</td>
            <td align="center">7.9</td>
            <td align="center">4.1 </td>
            <td align="center">31.6 </td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">InternVL2.5-8B</td>
            <td align="center">8.1B</td>
            <td align="center">84.8</td>
            <td align="center">2344</td>
            <td align="center">70.1</td>
            <td align="center">79.1</td>
            <td align="center">93.0</td>
            <td align="center">17.0</td>
            <td align="center">9.4</td>
            <td align="center">23.5</td>
            <td align="center">18.3</td>
            <td align="center">11.6</td>
            <td align="center">3.6 </td>
            <td align="center">37.2</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">MiniCPM-V-2.6</td>
            <td align="center">8.1B</td>
            <td align="center">79.4</td>
            <td align="center">2348</td>
            <td align="center">65.0</td>
            <td align="center">80.1</td>
            <td align="center">90.8</td>
            <td align="center">17.5</td>
            <td align="center">9.0</td>
            <td align="center">20.4</td>
            <td align="center">7.3</td>
            <td align="center">4.7</td>
            <td align="center">4.0 </td>
            <td align="center">29.9 </td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">MiniCPM-o-2.6</td>
            <td align="center">8.7B</td>
            <td align="center">86.9</td>
            <td align="center">2372</td>
            <td align="center">68.1</td>
            <td align="center">82.0</td>
            <td align="center">93.5</td>
            <td align="center">21.7</td>
            <td align="center">10.4</td>
            <td align="center">25.2</td>
            <td align="center">6.3</td>
            <td align="center">3.4</td>
            <td align="center">4.1 </td>
            <td align="center">31.3 </td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">MiniCPM-V-4.0</td>
            <td align="center">4.1B</td>
            <td align="center">84.4</td>
            <td align="center">2298</td>
            <td align="center">68.5</td>
            <td align="center">80.8</td>
            <td align="center">92.9</td>
            <td align="center">20.7</td>
            <td align="center">14.2</td>
            <td align="center">32.7</td>
            <td align="center">6.3</td>
            <td align="center">3.5</td>
            <td align="center">4.1 </td>
            <td align="center">29.2 </td>
        </tr>
    </tbody>
</table>
</div>

</details>

<details>
<summary>Click to view multi-image and video understanding results on Mantis, Blink and Video-MME. </summary>
<div align="center">
<table style="margin: 0px auto;">
    <thead>
        <tr>
            <th nowrap="nowrap" align="left">model</th>
            <th nowrap="nowrap">Size</th>
            <th nowrap="nowrap">Mantis</th>
            <th nowrap="nowrap">Blink</th>
            <th nowrap="nowrap" colspan="2" >Video-MME</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center"></td>
            <td align="center"></td>
            <td align="center"></td>
            <td align="center"></td>
            <td align="center">wo subs</td>
            <td align="center">w subs</td>
        </tr>
        <tbody align="center">
        <tr>
            <td colspan="6" align="left"><strong>Proprietary</strong></td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">GPT-4v-20240409</td>
            <td align="center">-</td>
            <td align="center">62.7</td>
            <td align="center">54.6</td>
            <td align="center">59.9</td>
            <td align="center">63.3</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">Gemini-1.5-Pro</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">59.1</td>
            <td align="center">75.0</td>
            <td align="center">81.3</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">GPT-4o-20240513</td>
            <td align="center">-</td>
            <td align="center">-</td>
            <td align="center">68.0</td>
            <td align="center">71.9</td>
            <td align="center">77.2</td>
        </tr>
        <tr>
            <td colspan="6" align="left"><strong>Open-source</strong></td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">Qwen2.5-VL-3B-Instruct</td>
            <td align="center">3.8B</td>
            <td align="center">-</td>
            <td align="center">47.6</td>
            <td align="center">61.5</td>
            <td align="center">67.6</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">InternVL2.5-4B</td>
            <td align="center">3.7B</td>
            <td align="center">62.7</td>
            <td align="center">50.8</td>
            <td align="center">62.3</td>
            <td align="center">63.6</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">Qwen2.5-VL-7B-Instruct</td>
            <td align="center">8.3B</td>
            <td align="center">-</td>
            <td align="center">56.4</td>
            <td align="center">65.1</td>
            <td align="center">71.6</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">InternVL2.5-8B</td>
            <td align="center">8.1B</td>
            <td align="center">67.7</td>
            <td align="center">54.8</td>
            <td align="center">64.2</td>
            <td align="center">66.9</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">MiniCPM-V-2.6</td>
            <td align="center">8.1B</td>
            <td align="center">69.1</td>
            <td align="center">53.0</td>
            <td align="center">60.9</td>
            <td align="center">63.6</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">MiniCPM-o-2.6</td>
            <td align="center">8.7B</td>
            <td align="center">71.9</td>
            <td align="center">56.7</td>
            <td align="center">63.9</td>
            <td align="center">69.6</td>
        </tr>
        <tr>
            <td nowrap="nowrap" align="left">MiniCPM-V-4.0</td>
            <td align="center">4.1B</td>
            <td align="center">71.4</td>
            <td align="center">54.0</td>
            <td align="center">61.2</td>
            <td align="center">65.8</td>
        </tr>
    </tbody>
</table>
</div>

</details>

### Examples <!-- omit in toc -->

<div style="display: flex; flex-direction: column; align-items: center;">
  <img src="../assets/minicpmv4/minicpm-v-4-case.png" alt="math" style="margin-bottom: 5px;">
</div>

We deploy MiniCPM-V 4.0 on iPhone 16 Pro Max with [iOS demo](https://github.com/OpenSQZ/MiniCPM-V-CookBook/blob/main/demo/ios_demo/ios.md). The demo video is the raw screen recording without edition.

<table align="center"> 
    <p align="center">
      <img src="../assets/minicpmv4/iphone_en.gif" width=45%/>
      &nbsp;&nbsp;&nbsp;&nbsp;
      <img src="../assets/minicpmv4/iphone_en_information_extraction.gif" width=45%/>
    </p>
    <p align="center">
      <img src="../assets/minicpmv4/iphone_cn.gif" width=45%/>
      &nbsp;&nbsp;&nbsp;&nbsp;
      <img src="../assets/minicpmv4/iphone_cn_funny_points.gif" width=45%/>
    </p>
</table> 


</details>
