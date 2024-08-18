---
layout: page
title: DL 380 Virtualization Server
description: Repurposing used enterprise equipment for virtualization
img: assets/img/proxmox/dl380.jpg
importance: 1
category: technical
related_publications: true
---

Similar to the [repurposed NAS](/projects/NAS/), I decided to create a server I could use for virtualization. I found an HP ProLiant on Ebay with the following specs:


    2x E5-2680v4 2.4GHz
    96Gb EEC RAM

As this is essentially what these servers are designed for only slight modifications were needed for the tasks I had in mind.

<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/NAS/cx3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
        Mellanox CX3
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proxmox/dl380.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
        HP DL380
        </div>
    </div>
</div>

I also added a Mellanox CX3 card to this machine so that I could have 10G networking between my NAS and this machine. As a hypervisor I decided to use proxmox, mostly because it has a price tag you can't pass up (0$).


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proxmox/prox.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Proxmox
</div>

Setting up a virtual machine is as easy as clicking through a couple menus and setting up the hardware how you see fit. In the following case I set up a single socket 16 core CPU, 64GB of memory, and an image for Ubuntu server.

<div class="row">
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proxmox/vm1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proxmox/vm2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proxmox/vm3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proxmox/vm4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>                 
</div>
<div class="row">
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proxmox/vm5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>   
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proxmox/vm6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>   
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proxmox/vm7.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>   
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proxmox/vm8.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>  
</div>            

Once the VM boots up, setting up Ubuntu is as the same as installing it on a bare metal machine.

<div class="row">
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proxmox/ubuntu.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>   
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proxmox/ubuntu2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>   
</div>        

From here we can do anything we like!

<div class="row">
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proxmox/ubuntu3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>    
<div class="caption">
Ubuntu terminal
</div>   