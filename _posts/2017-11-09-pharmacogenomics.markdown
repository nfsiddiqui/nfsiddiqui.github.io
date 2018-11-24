---
layout: post
title:  "Pharmacogenomics"
categories: genes, DNA
---
# What is Pharmacogenomics?

+ Pharmaco*genetics* was coined in 1959, and focused on how a **single gene** affects how a patient responds to medication.   
+ Pharmaco*genomics* (PGx) began being used after the Human Genome Project emerged in 2000, and focuses on how **many genes** interacting affect how you respond to medication.  
+ Pharmacogenomics / pharmacogenetics are largely interchangeable terms.

Other factors that influence how you react to drugs/medication:

+ the environment (your diet, what conditions you are exposed to)
+ clinical factors (age, severity of disease)

# Precision Medicine and PGx

### The idea behind precision medicine and PGx is to select the **right dose** of the **right drug** for the **right patient** at the **right time**.

Right now, when a doctor prescribes a drug, there are many options to choose from, which one the doctor chooses is largely due to her experience in practice on which drugs were effective for her patient population in the past.  However, efficacy may vary widely and adverse affects are common and unpredictable. The doctor's drug choice is also influenced to some degree by pharmaceutical reps and how well they market their drugs to doctors. What drug the patient ends up using is a trial and error process, the doctor prescribes something, the patient tries it out for a certain amount of time, and if the side effects are too great or if the medication isn't effective, another prescription is given until the patients condition is being managed appropriately.

In the future, doctors will use genetics to guide drug and dose selection. "Patients with your genotype typically have a lower response", "patients with your genotype typically experienced a higher rate of adverse reactions", etc. Helps select more responsive patients.

# The drug pathway

#### **Pharmacokinetics** (PK): what your body does to the drug

  + absorbing, digesting, metabolizing, excreting (ADME)  
  + **A** bsorption - passive, active, or co-transport  
  + **D** istribution - fat or water soluble  
  + **M** etabolism - broken down or modified
    + oxidation, methylation, sulfation, acetylation, glucuronidation
  + **E** limination - renal excretion (to urine, liver excretion to bowel)  

*Genes that affect pharmacokinetics (PK):*  

+ metabolizing enzymes (CYPs, UGTs) and transporters - help the drug get in and out of the cell to where it is metabolized (ABCs, SLCs).

#### **Pharmacodynamics** (PD): what the drug does to the body
Target - the molecules in the cell that the drug targets for its effect (mechanism of action)

*Genes that affect pharmacodynamics (PD):*  

+ GPCRs, kinases, ion channels, immune molecules.

### Together, variation in the genes that affect PK and PD influence the efficacy and toxicity of a drug.


# The greatest hits in PGx

+ **Thiopurines** - alter dose or use alternate drug for poor metabolizers
+ **Clopidogrel** - use alternate drug for ultra rapid metabolizers
+ **Codeine** - alter dose or alternate drug for ultra rapid metabolizers
+ **Warfarin** - alter dose based on PK and PD genes
+ **Single allele PGx** - presence of one allele puts the patient at risk of adverse drug reactions
+ **Cancer PGx** - drug targets genetic changes in tumors, PK genes


# Thiopurines

[Thiopurines](https://www.nature.com/articles/nrc2292) are a class of drugs that are used to suppress the immune system (purine analogs, 6-mercaptopurine, 6-thioguanine, azathioprine). Thiopurines are used to treat leukemias, inflammatory bowel disease, and after transplant to immunosuppress the patient (prevent organ rejection).

+ Thiopurines interfere with nucleic acid synthesis, and in some cases results in very severe side effects (fatal in some cases - myelosuppression, blood cells are not produced in bone marrow as they should be)

The gene TPMT is one of the very first examples of pharmacogenetics being used in the clinic.
If you have the active form of TPMT, the drug gets incorporated into your DNA and has an effect.

<img src="/images/posts/metabolism-tpmt.png" height="auto" width="48%">

Azathioprine gets broken down into 6-MP.  

+ If you have TPMT, 6-MP gets converted into 6-methyl mercaptopurine, which is the **inactive** form of the drug.  

+ If you don't have TPMT, then most of the 6-MP gets converted into 6-thioguanine, which is the **active** form of the drug. (A small amount is converted into oxidized metabolites).  

Here, we can see that TMPT levels *drastically* affects thioguanine levels.  

+ If you have **more** TMPT
  + you have less thioguanines (you are deactivating most of the drug into 6-methyl mercaptopurine), and **less efficacy** against the disease.

+ If you have **less** TMPT
  + you have more thioguanines (you are converting too much azathioprine into thioguanine, the "average" dose given is actually resulting in twice the amount of medication being delivered), at high risk of severe bone marrow toxicity.



# Cytochrome P450s

[Cytochrome P450s](https://ghr.nlm.nih.gov/primer/genefamily/cytochromep450) are a gene family consisting of ~60 genes in humans. Each gene that is part of the cytochrome P450 family is named with "CYP". **Cytochrome P450 genes produce enzymes** (largely in the liver) that breakdown (metabolize) many molecules and chemicals. Cytochrome P450s are responsible for metabolizing a huge number of drugs.

#### CYP1, CYP2, CYP3 metabolize ~90 percent of drugs used today

Sometimes the drug that you take orally is taken in an "inactive" state, and needs to be metabolized to its active state. An individual's ability to metabolize a drug depends on the form of CYP enzyme produced by their liver. Most people have active CYP enzymes, when they take medication it is broken down efficiently and there is no build up of medication in the body (no risk of overdose). If you have deficient CYP, you are not breaking down the medication in your body (leading to toxicity), or the drug may never be converted to an active form (the medicine doesn't work).

| Normal Metabolizer   | Intermediate Metabolizer  |  Poor metabolizer   |  Ultra rapid metabolizer |
|---  |---  |---  |---  |
|100% enzyme function  |  50% enzyme function |  0% enzyme function  |   150% enzyme function |
| 0 variant alleles  |  1 variant allele | 2 variant alleles   |  3 variant alleles |  
| Active CYP enzyme  | Inactive CYP enzyme |  Inactive CYP enzyme | Overactive CYP enzyme  |
|  Medicine works!  | Drug toxicity  |   Drug toxicity | Drug toxicity  |


# Clopidogrel

[Clopidogrel](https://www.drugbank.ca/drugs/DB00758) (brand name is Plavix) is an anti platelet agent used to prevent blood clots. Prevents people who recently had a cornary event from having another one (by making their blood less sticky).

+ Response to clopidogrel is very variable (in 4-20% of people it doesn't work)!
+ This means those people are at risk of having another clot, which means they may have another coronary event

Clopidogrel is an example of a drug that has to be activated in the body (metabolized) in order become active.
Clopidogrel needs to be converted to an active metabolite by CYP2C19.

CYP2C19 is highly polymorphic.  
CYP2C19*2 is the most common variant that affects the response to this medication.

For poor metabolizers, this means they will have lower levels of the active metabolite, leading to decreased platelet inhibition and greater platelet aggregation, and a high risk for an adverse cardiovascular event. The FDA knows about this and issued a box warning in 2010 stating that the drug is not effective at preventing coronary events in poor metabolizers.

Tests are available for the CYP2C19 genotype, and can be used to inform therapeutic strategy (prescribe an alternative drug), but right now, it is not standard of care to be tested if you are a poor metabolizer.

# Codeine

Codeine is a commonly used opioid. Codeine isn't effective until it is metabolized into morphine, which provides the "pain killing" effect.
CYP2D6 is the gene that produces the metabolizing enzyme that transforms codeine into it's active form (morphine).
CYP2D6 alleles are complicated, highly polymorphic (at least 140 known alleles).
Depending on the variant of CYP2D6 that you have, you're categorized as a "Normal", "Intermediate", "Poor", or "Ultra rapid metabolizer".
If you're a "poor" metabolizer, the codeine isn't converted into morphine and you don't get any pain relief.

If you're an ultra-rapid metabolizer, the codeine can be converted into too much morphine (resulting in morphine toxicity). There was a case where a mother didn't know that she was an ultra-rapid metabolizer, took tylenol, and produced way too much morphine. This didn't kill her, because as an adult she has a higher tolerance, but it killed her infant because it was passed through to the breast milk.

Codeine is relatively accessible/inexpensive, was very commonly prescribed for a long time. Right now, The Academy of Pediatrics has decided it shouldn't be used in children at all because of the lethality to children who are ultra-rapid metabolizers, it has been banned for use in children. However, to geneticists this is seen as a loss, since it codeine can be safely prescribed to be patients, if a genetic test is administered beforehand verifying that the patient is not an ultra-rapid metabolizer.


<!-- # Warfarin
A few genes effect warfarin response: Cytochrome P450, also known as CYP2C9 (pronounced "sip 2C9"), VKORC1, CYP4F2.

Warfarin is a cheap, widely used anti coagulant, that has a narrow therapeutic index (hard to predict the correct final dose). If you have an overdose of warfarin you are at risk of bleeding events, however if your dose is too small, you are at risk of another coronary event (not )

If you have too much warfarin

originally used as a rat poison
INR - therapeutic range
beginning, dangerous, not in therapeutic range
other drugs on the market, more expensive, dont need to

# HLA alleles
HLA genes are part of the immune system.

If you have certain alleles, you never take certain medications because of severe reactions. For examples..

+ Allopurinol - HLA-B*58:01

+ Carbamazepine - HLA-B*15:02

+ Phenytoin - HLA-B*58:01

+ Abacavir - HLA-B*57:01

Different allele frequencies mean different warnings in different populations.

# Cancer PGx
Genetics of your tumor
Cetuximab
A lot of oncology examples

[PharmGKB](www.pharmgkb.org)
FDA biomarker list - drug labels

Identify variation in drug response, reduce adverse events in

# Challenges

+ difficulty in getting randomized control trials
+ the cost of genotyping (and whether on not this cost will be reimbursed by insurance companies)
+ the time delay introduced in getting a response by genotyping
+ clinical adoption - when this information about how genes interact with drugs will be integrated into routine into medical training, FDA drug labelling, publishing dosing guidelines -->



# Deep Learning for Pharmacogenomics -- Papers

+ [Molecular Graph Convolutions: Moving Beyond Fingerprints](https://arxiv.org/abs/1603.00856)

+ [AtomNet: A Deep Convolutional Neural Network for Bioactivity Prediction in Structure-based Drug Discovery](https://arxiv.org/abs/1510.02855)

+ [Convolutional LSTM Networks for Subcellular Localization of Proteins](https://arxiv.org/pdf/1503.01919.pdf)

+ [Protein contact map prediction using ultra deep residual nets](http://biorxiv.org/content/early/2016/09/06/073239)

+ [DeepTox: Toxicity Prediction using Deep Learning](https://www.frontiersin.org/articles/10.3389/fenvs.2015.00080/full)


## Thanks

Credit for the good stuff goes to [Anshul Kundaje](https://profiles.stanford.edu/anshul-kundaje) and [Dr. Michelle Whirl-Carrillo, PhD](https://profiles.stanford.edu/michelle-carrillo?tab=publications), mistakes are mine!   
