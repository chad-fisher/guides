# Computing Resources

The Tufts HPC Cluster is comprised of various type of CPU and GPU enabled compute nodes.  This table provides a 
general idea of what is currently available for use.

| Number  | Type         | CPU          | Memory  | GPU          |
|:--------|:-------------|:-------------|:--------|:-------------|
| 40      | CPU          | 2x 32 Cores  | 512GB   |              |
| 45      | CPU          | 2x 18 Cores  | 256GB+  |              |
| 2       | CPU          | 2x 18 Cores  | 1TB     |              |
| 8       | CPU          | 2x 24 Cores  | 756GB   |              |
| 8       | CPU          | 2x 32 Cores  | 256GB   |              |
| 5       | GPU          | 2x 16 Cores  | 756GB   | 8x a100-40G  |
| 5       | GPU          | 2x 32 Cores  | 1TB     | 8x a100-80G  |
| 20      | GPU          | 2x 20 Cores  | 92GB    | 4x t4        |
| 9       | GPU          | 2x 32 Cores  | 256GB   | 4x l40       |
| 25      | MIXED        | MIXED        | MIXED   | MIXED        |

Some systems are only available to all users on the preempt partition.

Mixed systems include a limited number of various GPUs including V100, A100, H100 and GH200.

```{gallery-grid}
:grid-columns: 1
:grid-rows: 16

- header: "{fas}`book;pst-color-primary` 01 Terminology Overview"
  content: "Understand the terminoloies used accross Tufts HPC cluster documentations"
  link: "../terminology.html"

- header: "{fas}`book;pst-color-primary` 02 HPC Partitions"
  content: "Partitions on Tufts HPC cluster and their purposes"
  link: "../Slurm/partition.html"

- header: "{fas}`book;pst-color-primary` 03 GPU Resources"
  content: "Available GPU resources on Tufts HPC cluster and how to request them"
  link: "GPU.html"

- header: "{fas}`book;pst-color-primary` 04 hpctools"
  content: "Utilize a command line tool - hpctools - to help you find available resource on Tufts HPC cluster"
  link: "../examples/hpctools.html"

```
