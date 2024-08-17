---
layout: page
title: DL 380 NAS
description: Repurposing used enterprise equipment into a home NAS
img: assets/img/NAS/NAS.jpg
importance: 1
category: technical
related_publications: true
---

With increasing affordability of used enterprise equipment I decided to repurpose an old HP server for a NAS. I found an HP ProLiant on Ebay with the following specs:


    2x E5-2620v4 processors
    128Gb EEC RAM
    LFF backplane

To repurpose this unit, I also purchased an LSI HBA card, and a Mellanox cx3 for high speed networking.

<div class="row">
        <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/NAS/NAS.jpg" title="HP" class="img-fluid rounded z-depth-1" %}
            <div class="caption">
            DL380
            </div>
    </div>
        <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/NAS/lsi.jpg" title="LSI" class="img-fluid rounded z-depth-1" %}
            <div class="caption">
            LSI HBA
            </div>
    </div>
        <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/NAS/cx3.jpg" title="CX3" class="img-fluid rounded z-depth-1" %}
            <div class="caption">
            Mellanox CX3
            </div>
    </div>
</div>

Utlizing the existing PCIe risers, I simply assembled these cards into the servers and connected the HBA cabling to the backplane.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/NAS/internal.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/NAS/cards.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The mellanox SFP+ cabling was attached to my TP-Link 10g switch.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/NAS/switch.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    TL-SX3008F
</div>

Once the networking was sorted out, I installed trueNas scale onto the system and configured the drives.

<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/NAS/truenas.png" title="example image" class="img-fluid rounded z-depth-1"%}
    </div>
        <div class="col-lg mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/NAS/drives.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Finally I set up SMB shares so that I could easily transfer data from my desktop to the server.

<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/NAS/10g.jpg" title="example image" class="img-fluid rounded z-depth-1"%}
    </div>
        <div class="col-lg mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/NAS/smb.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
