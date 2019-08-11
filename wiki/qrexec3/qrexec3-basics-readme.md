Diagram created with mermaidjs using the web app at https://mermaidjs.github.io/mermaid-live-editor/.

To generate the diagram, use the following code:

```
graph LR
    subgraph someVM
    A[qrexec-agent]
    end
    subgraph dom0
    C[qrexec-client]
    B[qrexec-daemon]
    C -->|initial request| B
    B -->|relayed request| A
    B -. vchan details .-> C
    B -. vchan details .-> A
    end
    C -->|established vchan channel| A
```
