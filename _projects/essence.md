---
layout: page
title: ESSENCE CubeSat Mission
description: "From concept to orbit: Engineering a university student-led satellite mission."
img: assets/img/essence_logo_png.png
importance: 1
category: work
tags: [Systems Engineering, V&V, Space Engineering]
---

## At a glance
- **Roles**: Systems Engineer, Electrical Engineer, V&V Engineer
- **Timeline & Context**: Sep 2019 - Aug 2023 | Academic
- **Skills**: Requirements Management, Assembly Integration and Test (AIT), Circuit Diagrams and Design, System Diagrams, Stakeholder Meetings
- **Tools**: KiCAD, SysML, Python, Arduino C++

### Summary
It is a rare privilege to be part of a satellite mission from its initial whiteboard concepts all the way to a successful orbital launch. It is even rarer when that entire lifecycle is driven by a team of university students. 

The ESSENCE CubeSat mission was exactly that: a fully student-led space project that demanded professional-grade engineering, rigorous testing, and uncompromising project management to design a working satellite and launch it into space within 4 years.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/essence_mission_diag.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/essence_sat.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/essence_integration_test.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    On the left, the ESSENCE Mission Overview Diagram. Middle, the ESSENCE satellite poses for a photo at the Canadian Space Agency. Right, the final ESSENCE - NanoRacks Integration Test, AKA "the fit test".
</div>

## The Mission & The Challenge
- **Mission Objectives**: 
    1. Perform Earth observation of northern ice melt
    2. Demonstrate ADCS Experiment
    3. Qualify low-cost commercial hardware for space.
- **Solution**: ESSENCE, a 3U CubeSat featuring a Canadensys optical payload, a hybrid reaction wheel/magnetorquer ADCS experiment, and subsystems powered by popular commercial off-the-shelf (COTS) components: a Raspberry Pi Zero and Arduino Uno.
- **Impact**: Engineered for a 2-year orbital mission to capture critical environmental imagery while validating COTS components and hybrid attitude control strategies in space.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/essence_team_photo.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The ESSENCE team, just before COVID lockdown. This moment was later featured by the <a href="https://x.com/csa_asc/status/1365330116977389573?s=20">Canadian Space Agency</a>. Yours truly front and center!
</div>

## Technical Contributions
### Systems Engineering
I initially joined the project as a Systems Engineer. I managed a complex, mission critical requirements matrix across multiple major space organizations and payload partners. To ensure strict cross-agency compliance, I frequently presented to these stakeholders during formal Waterfall design reviews:
#### SpaceX
Dictated the CubeSat's launch survivability constraints. This included strict vibration tolerances, payload power restrictions during transit, and requirements for the physical placement of the Remove Before Flight (RBF) pin.
#### NanoRacks
NanoRacks operates the NanoRacks CubeSat Deployer (NRCSD) on the International Space Station (ISS), the Canadian Space Agency's (CSA) chosen orbital insertion method for the project. They governed our deployment constraints, demanding strict dimensional compliance to fit the deployer and mandating a strict 30-minute power-on delay post-deployment that *had* to be hardware-driven, bypassing any software timers.
#### NASA and CSA
Enforced launch site safety protocols for the Cape Canaveral launch facility, as well as end-of-life orbital debris mitigation and deorbiting regulations.
#### Canadensys
Supplied the primary Earth imaging payload. They provided operational constraints including power budgets, Attitude Determination and Control System (ADCS) pointing accuracy, and downlink bandwidth requirements necessary for successful image capture and transmission.
#### Toronto Metropolitan University (formerly Ryerson University)
Provided a secondary ADCS experiment payload. They defined system-level operational requirements for the experiment, including strict mass and power allocations.

Requirements Management, managing customer requirements from 3 different agencies: NASA, CSA,  NanoRacks, SpaceX. SpaceX provided launch requirements such as vibration tolerances, Payload power rules, RBF pin location, etc. NanoRacks provided additional launch requirements as the cubesat was to be launched from the NanoRacks Cubesat Deployer on the International Space Station, this included cubesat size requirements - it had to fit in the launcher, power-on procedure requirements: Must power on no sooner than 30 minutes after being launched from the deployer, and could not be a onboard computer software based timer. NASA provided additional launch requirements for use of the Cape Canaveral launch site and deorbiting requirements through the Canadian Space Agency.

### V&V Engineering
Assembly, Integration and Test procedures: Created the Assembly, INtegration and Test procedures for all satellite systems and subsystems. Outlined procedures for the vibration test at CSA's David Florida Lab (later replaced by a private lab due to COVID). Designed test for NanoRacks requirements called the 'fit test', involving machining a case the same dimensions as the NanoRacks launcher, and fitting the cubesat into the case to ensure the fit is as expected. Designed travel procedures for the cubesat to travel from Toronto to Ottawa for the vibration test, then Toronto to Cape Canaveral for launch.

### Electrical Engineering
Drafted numerous PCB drawings in KiCAD, connectivity diagrams for an Arduino Uno and a Raspberry Pi Zero, a 30-minute timer using ICs, an RBF pin circuit.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
