---
layout: post
title:  "How Gene Therapy Works"
categories: genes, DNA
---
# What is gene therapy?
The core idea behind gene therapy is to replace a defective gene with a functional gene.     
So, "gene therapy" is when DNA is used as the therapeutic. This is in contrast to most drugs, which use a small molecule, or a recombinant protein. The DNA (gene) used usually encodes a protein the patient needs.

# Core use cases for gene therapy
+ Genetic diseases where a single gene is mutated and needs to be fixed.
+ Some examples:
  * Severe combined immunodeficiency (SCID) - a rare genetic disorder characterized by nonfunctional T cells and B cells
  * Hemophilia - an inherited genetic disorder that compromises the ability to make blood clot
    * Deficiency of factor VIII or IX leads to poor clotting
    * Hemophilia is a good gene therapy target because (1) a small amount of factor VIII or IX is needed in blood and (2) a wide range of concentrations are tolerated.
  * Muscular Dystrophy - a genetic disorder that results in progressive muscle wasting
  * Cancer is becoming an increasingly interesting target for gene therapy.
+ The solution is generally to add the wild-type version of the gene to correct the mutation.

# The difficulty is in the details...

+ Delivery - how do you get these genes to the right cells in the body (liver, blood, brain)?
+ How do you ensure the body's immune system doesn't detect and reject the payload (the functional gene you're trying to introduce)?
+ How do you get the gene to express long term (so the patient is cured for life, rather than being dependent on repeat treatments)?
+ How do you make it safe? How do you reduce side effects?

Research in gene therapy began in the 1980s, and there has been incremental progress since then (several gene therapy trials over the years, with growing success).

+ 1999 - first death (Jesse Gelsinger at The University of Pennsylvania) from gene therapy. Rapid death from acute inflammatory response to adenovirus vector. This incident put a chill on the field because the scientists involved were seen as "cowboys" / rushing a process that required careful consideration.
+ 2002 - SCID success, by treating hematopoietic stem cells with retrovirus vectors


# The process of SCID gene therapy
1. Isolate bone marrow cells from patient
2. Culture cells in vitro and add cytokines to stimulate cell division
3. Infect with retroviruses carrying therapeutic gene
4. Infuse cells back into patient

# Modalities of gene delivery
*in vivo, ex vivo, viral vectors, nonviral vectors*

**In vivo** - direct delivery to the body

**Ex vivo** - deliver to cells, then transplant cells to the body    

+ Solid tissues typically don't accept grafts very well, so ex vivo techniques are typically used for blood disorders.

#### **Viral Vectors**

Viruses know how to deliver their DNA into a cell, scientists have co-opted the virus's machinery to deliver a gene of interest to a cell of interest. Different viruses have different payloads (size of gene they can deliver)  
Some examples: Adenovirus, herpes virus, retrovirus, lentivirus, adeno-associated virus (AAV).

+ Adenovirus (cold virus), capacity 30kb
+ Herpes virus
+ Retrovirus - RNA virus, capacity 8-10kb, Integrates randomly, needs dividing cells
+ Lentivirus - (HIV virus)
+ Adeno-associated virus (AAV) - Single-stranded DNA, small carrying capacity, ~4.7 kb, mostly unintegrated concatemer, <5% integrates randomly, many humans have pre-existing immunity to capsid.

**Pros of viral vectors**

+ Adenovirus has a carrying capacity of 30kb, large enough to carry any human gene (even multiple). Doesn't integrate with the genome (not good for dividing cells, but if the cells are not dividing, can be viewed as a safety feature)

**Cons of using viral vectors**

+ Capsid, the protein encasing the virus, inherently produces an immune / inflammatory response.  
+ Insertional mutagenesis hazard of random integration


#### **Nonviral Vectors**

Electroporation, lipids, nanoparticles, fluid pressure.  

+ Electroporation - electroporation is a physical method that is often used for cells in culture. The idea is to introduce a transient electrical charge that makes the cell membrane permeable (so the DNA can enter the cell) and the cell membrane heals following.  
+ Lipids - Combine DNA with lipids so that the complex can be taken up by cells
+ Nanoparticles - under development   
+ Fluid pressure -  use fluid pressure to get DNA in contact with and then taken up by cells   

**Pros of nonviral vectors**

+ Not immunogenic (doesn't elicit an immune response). Nonviral vectors "leave no trace", meaning no viral protein is introduced to the cell.
+ No size limit for the payload, since no viral vector is needed to introduce the payload to the body
+ Cheaper, since no vector needs to be engineered

## Gene Therapy Successes
*CAR-T, HIV, ADA-SCID*

# CAR-T

The most compelling success to date has been in chimeric antigen receptor in T-cells (CAR-T). (CARs) are synthetic receptors that reprogram T lymphocytes to target chosen antigens.
The idea here is to add a new antigen receptor in a patient's T-cells that recognizes cancer cells. These modified T-cells then go out and kill the tumor. There has been success in leukemia and other cancers. Most success in targeting CD19, a cell surface molecule expressed on most leukemias and lymphomas.
15-30% of patients experience severe side effects, toxicities, cytokine release syndrome
The focus now is on resolving toxicities and expanding reach to solid tumors.

Scientists are working to extend these ideas in solid tumors as well, it is an entire field of research to find a target on solid tumors that is not expressed on other cells as well. May work best in blood, cells in suspension.

# First two FDA approvals for CAR-T

+ Kymriah (Novartis) *Approved: August 30th 2017*    
  * Treats advanced acute lymphoblastic leukemia in children and young adults up to age 25  
  * Cost: $373,000 + costs of hospital services   
  * 15-30% will have complications, requiring up to months in the ICU

+ Yescarta (Kite-Gilead) *Approved: October 19th 2017*  
  * Treats non-Hodgkin lymphomas, age 60+  
  * 4% of all cancers in the USA, 72k new cases each year   
  * 51% of patients had complete remission   
  * Some percentage will have severe side effects  

# First approved gene therapy in Europe

+ Glybera
  * Treats a rare metabolic disorder lipoprotein lipase deficiency.
  * Cost: $1.2M USD per treatment
  * As of 2012, not seeking U.S. FDA approval, and pulled from Europe market after treating just one patient.

# First FDA approved gene therapy in the United States

+ Luxturna *Approved: December 19, 2017*
  * AAV gene therapy for retinitis pigmentosa RPE 65
  * Probable approval by January 12, 2018
  * Sustained benefit for >3 years, >90% patients had improved vision, but not normal vision
  * 1 – 2K patients in USA, 6K worldwide


# HIV

HIV infects cells through CCR5, a receptor on T-cells. Clinical trials have explored extracting a patients t-cells, using a  zinc finger nuclease (ZFN) to cut out the CCR5 receptor in the T-cells, purify, and reintroduce them into the patients body. This means the entire population isn't resistant, but at least a small population is, which has been shown to confer some resistance.

# ADA-SCID

ADA-SCID approved gene therapy product in Europe
and X-SCID (retrovirus and lentivirus vectors) dozens of patients improved or cured
Successes in blood disorders, namely beta thalassemia and sickle cell anemia  



2. T-VEC – herpesvirus vector for cancer, oncolytic immunotherapy, GM-CSF for tumor lysis and immunoreactivity, extends survival in melanoma (U.S. & Europe) 2015

3. Strimvelis – retrovirus for ADA-SCID, rare genetic disease, approved in Europe, May 2016, $648,000, 1 patient treated

# Roadblocks

+ The main problem is delivery

# Thanks

Credit for the good stuff goes to [Dr. Michele Calos](https://profiles.stanford.edu/michele-calos?tab=publications), mistakes are mine!
