

# Description

Example MATLAB code to perform the estimation and demodulation of field map contributions in magnetic resonance water&#x2013;fat imaging from the article

*Diefenbach, M. N., Ruschke, S., Eggers, H., Meineke, J., Rummeny, E. J., & Karampinos, D. C., Improving chemical shift encoding-based water-fat separation based on a detailed consideration of magnetic field contributions, Magnetic Resonance in Medicine, 80(3), 990–1004 (2018).*  <http://dx.doi.org/10.1002/mrm.27097>

    @article{diefenbach18_improv_chemic_shift_encod_based,
      author =       {Maximilian N. Diefenbach and Stefan Ruschke and Holger Eggers and Jakob Meineke and Ernst J. Rummeny
                      and Dimitrios C. Karampinos},
      title =        {Improving Chemical Shift Encoding-Based Water-Fat Separation Based on a Detailed Consideration of
                      Magnetic Field Contributions},
      journal =      {Magnetic Resonance in Medicine},
      volume =       80,
      number =       3,
      pages =        {990-1004},
      year =         2018,
      doi =          {10.1002/mrm.27097},
      url =          {https://doi.org/10.1002/mrm.27097},
    }


# Repository Overview

-   `demo.m`: Example script comparing water&#x2013;fat separation w/ and w/o demodulation of estimated field contributions.
-   `utils/`:
    -   `get_magnetInhomogeneities_Hz.m`: estimate inhomogeneities of the main magnetic field
    -   `get_shimField_Hz.m`: compute the shim field
    -   `get_objectBasedFieldmap_Hz.m`: estimate the object-based fast field map estimate from the article 
        *Sharma, S. D., Artz, N. S., Hernando, D., Horng, D. E., & Reeder, S. B., Improving chemical shift encoded water-fat separation using object-based information of the magnetic field inhomogeneity, Magnetic Resonance in Medicine, 73(2), 597–604 (2014).*  <http://dx.doi.org/10.1002/mrm.25163>
    -   `get_residualLinearField_Hz.m`: estimate a residual linear field
-   `20151101_151725_0302_ImDataParams.mat`: example data set of the cervical region
-   `fwtoolbox_v1_code/`: excerpt from the ISMRM water&#x2013;fat toolbox (version 1) containing MATLAB implementations of the graph cut water&#x2013;fat separation algorithm (*Hernando, D., Kellman, P., Haldar, J. P., & Liang, Z., Robust water/fat separation in the presence of large field inhomogeneities using a graph cut algorithm, Magnetic Resonance in Medicine, 63(1),  (2009).*  <http://dx.doi.org/10.1002/mrm.22177>) and the hierachical IDEAL algorithm (*Tsao, J., & Jiang, Y., Hierarchical ideal: fast, robust, and multiresolution separation of multiple chemical species from multiple echo times, Magnetic Resonance in Medicine, 70(1), 155–159 (2012).*  <http://dx.doi.org/10.1002/mrm.24441>).
    Full toolbox available here: <http://www.ismrm.org/workshops/FatWater12/data.htm>


# Example Result

Output from the script `demo.m`:

-   water&#x2013;fat separation **without** demodulation of estimated field contributions
    ![img](./stdWFI.png)
-   water&#x2013;fat separation **with** demodulation of estimated field contributions
    ![img](./proposedWFI.png)
-   sequential demodulation of estimated field contributions
    ![img](./field_contributions.png)


# License

MIT License

Copyright (c) 2017 Maximilian N. Diefenbach

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

