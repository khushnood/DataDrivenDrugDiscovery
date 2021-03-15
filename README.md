# Help

Here is the pre-process data for application of link prediction in data driven drug discovery paper. We have uploaded the preprocessed datasets which is compatible to online available code with https://github.com/THUDM/cogdl. The partial online code can be found from https://github.com/THUDM/cogdl such as node2vec, Deepwalk etc. 
You can donload the code and register our datasets as follows. Further the datasets can be used by using data name such as DDI, DDA etc.


```bash


@register_dataset("ddi")
class DDI(EdgelistLabel):
    def __init__(self):
        dataset = "ChCh-Miner_durgbank-chem-chem_Processed"
        path = osp.join(osp.dirname(osp.realpath(__file__)), "../..", "data", dataset)
        super(DDI, self).__init__(path, dataset)

@register_dataset("matador")
class MATADOR(EdgelistLabel):
    def __init__(self):
        dataset = "ChemicalProteinNetworkMATADOORProcessed"
        path = osp.join(osp.dirname(osp.realpath(__file__)), "../..", "data", dataset)
        super(MATADOR, self).__init__(path, dataset)
@register_dataset("dti")
class DTI(EdgelistLabel):
    def __init__(self):
        dataset = "ChG-Miner_miner-chem-gene_Processed"
        path = osp.join(osp.dirname(osp.realpath(__file__)), "../..", "data", dataset)
        super(DTI, self).__init__(path, dataset)

@register_dataset("dda")
class DDA(EdgelistLabel):
    def __init__(self):
        dataset = "DCh-Miner_miner-disease-chemical_Processed"
        path = osp.join(osp.dirname(osp.realpath(__file__)), "../..", "data", dataset)
        super(DDA, self).__init__(path, dataset)
@register_dataset("dga")
class DGA(EdgelistLabel):
    def __init__(self):
        dataset = "DG-AssocMiner_miner-disease-gene_Processed"
        path = osp.join(osp.dirname(osp.realpath(__file__)), "../..", "data", dataset)
        super(DGA, self).__init__(path, dataset)
```
