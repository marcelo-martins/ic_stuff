Cycle 1
=======

Begin (start, presentation_3)
-------------
  ![Emergency room](theme/background-emergency-room-1.png)

@NURSE: Doctor, please, come to the emergency room. A man (52 years old reports he is feeling a very strong chest pain. His vital signs are ABP (right arm): 164x108mmHg; HR: 124bpm; RR: 23rpm; Temp: 36,1 o C; O 2 Sat: 96%.

@PATIENT: Doctor, I am feeling chest pain since yesterday. The pain is continuous and is located just in the middle of my chest, worsening when I breathe and when I lay down on my bed. I suffer from arterial hypertension and smoke 20 cigarettes every day. My father had a “heart attack” at my age and I am very worried about it.

<b>PHYSICAL EXAMINATION</b> <br> On physical examination, you note: cardiac and pulmonary auscultation is normal; ABP in left arm: 160x102mmHg; radial pulses are symmetric; chest pain does not worse with palpation of the thorax; there is no jugular stasis nor lower limb edema. You don´t find any abnormal findings on abdominal examination.

@SYSTEM: What do you want to do?

* -> Generate hypothesis
* -> More information
* Call the supervisor -> Call the supervisor.A

Generate hypothesis (input)
---------------------------
@SYSTEM: What is your main diagnostic hypothesis?


? hypothesis
  * vocabularies: mesh
  * right answers: aortic dissection, acute aortic dissection, aortic aneurysm, acute aortic syndrome
  * wrong answers: infarction, myocardial infarction, coronary syndrome, acute coronary syndrome, ischemia, myocardial ischemia, coronary insufficiency, angina, angina pectoris, pericarditis, pneumonia, myopericarditis, pneumothorax, pulmonary embolism, thromboembolism, PE, PTE

* Submit hypothesis -> Check hypothesis

More information (information)
------------------------------
  ![Emergency room](theme/background-emergency-room-2.png)

<b>MORE INFORMATION</b> <br> The patient had never felt similar chest pain before. He had never had myocardial infarction. He made a cardiovascular “check-up” last year, resulting normal. He denies smoking cigarettes, and he was not immobilized nor made long trip recently.

@PATIENT Jakob

@SYSTEM: What do you want to do?

* Back to the case -> Cycle 1.Begin

Call the supervisor
-------------------

### A (detailed)
  @SUPERVISOR Harry
    ![Supervisor Harry](theme/supervisor.png)
  
Hi! I am glad that you called me. Chest pain is an important
complaint at the emergency department and we have to exclude the
fatal causes: myocardial infarction (MI), acute aortic dissection
(AAD), pulmonary embolism PE), hypertensive pneumothorax (HP),
and Boerhaave Syndrome (BS).
The best way to find out what is happening with your patient, my young padawan, is to gather as much information as possible through history taking and physical examination. We need to search for the signs and symptoms that can guide our clinical reasoning process by changing the pre-test probabilities of each disease.


Do you know the concept of Likelihood ratio (LR)?

+ -> Clinical History Myocardial Infarction

+ -> Physical Examination Myocardial Infarction

+ -> Clinical History Aortic Dissection

+ -> Physical Examination Aortic Dissection

+ -> Pulmonary Embolism Wells Criteria

Hypertensive pneumothorax is more common in tall and thin young adults (primary pneumothorax) or in patients with chronic pulmonary diseases or chest trauma (secondary pneumothorax). On physical examination, we expect asymmetry in lung auscultation and the trachea may be dislocated to the contralateral side of the pneumothorax.
Boerhaave Syndrome is more common in patients who presented vomiting before the chest pain started, were submitted to endoscopic procedures or had chest trauma.
How does this information can help you to solve your case?

* Back to the case -> Cycle 1.Begin

### Likelihood Ratio (notice)

Likelihood ratio (LR) - like sensitivity and specificity, LR describe the discriminatory power of features in a clinical context, estimating the probability of disease. When the LR is higher than 1, the feature increases the probability; when lower than 1, reduces it.

* Back -> Supervisor B

### Clinical History Myocardial Infarction (notice)
![Clinical History Myocardial Infarction](https://www.ic.unicamp.br/~santanch/lab/health-game/jacinto-harena-5-images/case01/ebm-clinical-history-myocardial-infarction.png)

* Back -> Supervisor B

### Physical Examination Myocardial Infarction (notice)
![Physical Examination Myocardial Infarction](https://www.ic.unicamp.br/~santanch/lab/health-game/jacinto-harena-5-images/case01/ebm-physical-examination-myocardial-infarction.png)

* Back -> Supervisor B

### Clinical History Aortic Dissection (notice)
![Clinical History Aortic Dissection](https://www.ic.unicamp.br/~santanch/lab/health-game/jacinto-harena-5-images/case01/ebm-clinical-history-aortic-dissection.png)

* Back -> Supervisor B

### Physical Examination Aortic Dissection (notice)
![Physical Examination Aortic Dissection](https://www.ic.unicamp.br/~santanch/lab/health-game/jacinto-harena-5-images/case01/ebm-physical-examination-aortic-dissection.png)

* Back -> Call the supervisor B

### Pulmonary Embolism Wells Criteria (notice)
![Pulmonary Embolism Wells Criteria](https://www.ic.unicamp.br/~santanch/lab/health-game/jacinto-harena-5-images/case01/ebm-pulmonary-embolism-wells-criteria.png)

* Back -> Call the supervisor B

Check hypothesis (detailed_role)
---------------------------

@SYSTEM: Let us check out your hypothesis. Highlight in green the findings that corroborate your hypothesis; in blue those that are neutral; and in red the ones speaking against your hypothesis.

? contribution to diagnostics
  * type: group select
  * states: _, k, +, =, -
  * labels: empty, key, contibutes, indiferent, against
{{symptoms/contribution to diagnostics/

@Nurse - Doctor, please, come to the emergency room. A {man}(male) ({52 years-old}(aging=52)/=/) reports he is feeling a {very strong chest pain}/+/. His vital signs are {ABP (right arm): 164x108mmHg}/=/; HR: 124bpm; RR: 23rpm; Temp: 36,1oC; O2Sat: 96%.

@Patient - Doctor, I am feeling a very strong chest pain in the middle
of my chest. It has started 2 hours ago, but {it´s intensity isn´t
decreasing}/+/. {It has started suddenly}/+/ and {I am also feeling pain
on my back and on my neck}/+/. The pain is continuous, and {it did
not worse when I am breathing}/=/. I have {arterial hypertension}/+/ but
I don´t take my medication every day, I am sorry! I don´t smoke, and I don´t know If I have other diseases. {My father has also arterial
hypertension}/=/.

On physical examination, you note: {cardiac and pulmonary
auscultation is normal}/=/; {ABP in left arm: 160x102mmHg}/=/; {radial
pulses are symmetric}/=/; {chest pain does not worse with palpation of
the thorax}/=/; there is no jugular stasis nor lower limb edema. {You
don´t find any abnormal findings on abdominal examination}/=/.

}}

* Submit -> Review hypothesis 

Review hypothesis (input)
-------------------------

@SYSTEM: If you want to review your hypothesis, type below the new hypothesis.

? hypothesis

* Submit -> Cycle 2.Order EKG

Cycle 2
=======

## Order EKG (exam)
Our patient denies any chest trauma or vomiting. The blood
pressure is symmetric in the four limbs.

@EKG
  ![EKG](https://www.ic.unicamp.br/~santanch/lab/health-game/jacinto-harena-5-images/caso03/SOBRECARGA_DE_VE_2.jpg)

* Magnify -> Magnify EKG

@SYSTEM: What do you want to do?
* -> Generate hypothesis
* -> More information
* -> Call the supervisor

## Magnify EKG (notice,magnify_exam)

@EKG

* Return -> Order EKG

## Generate hypothesis (input)

@SYSTEM: What is your main diagnostic hypothesis?

? hypothesis

* Submit hypothesis -> Check hypothesis

## More information (information_exam)

<b>MORE INFORMATION</b>

EKG description/EKG findings

<span style="color:#0d4a71;font-weight:bold">Rhythm:</span><br>
sinus rhythm<br>
<span style="color:#0d4a71;font-weight:bold">P waves:</span><br>
normal<br>
<span style="color:#0d4a71;font-weight:bold">PR interval:</span><br>
normal; PR-segment depression in<br>
DII lead<br>
<span style="color:#0d4a71;font-weight:bold">QRS:</span><br>
narrow<br>
normal QRS axis (0 – 90 degrees)<br>
<span style="color:#0d4a71;font-weight:bold">Segmento ST e ondas T:</span><br>
supra ST in DI, DII, DIII, avF, V2-V6 leads

@EKG
  

* Analyze EKG -> EKG Analysis

@SYSTEM: What do you want to do?
* Back -> Order EKG

## EKG Analysis (notice,marker_exam)

<dcc-group-marker context="ekg" image="images/ekg.png">
   <dcc-image-marker id="DI" label="DI" coords="238,127,164,76" image="images/ekg-detail-01.png"></dcc-image-marker>
   <dcc-image-marker id="DII" label="DII" coords="231,328,148,273" image="images/ekg-detail-01.png"></dcc-image-marker>
   <dcc-image-marker id="DIII" label="DIII" href="" coords="67,484,148,528" image="images/ekg-detail-02.png"></dcc-image-marker>
   <dcc-image-marker id="aVL" label="aVL" coords="413,286,515,332" image="images/ekg-detail-01.png"></dcc-image-marker>
   <dcc-image-marker id="IV" label="IV" coords="1005,40,1123,130" image="images/ekg-detail-01.png"></dcc-image-marker>
   <dcc-image-marker id="V" label="V" coords="1004,248,1133,323" image="images/ekg-detail-01.png"></dcc-image-marker>
   <dcc-image-marker id="VI" label="VI" coords="1010,460,1130,538" image="images/ekg-detail-01.png"></dcc-image-marker>
</dcc-group-marker>

* Return -> Order EKG

## Call the supervisor (exam)
@"SUPERVISOR Harry" - My young padawm, we are really facing a very difficult case.
Our patient´s chest pain irradiates to his back and was sudden, both
features that increases the likelihood ratio for acute aortic dissection.
Besides, our patient has arterial hypertension, an EKG showing
signs of left ventricular hypertrophy, which further increases the
same likelihood ratio.
We found a St-segment elevation in V2 and V3. In Left ventricular
hypertrophy, in precordial leads V1 – V3, it is usual to find a St-
segment elevation, which is maior conforme a profundidade da onda
S. Observe que o supra tem concavidade superior, e é seguido de
onda T positiva e assimétrica (normal), e portanto consideramos o
supra secundário a hipertrofia ventricular, e não secundário à
isquemia.

* -> EKG Analysis

@EKG

@SYSTEM: What do you want to do?
* Back -> Order EKG

## Check hypothesis (marker_exam)

<dcc-group-marker context="ekg" image="images/ekg.png">
   <dcc-image-marker id="DI" label="DI" coords="238,127,164,76" image="images/ekg-detail-01.png"></dcc-image-marker>
   <dcc-image-marker id="DII" label="DII" coords="231,328,148,273" image="images/ekg-detail-01.png"></dcc-image-marker>
   <dcc-image-marker id="DIII" label="DIII" href="" coords="67,484,148,528" image="images/ekg-detail-02.png"></dcc-image-marker>
   <dcc-image-marker id="aVL" label="aVL" coords="413,286,515,332" image="images/ekg-detail-01.png"></dcc-image-marker>
   <dcc-image-marker id="IV" label="IV" coords="1005,40,1123,130" image="images/ekg-detail-01.png"></dcc-image-marker>
   <dcc-image-marker id="V" label="V" coords="1004,248,1133,323" image="images/ekg-detail-01.png"></dcc-image-marker>
   <dcc-image-marker id="VI" label="VI" coords="1010,460,1130,538" image="images/ekg-detail-01.png"></dcc-image-marker>
</dcc-group-marker>

* Submit -> Review hypothesis

## Review hypothesis (input)
If you whant to review your hypothesis, type below the new hypothesis.
@PATIENT Jakob
? hypothesis

* Submit -> Final.Report

Final
=====

Report (detailed)
-----------------

Congratulations, my young Dr. you could helped your patient providing his diagnosis. Now, Let's review all levels of this case.

@Computer: Select a final report level:

* -> Level 1
* -> Level 2.2a
* -> Level 3.3a

Level 1 (detailed)
------------------

<b>Level 1</b>: your answer was ^Cycle 1.Generate hypothesis.hypothesis^.

* Next -> Level 2.2a


Level 2
-------

### 2a (detailed)

<div style="font-size: 14px">
<b>Level 2</b>: At this level, we asked you to highlight in green all features that corroborate your hypothesis, in blue those are neutral and in red the ones speaking against your hypothesis.
<br><br>
<b>Your answer:</b>
^Cycle 1.Check hypothesis.contribution to diagnostics^
<br><br>
<b>Our answer:</b> 
<br>
^Cycle 1.Check hypothesis.contribution to diagnostics(right)^
</div>

* Next -> 2b


### 2b (detailed)

* Next -> 2c


### 2c (detailed)

* Next -> Level 3.3a


Level 3
-------

### 3a (detailed)

* Next -> 3b


### 3b (detailed)

* Next -> 3c


### 3c (detailed)
<div style="font-size: 18px">
In the following table, we provide the diagnostic criteria for :

![Clinical History Myocardial Infarction](https://www.ic.unicamp.br/~santanch/lab/health-game/jacinto-harena-5-images/case01/ebm-pericarditis.png)

Cooper LT, Imazio M. Management of myopericarditis. Expert Rev Cardiovasc Ther 2013; 11(2): 193-201.

Our patient fullfill the following criteria: 1 and 3. So, acute pericarditis is the main diagnostic hypothesis.
</div>

# _Case_
* theme: jacinto
* title: phillmuchbetter-case03
