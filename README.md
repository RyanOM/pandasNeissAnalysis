# An analysis of the United States Consumer Product Safety Commission’s National Electronic Injury Surveillance System (NEISS) data using Python and Pandas.

Each question is answered individually in its own notebook. 
These notebooks can be viewed using Jupyter nbviewer:
https://nbviewer.jupyter.org/github/RyanOM/pandasNeissAnalysis/tree/master/


---

### Question 1
```
What are the top three body parts most frequently represented in this dataset?
What are the top three body parts that are least frequently represented?
```

#### Answer:

[View notebook Question1.ipynb](https://nbviewer.jupyter.org/github/RyanOM/pandasNeissAnalysis/blob/master/Question1.ipynb)


The top 3 most frequently body parts represented in this dataset are **Head**, **Face** and **Finger**:

BodyPart | Frequency
--- | ---
Head | 9891
Face | 5786
Finger | 5783


The top 3 less frequently body parts represented in this dataset are **Arm, upper**, **Internal** and **Pubic region**:

BodyPart | Frequency
--- | ---
Arm, upper | 745
Internal | 549
Pubic region | 286

---

### Question 2
```
How many injuries in this dataset involve a skateboard?
Of those injuries, what percentage were male and what percentage were female?
What was the average age of someone injured in an incident involving a skateboard?
```

### Answer:
[View notebook Question2.ipynb](https://nbviewer.jupyter.org/github/RyanOM/pandasNeissAnalysis/blob/master/Question2.ipynb)

The number of injuries that involved a skateboard: **466**


Percentage skateboard incidents Female/Male:

Sex | Percentage | Nb incidents
--- | --- | ---
Female | 17.6% | 82
Male | 82.4% |  384


The average age of someone injured in an incident involving a skateboard: **17.99 years old**

---

### Question 3
```
What diagnosis had the highest hospitalization rate? 
What diagnosis most often concluded with the individual leaving without being seen?
Briefly discuss your findings and any caveats you'd mention when discussing this data
```

### Answer:
[View notebook Question3.ipynb](https://nbviewer.jupyter.org/github/RyanOM/pandasNeissAnalysis/blob/master/Question3.ipynb)


**Submersion** had the highest hospitalization rate.

**Poisoning** most often concluded with the individual leaving without being seen


Briefly discuss your findings and any caveats you'd mention when discussing this data:

The **narrative** field is plain text / non-structured and not always consistent. 
For example there are a few different ways to say `the patient left without being seen`: **left w/o being seen**, **left w ithout**, etc
Making this data hard to analyze & quantify since it may contain typos

The  are also 394 cases where specific body parts aren't mentioned (**Not Recorded** and **25-50% of body**, [as seen in Question1.ipynb](https://nbviewer.jupyter.org/github/RyanOM/pandasNeissAnalysis/blob/master/Question1.ipynb)
)

---

### Question 4
```
Visualize any existing relationship between age and reported injuries
```

### Answer:
[View notebook Question4.ipynb](https://nbviewer.jupyter.org/github/RyanOM/pandasNeissAnalysis/blob/master/Question4.ipynb)

Infants between the age of 1 to 12 are often diagnosed with Lacerations. The most likely affected body part being th head.

Teenagers and Young Adults are most often diagnosed with Strains/Sprains.

Senior Adults are more prone to fractures and abrasions to the head, trunk and face (probably due to falls).

---

### Question 5
```
Investigate the data however you like and discuss any interesting insights you can find in the data

```

### Answer:
[View notebook Question5.ipynb](https://nbviewer.jupyter.org/github/RyanOM/pandasNeissAnalysis/blob/master/Question5.ipynb)

##### Calendar Results

Saturday, Sundays and Mondays have more patients registered than other days of the week.

May and June are the months with the highest numbers of patients while November and December have the least.

##### Fatality Results
      
The diagnosis that most resulted in deaths was **Other/Not Stated**: 46.4%. 
This shows the need to better record the causes of death.
      
**Internal organ injury** was the second most common cause of death: 25%

##### Transfered to other facilities Results

The diagnosis that has the highest transfer rate to other facilities is **Amputation**: 9.6%

Even though **Fractures** is the diagnosis that is the most transfered with **267 cases**, this only represents **2.74% of the total cases**