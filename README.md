<h1 align="center">Clean WMC output</h1>

<p align="center">
  (deprecated by Remove Tract Outliers App) This service cleans the output from AFQ and WMA using AFQ's AFQ_removeFiberOutliers function. For more information on the inputs of this application, please read the documentation at the top of the function: https://github.com/yeatmanlab/AFQ/blob/master/functions/AFQ_removeFiberOutliers.m
</p>

<p align="center">
  <a href="https://github.com/brainlife/abcd-spec"><img src="https://img.shields.io/badge/ABCD_Spec-v1.1-green.svg" alt="ABCD Spec v1.1"></a>
  <a href="https://doi.org/10.25663/bl.app.11"><img src="https://img.shields.io/badge/Brainlife-bl.app.11-blue.svg" alt="Run on brainlife.io"></a>
  <a href="https://github.com/brainlife/app-AFQclean/blob/master/LICENSE"><img src="https://img.shields.io/badge/License-MIT-lightgrey.svg" alt="MIT license"></a>
</p>

> **This branch, `1.4`, is the deprecated brainlife.io App Clean WMC output** ([doi:10.25663/bl.app.11](https://doi.org/10.25663/bl.app.11)). It is kept so earlier results stay reproducible. Use **Remove Tract Outliers** ([doi:10.25663/brainlife.app.157](https://doi.org/10.25663/brainlife.app.157)) instead.

## At a glance

<!-- brainlife-app:begin (generated from the App manifest; edit the manifest, not this block) -->

> **(deprecated by Remove Tract Outliers App) This service cleans the output from AFQ and WMA using AFQ's AFQ_removeFiberOutliers function. For more information on the inputs of this application, please read the documentation at the top of the function: https://github.com/yeatmanlab/AFQ/blob/master/functions/AFQ_removeFiberOutliers.m**

| | |
|---|---|
| **Inputs** | `neuro/wmc-deprecated` |
| **Outputs** | `neuro/wmc-deprecated` |
| **Container** | `brainlife/mcr:r2019a` |
| **Resources** | 1 CPUs · 28 GB memory · 3 h walltime |
| **Run it** | [doi.org/10.25663/bl.app.11](https://doi.org/10.25663/bl.app.11) |

#### Inputs

| Input | Datatype | Required | Description |
|---|---|---|---|
| `AFQ` | `neuro/wmc-deprecated` | yes |  |

#### Outputs

| Output | Datatype | Description |
|---|---|---|
| `output` | `neuro/wmc-deprecated` |  |

<details>
<summary><b>Parameters</b> (5)</summary>

| Parameter | Type | Default | Description |
|---|---|---|---|
| `maxiter` | integer | `5` |  |
| `numnodes` | integer | `100` |  |
| `maxlen` | integer | `4` |  |
| `maxdist` | integer | `4` |  |
| `M` | enum | `mean` | Select method for representing the center of the tract Options: `mean`, `median`. |

</details>

<!-- brainlife-app:end -->

## Running the App

### On brainlife.io

Open the App at [doi.org/10.25663/bl.app.11](https://doi.org/10.25663/bl.app.11), choose `neuro/wmc-deprecated` from your project, set the parameters and press **Execute**. The results are saved to your project as `neuro/wmc-deprecated`.

### Locally

You need [Singularity/Apptainer](https://apptainer.org/) (the App runs in `brainlife/mcr:r2019a`), [`jq`](https://jqlang.github.io/jq/).

1. Clone this repository.
2. Create `config.json` with the paths to your inputs and the parameters:

   ```json
   {
       "afq_fg": "/path/to/AFQ/afq_fg",
       "maxiter": 5,
       "numnodes": 100,
       "maxlen": 4,
       "maxdist": 4,
       "M": "mean"
   }
   ```

3. Run `./main`.

## Citing

If you use this App, please cite it, the software it builds on and brainlife.io:

- Clean WMC output. brainlife.io App. [doi:10.25663/bl.app.11](https://doi.org/10.25663/bl.app.11)
- Hayashi S, Caron BA, Heinsfeld AS, et al. brainlife.io: a decentralized and open-source cloud platform to support neuroscience research. *Nature Methods* 21:809–813 (2024). [doi:10.1038/s41592-024-02237-2](https://doi.org/10.1038/s41592-024-02237-2)
- Avesani P, McPherson B, Hayashi S, et al. The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services. *Scientific Data* 6:69 (2019). [doi:10.1038/s41597-019-0073-y](https://doi.org/10.1038/s41597-019-0073-y)

## Authors

brainlife.io team

## Funding

[![Wellcome-226486/Z/22/Z](https://img.shields.io/badge/Wellcome-226486%2FZ%2F22%2FZ-purple.svg)](https://wellcome.org/)
[![NIH-NINDS-U24NS140384](https://img.shields.io/badge/NIH_NINDS-U24NS140384-green.svg)](https://reporter.nih.gov/project-details/11261037)
[![NIH-NINDS-UM1NS132207](https://img.shields.io/badge/NIH_NINDS-UM1NS132207-green.svg)](https://reporter.nih.gov/project-details/11411328)
[![NIH-NIBIB-R01EB029272](https://img.shields.io/badge/NIH_NIBIB-R01EB029272-green.svg)](https://reporter.nih.gov/project-details/10262925)
[![NIH-NIBIB-R01EB030896](https://img.shields.io/badge/NIH_NIBIB-R01EB030896-green.svg)](https://reporter.nih.gov/project-details/10428625)
[![NIH-NIMH-R01MH126699](https://img.shields.io/badge/NIH_NIMH-R01MH126699-green.svg)](https://reporter.nih.gov/project-details/10460628)
[![NIH-NIDCD-R01DC020088](https://img.shields.io/badge/NIH_NIDCD-R01DC020088-green.svg)](https://reporter.nih.gov/project-details/11140284)
[![NSF-BCS-1734853](https://img.shields.io/badge/NSF_BCS-1734853-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1734853)
[![NSF-BCS-2203524](https://img.shields.io/badge/NSF_BCS-2203524-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2203524)
[![NSF-IIS-1636893](https://img.shields.io/badge/NSF_IIS-1636893-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1636893)
[![NSF-OAC-2148729](https://img.shields.io/badge/NSF_OAC-2148729-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2148729)
[![NSF-IIS-1912270](https://img.shields.io/badge/NSF_IIS-1912270-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1912270)
[![NSF-IIS-2148700](https://img.shields.io/badge/NSF_IIS-2148700-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2148700)
[![NSF-OAC-1916518](https://img.shields.io/badge/NSF_OAC-1916518-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1916518)

<sub>brainlife.io is publicly funded, and acknowledging that support helps keep it running. This App was developed with support from Wellcome, the U.S. National Institutes of Health (including the BRAIN Initiative BRAIN CONNECTS program: The Axonal Projectome EXchange, U24NS140384, and the Center for Mesoscale Connectomics, UM1NS132207) and the U.S. National Science Foundation.</sub>

## License

See [LICENSE](https://github.com/brainlife/app-AFQclean/blob/master/LICENSE).
