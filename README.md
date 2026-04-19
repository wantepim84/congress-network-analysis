<h1>Congress Network Analysis</h1>
<h3>Understanding Influence, Community Structure, and Network Robustness</h3>

<hr>

<h2>Overview</h2>

<p>
Many real-world systems are best understood as <strong>networks of relationships</strong> rather than isolated data points.
In political systems, interactions between actors form complex structures that shape influence, collaboration,
and information flow.
</p>

<p>
This project applies <strong>graph-based network analysis</strong> using Python and
<strong>NetworkX</strong> to study a Congressional interaction network,
focusing on identifying <strong>influential actors, community structure, and structural robustness</strong>.
</p>

<p>
While this project uses a political network, the same analytical approach applies to:
</p>

<ul>
  <li>Social and political networks</li>
  <li>Organizational structures</li>
  <li>Financial and fraud detection systems</li>
  <li>Recommendation and knowledge graphs</li>
  <li>Biological and molecular networks</li>
</ul>

<hr>

<h2>Problem Framing</h2>

<p>
Large relational networks often appear complex but follow consistent structural patterns:
</p>

<ul>
  <li>Influence is concentrated among a small number of nodes</li>
  <li>Connectivity depends on key bridging actors</li>
  <li>Groups naturally form into tightly connected communities</li>
</ul>

<p>
This project addresses four key questions:
</p>

<ol>
  <li>Which nodes are most influential in the network?</li>
  <li>Which nodes act as bridges between communities?</li>
  <li>How does the network partition into communities?</li>
  <li>How robust are these findings under different assumptions?</li>
</ol>

<hr>

<h2>Data</h2>

<ul>
  <li><strong>Dataset:</strong> Congressional interaction network</li>
  <li><strong>Nodes:</strong> Individual actors (e.g., members)</li>
  <li><strong>Edges:</strong> Interactions between actors</li>
  <li><strong>Graph type:</strong> Directed, weighted</li>
  <li><strong>Size:</strong> ~475 nodes, ~10,000 edges</li>
  <li><strong>Edge format:</strong> Weighted relationships stored as attributes</li>
</ul>

<p>
Edge weights represent the <strong>strength of interaction</strong> between nodes.
</p>

<hr>

<h2>Modelling Choices</h2>

<p>
The network is modelled with a focus on preserving meaningful structure:
</p>

<ul>
  <li>Directed graph to capture asymmetric relationships</li>
  <li>Weighted edges to reflect interaction strength</li>
  <li>Explicit parsing of edge attributes for correctness</li>
  <li>No temporal dynamics included (static snapshot)</li>
</ul>

<p>
These choices balance realism with interpretability.
</p>

<hr>

<h2>Analysis Approach</h2>

<p>
The analysis follows a structured pipeline:
</p>

<ul>
  <li><strong>Graph validation</strong> — ensuring correct structure and attributes</li>
  <li><strong>Degree analysis</strong> — identifying highly connected nodes</li>
  <li><strong>Centrality measures</strong> — quantifying influence (degree, betweenness, closeness, PageRank)</li>
  <li><strong>Community detection</strong> — identifying clusters using modularity-based methods</li>
  <li><strong>Bridge analysis</strong> — detecting nodes connecting multiple communities</li>
  <li><strong>Visualization</strong> — mapping structure and highlighting key nodes</li>
  <li><strong>Robustness testing</strong> — validating stability of findings</li>
</ul>

<p>
The focus is on <strong>interpretable metrics</strong> and <strong>reproducible insights</strong>.
</p>

<hr>

<h2>Key Findings (High-Level)</h2>

<ul>
  <li>A dominant hub node emerges consistently across all centrality measures</li>
  <li>The network partitions into <strong>4 stable communities</strong></li>
  <li>Community structure is highly robust (near-perfect stability across runs)</li>
  <li>A small number of nodes act as critical <strong>bridges between communities</strong></li>
  <li>Influence is partially consistent across metrics, indicating multiple forms of importance</li>
  <li>The network remains connected but shows sensitivity to removal of key nodes</li>
</ul>

<p>
These patterns suggest a structured and non-random system with concentrated influence and modular organization.
</p>

<hr>

<h2>Repository Structure</h2>

<pre>
congress-network-analysis/
│
├── README.md
├── data/
│   └── congress.edgelist.txt
│
├── src/
│   └── main.py
│
├── outputs/
│   ├── community_plot.png
│   └── bridge_plot.png

</pre>

<ul>
  <li><strong>Script:</strong> End-to-end analysis pipeline</li>
  <li><strong>Outputs:</strong> Visualizations of network structure</li>
</ul>

<hr>

<h2>Tools Used</h2>

<ul>
  <li>Python</li>
  <li>:contentReference[oaicite:0]{index=0}</li>
  <li>:contentReference[oaicite:1]{index=1}</li>
</ul>

<hr>

<h2>About</h2>

<p>
This project demonstrates how <strong>network science techniques</strong> can be applied to real-world relational data
to extract meaningful structural insights.
</p>

<p>
The emphasis is on building a clear, reproducible pipeline that moves from raw data
to interpretable conclusions about influence, structure, and robustness.
</p>

<hr>

<h2>Notes</h2>

<p>
This repository is intended as a <strong>demonstration of analytical approach and methodology</strong>,
rather than a production-ready system.
</p>

<p>
All modelling assumptions are made explicit to ensure clarity and reproducibility.
</p># congress-network-analysis
