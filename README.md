# Quantifying performance of Red Hat OpenShift for Machine Learning (ML) Training on Supermicro  A+ Servers with MLPerf Training v3.1

## Summary
We are proud to announce the first MLPerf Training submission on OpenShift, which is also the first ever MLPerf training submission on a variant of Kubernetes.  This demonstates the power of OpenShift to solve real world ML problems efficiently while providing all the benefits of enterprise kubernetes container orchestration. Red Hat partnered with Supermicro on this submisison and ran the benchmarks on a Supermicro GPU A+ Server with 8XH100 Nvidia GPUs. Red Hat OpenShift is leading the way in making it easier to run, reproduce and monitor your AI/ML workloads, while adding minimal overhead to your training jobs.  

In this blog we provide the performance numbers of our recent submission to MLPerf v3.1 training. 


## MLPerf Training v3.1 performance results


OpenShift performed excepetionally well when compared to baremetal (Ubuntu only) results, on the same Superimcro GPU A+ Server with 8XH100 GPUs. 

We have two impressive MLPerf training v3.1 benchmark submissions using Red Hat Openshift 4.13, on a Supermicro GPU A+ Server with 8 directly attached Nvidia H100 GPUs.  The Red Hat/Supermicro MLPerf Training v3.1 benchmark results closely match baremetal results (within the error bar +/- 1 standard deviation of the mean). We ran MLPerf training with Supermicro GPU A+ Server 8XH100, and compared our results with baremetal (Ubuntu results) on the same hardware.  


Overall, this shows that running these training benchmarks on OpenShift did not add significant overhead and time-to-train is similar to baremetal training time.  Red Hat OpenShift makes it easier to run, reproduce and monitor your AI/ML workloads, while adding very minimal overhead to your training jobs.

## MLPerf Training Benchmark

MLPerf is the industry standard open-source Machine Learning (ML) Benchmark with real world workloads for Natural Languge Processing (NLP), Computer Vision (image classification, object detection & medical image segmentation). The MLPerf Training benchmark suite measures how fast the system can train a model to a target accuracy. 

## ResNet 50 

ResNet-50 is a popular model for performing image classifiation.  

The following graphs show ResNet-50 training results.  The Red Hat OpenShift 4.13 training result is within .4% of the baremetal ResNet-50 results. 

<img width="468" alt="image" src="https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/blob/main/Resnet_Density.png"><img width="468" alt="image" src="https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/blob/main/ResNet_BoxPlot.png">

## Unet3D

The Unet3D model performs a 3D medial image segmentation task using the 2019 Kidney Segmentation Challenge dataset called KiTS19.  The task is carried out using a U-Net3D model variant based on the No New-Net paper. 


The OpenShift Unet3D results are within the error bar (one standard deviation from the mean ) of the baremetal results.  The Unet3D benchmark has a random component which makes it useful to view the results in terms of standard deviation, or spread of the data, rather than representing the result as one number. 

<img width="468" alt="image" src="https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/blob/main/Unet3D_Density.png"><img width="468" alt="image" src="https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/blob/main/Unet3D_Boxplot.jpeg">

## Red Hat OpenShift Benefits 

Red Hat OpenShift made it easy to deploy and monitor the containerized ML applications used in this benchmark.  Red Hat Openshift Operators and the Nvidia GPU Operator discovered, configured and enabled the GPUs and locally attached storage (NVMe drives) used in this benchmark. 

## Operators
The figure below shows the Operators we installed for the Red Hat/Supermicro MLPerf trianing v3.1 submission.  These operators automate many tasks associated with discovering and configuring cluster resources making it much easier to operator you clusters.



![OC-console-GPU-Util4](https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/blob/main/Operators_screenshot.jpeg)

## Nvidia GPU Operator Dashboard

As shown in the following figure the Nvidia GPU ultizaiton is a useful tool when determine if your GPUs are over or under utilized when tuning an AI/ML application.  This dashboard is a screen available in the Red Hat OpenShift web console: 


![OC-console-GPU-Util4](https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/blob/main/NvidiaGPUOPeratorDashboard.jpeg)


## Conclusions 

This submission demonstrates the delivery of outstanding performance, within the error bar of bare metal, while providing an exceptional Developer, User and DevOps experience.
Red Hat OpenShift is now available for a free trial period of 60-days, on premise and in multiple public clouds. 




## Acknowledgements

We would like to thank our partner Supermicro for providing servers and assistance creating this MLPerf Training Submission. 
