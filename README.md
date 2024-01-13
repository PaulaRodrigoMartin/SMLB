```mermaid
graph TD;
    seqlist[seqs/hs.utr3.seqlist.rds]
    seqs[seqs/hs.utr3.seq.rds]
    mireact_input[data/xxxxxxx]
    miReact_output[log/data/mirnaActivity_th_downsampled.rds]
    7mers[patterns/patterns7.csv]
    annotation[data/annotation.csv]
    miReact[code/mireact.sh]
    rank[code/xxxxxxx]
    functions[code/functions.R]
    main_notebook[code/main.Rmd]
    GSEA[code/GSEA.Rmd]
    logos[results/logos.pdf]
    corrm[results/correlations.pdf]
    distrib[results/hit_distrib.pdf]
    ranked_seqs[data/ranked_kmers.rds]
    

    style seqlist fill:#7cb5ec,stroke:#333,stroke-width:2px;
    style miReact_output fill:#7cb5ec,stroke:#333,stroke-width:2px;
    style 7mers fill:#7cb5ec,stroke:#333,stroke-width:2px;
    style mireact_input fill:#7cb5ec,stroke:#333,stroke-width:2px;
    style seqs fill:#7cb5ec,stroke:#333,stroke-width:2px;
    style annotation fill:#7cb5ec,stroke:#333,stroke-width:2px;
    style logos fill:#7cb5ec,stroke:#333,stroke-width:2px;
    style corrm fill:#7cb5ec,stroke:#333,stroke-width:2px;
    style distrib fill:#7cb5ec,stroke:#333,stroke-width:2px;
    style ranked_seqs fill:#7cb5ec,stroke:#333,stroke-width:2px;

    seqlist-->miReact
    7mers-->miReact
    mireact_input-->miReact
    annotation-->miReact
    miReact-->miReact_output
    functions-->main_notebook
    main_notebook-->GSEA
    main_notebook-->logos
    main_notebook-->corrm
    main_notebook-->distrib
    seqs-->GSEA
    rank--> ranked_seqs
    miReact_output-->rank
    rank-->ranked_seqs
    ranked_seqs-->main_notebook

```
