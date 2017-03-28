# SiRCub 1.3

**SiRCub** stands for *Sistema de Reconhecimento de Culturas brasileiro* (Brazilian Agricultural Crop Recognition System).
It allows to create agricultural crop classifiers and to test them.

## Prerequisites

* MySQL (ver. 5.6.21 or newer): recommended XAMPP, https://www.apachefriends.org/index.html
* Libsvm (ver. 3.17 or newer): https://www.csie.ntu.edu.tw/~cjlin/libsvm/
* Libopf (ver. 2.1 or newer): http://www.ic.unicamp.br/~afalcao/libopf/
* Gnuplot: run `$ sudo apt-get install gnuplot`

## Installation

1. If you haven't done it before, install & initialize Git:

   ```bash
   $ sudo apt-get install git
   $ git config --global user.name "YOUR NAME"
   $ git config --global user.email "YOUR EMAIL ADDRESS"
   ```

2. Clone the repository:

   ```bash
   $ git clone https://github.com/jordi-ic-unicamp/sircub.git
   ```

3. Create a new database for SiRCub into your MySQL server.

4. Create SiRCub's tables in the database:

   Import [db/sircub2_STRUCTURE.sql](db/sircub2_STRUCTURE.sql) script into the database.

5. Run [sircub.sh](sircub.sh) script to launch the program:

   ```bash
   $ cd sircub
   $ chmod u+x sircub.sh
   $ sircub.sh
   ```

6. Open the *Configuration* window and set up the SiRCub parameters (see Figure 2).

## Format of Input Files

* Descriptor locations file

   ```
   latitude,longitude
   ...
   ```





* Annotation labels file

   ```
   id,name
   1,bean
   2,corn
   3,corn+pasture
   ...
   ```

   *Example*: [input/dataset1/annotation_labels_en.csv](input/dataset1/annotation_labels_en.csv)

* Annotations file

   ```
   latitude,longitude,year,first_season,second_season
   -13.593828,-57.950981,2009-2010,no_data,no_data
   -13.593828,-57.950981,2010-2011,soybean,cotton
   -13.593828,-57.950981,2011-2012,soybean,sunflower
   -13.593828,-57.950981,2012-2013,soybean,corn
   ...
   ```

## Screenshots

<p align="center">
<img src="https://raw.githubusercontent.com/jordi-ic-unicamp/sircub/master/fig/screenshots/main_menu.png" />
<br />
<i>Figure 1</i>. Main Menu of the SiRCub prototype.
</p>

---

<p align="center">
<img src="https://raw.githubusercontent.com/jordi-ic-unicamp/sircub/master/fig/screenshots/configuration.png" />
<br />
<i>Figure 2</i>. Configuration dialog of the prototype.
</p>

---

<p align="center">
<img src="https://raw.githubusercontent.com/jordi-ic-unicamp/sircub/master/fig/screenshots/import_descriptors.png" />
<br />
<i>Figure 3</i>. Import Descriptors input dialog.
</p>

---

<p align="center">
<img src="https://raw.githubusercontent.com/jordi-ic-unicamp/sircub/master/fig/screenshots/import_annotations.png" />
<br />
<i>Figure 4</i>. Import Annotations input dialog.
</p>

---

<p align="center">
<img src="https://raw.githubusercontent.com/jordi-ic-unicamp/sircub/master/fig/screenshots/new_experiment.png" />
<br />
<i>Figure 5</i>. Screenshot of the New Experiment input dialog.
</p>

---

<p align="center">
<img src="https://raw.githubusercontent.com/jordi-ic-unicamp/sircub/master/fig/screenshots/log_tab.png" />
<br />
<i>Figure 6</i>. Screenshot of <i>experiment3</i> log tab.
</p>

---

<p align="center">
<img src="https://raw.githubusercontent.com/jordi-ic-unicamp/sircub/master/fig/screenshots/results_tab.png" />
<br />
<i>Figure 7</i>. Screenshot showing the <i>experiment3</i> results page generated by the prototype.
We can see the 3 most frequent classes: <i>corn</i>, <i>cotton</i>, and <i>pearl millet</i>.
</p>

---

<p align="center">
<img src="https://raw.githubusercontent.com/jordi-ic-unicamp/sircub/master/fig/training_txt_scale_margins.png" />
<br />
<i>Figure 8</i>. Plot of the cross-validation accuracy contour for <i>round1</i> of <i>experiment3</i>.
</p>

---

<p align="center">
<img src="https://raw.githubusercontent.com/jordi-ic-unicamp/sircub/master/fig/screenshots/new_classification.png" />
<br />
<i>Figure 9</i>. Screenshot of the New Classification input dialog.
</p>

## Acknowledgements

Work partially financed by FAPESP 2012/25169-5 fellowship, FAPESP/Cepid in Computational Engineering and Sciences (2013/08293-7), the Microsoft Research FAPESP Virtual Institute (NavScales project), FAPESP-PRONEX (eScience project), INCT in Web Science, and individual grants from CNPq.

