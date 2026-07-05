This first paragraph will be removed.  This document is a short first iteration of an action plan.  The audience is the internal team of MDs, database drivers, and assorted managers on the data side of the house. The objectives are (1) marshal the group to actually start, rather than just trading emails (2) to build trust with the MDs and (3) make data managers allocate resources to get this done.  Retain the outline as defined by the markdown headers.  You may add headers if you wish.

## Problem definition 
With the strong correlation of cardiovascular health to an increased likelihood of cognitive impairment, a cardiologist will, at each patient encounter, look for any indicators of impairment, assess the likelihood of near-future impairment, and recommend one of:
- No immediate action
- Cardiology follow-up with cognitive concern documented
- Communication to the patient's PCP (with or without specific recommendations)
- Referral to neurology, geriatrics, psychiatry, or a memory clinic (again, with or without specific recommendations)

At that point, the next physician (in whatever discipline) can proceed with additional diagnostic tests:
- Cognitive screening: MiniCog, GPCOG, MoCA, MMSE, ...
- blood biomarker, APOE, ...
- MRI, PET, CSF,  ... 

And/or proceed with intervention:
- specific monitoring regime
- general health improvement preventative measures 
- cognition-targeted non-drug intervention
- drug intervention

## Intuition 
The specific intuition driving this effort is that unstructured free-text data in the longitudinal EHR up to the point of a cardio encounter is (1) an indicator of current, undiagnosed cognitive impairment and (2) future cognitive impairment.  And therefore, a scoring model that uses this unstructured text will help the cardiologist to shape the current encounter and then recommend next steps.

## Applying the intuition
In this workflow, we see three potential points for injecting AI/ML on the EHR (and its unstructured text):
1. Risk scoring *prior* to the cardiology encounter. From this, the physician (or a next model) determines the course of the encounter.  The specific target remains an open question; we expect to close with MD collaboration.    
    - Given the patient's EHR, what is the current probability of unmet cognitive care need?  
    - Given the patient's EHR, what is the likelihood of future cognitive impairment? We have a causal problem here that will complicate modeling and labeling (and steer lit review).   
1. Sequential diagnosis and evaluation *during* the cardiology encounter.  Given the EHR-derived risk score, what evaluations should the physician do during the encounter? How should the physician proceed given information revealed during the encounter?
1. Subsequent policy scoring *after* the encounter. Once no new information is collected in the encounter, and continuing the idea of sequential diagnosis, the point is to quantify the value and burden (however determined) of each possible next action to assist the final recommendation for next steps.
 
Our present focus is only on the first possible injection point - the risk scoring prior to the cardiology encounter. Our model predicts on a single cardiology encounter (meaning a model can be applied to a single patient over multiple encounters).  This bounds the scope to a learned diagnostic tool.  We are specifically not diving into within-encounter assistance, and we are not looking to develop a model that scores or recommends follow-up action.

This means our model inputs include all data up to the start of the cardiac encounter.  Inputs do not include data collected within the encounter, and they do not include data collected after the encounter.  

That said, training and evaluating the models are a function of labels we apply to patient records, and those labels are highly dependent on downstream action.  As an example, for two equivalent patients, if one is referred to neurology and one sent home with no further action, the neurology referral is more likely to receive a diagnosis of cognitive impairment.  In building the risk model, we need it to yield a risk score solely that is a function of the EHR, not one that is implicitly biased because of later decisions.  So again, while we're building a model that consumes only the EHR prior the encounter, development of that model requires a full understanding of the full patient record and the decision space from the cardiology encounter and onward.

## Anticipated contribution
We expect two contributions from this effort:
1. Dementia risk models.  We expect to extend the state of the art with the use of unstructured text from EHRs as predictors in detection models. This will be through a new application of existing AI/ML technology; we are not looking to extend core algorithms themselves. We'll sharpen our targeted contribution with the literature review, but at this point we tentatively see possible contribution through some combination of:
    - Methods for developing historical training and evaluation populations.  In particular, we're looking to specifically build labels that account for downstream action. 
    - A novel application of extant natural language processing models or encodings.
    - LLM augmentation. This includes domain-specific plain-text context, agent harnesses, or neural net augmentation to extend commercially available LLMs. 
2. Data transformation code. Like a large fraction of US hospitals, Inova uses Epic. The immediate study is predicated on extraction of patient records into model-ready formats. But practical benefit requires reproducibility across hospital systems.  Therefore, the translation from Epic into the models needs to be reproducible itself.  The ideal translation path is from Epic into a general cross-platform format (OMOP as an/the example target) and then to study-specific format.  Determination of an appropriate path will be a subject of literature review.

## Literature review
### Risk score
For the risk estimation problem, we're targeting a review of
- Longitudinal EHR representation
- Study population definition 
- Alzheimer disease and dementia diagnosis/prediction
- Unstructured text -> prediction model (within and outside the specific problem of cognitive impairment)

### Subsequent action policy
We consider the subsequent action space only in terms of creating datasets and accounting for bias and possibly including causal mechanisms in the risk model. If we were looking at developing the policies for selecting between the various actions, the literature would expand to 
- Sequential diagnosis
- Cost-sensitive and test-time feature acquisition
- Dynamic treatment regimes and policy learning

