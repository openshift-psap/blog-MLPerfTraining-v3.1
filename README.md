# Quantifying performance of Red Hat OpenShift for Machine Learning (ML) Training on Supermicro  A+ Servers with MLPerf Training v3.1
November 2023 | by Diane Feddema
## Summary
We are proud to announce the first MLPerf Training submission on Red Hat OpenShift, which is also the first MLPerf training submission on a variant of Kubernetes.  This demonstrates the power of Red Hat OpenShift to solve real world machine learning (ML) problems efficiently while providing all the benefits of enterprise Kubernetes container orchestration. Red Hat collaborated with Supermicro on this submission and ran the benchmarks on a Supermicro GPU A+ Server with 8XH100 NVIDIA GPUs. Red Hat OpenShift helps make it easier to run, reproduce and monitor your AI/ML workloads, while adding minimal overhead to your training jobs.  

In this blog we provide the performance numbers of our recent submission to MLPerf v3.1 training. 


## MLPerf Training v3.1 performance results


Red Hat OpenShift performed well when compared to baremetal (Ubuntu only) results, on the same Superimcro GPU A+ Server with 8XH100 GPUs. 

We have two impressive MLPerf training v3.1 benchmark submissions using Red Hat Openshift 4.13, on a Supermicro GPU A+ Server with 8 directly attached NVIDIA H100 GPUs.  The Red Hat/Supermicro MLPerf Training v3.1 benchmark results closely match baremetal results (within the error bar +/- 1 standard deviation of the mean). We ran MLPerf training with Supermicro GPU A+ Server 8XH100, and compared our results with baremetal (Ubuntu results) on the same hardware.  


Overall, this shows that running these training benchmarks on Red Hat OpenShift did not add significant overhead and time-to-train and is similar to baremetal training time.  Red Hat OpenShift makes it easier to run, reproduce and monitor your AI/ML workloads, while adding very minimal overhead to your training jobs.

## MLPerf Training Benchmark

MLPerf is the industry standard open source machine learning benchmark with real world workloads for natural languge processing (NLP), and computer vision (image classification, object detection & medical image segmentation). The MLPerf Training benchmark suite measures how fast the system can train a model to a target accuracy. 

## ResNet 50 

ResNet-50 is a popular model for performing image classification.  

The following graphs show ResNet-50 training results.  The Red Hat OpenShift 4.13 training result is within .4% of the baremetal ResNet-50 results. 

<img width="468" alt="image" src="https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/blob/main/Resnet_Density.png"><img width="468" alt="image" src="https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/blob/main/ResNet_BoxPlot.png">

## Unet3D

The Unet3D model performs a 3D medical image segmentation task using the 2019 Kidney Segmentation Challenge dataset called KiTS19.  The task is carried out using a U-Net3D model variant based on the No New-Net paper. 


The Red Hat OpenShift Unet3D results are within the error bar (one standard deviation from the mean) of the baremetal results.  The Unet3D benchmark has a random component which makes it useful to view the results in terms of standard deviation, or spread of the data, rather than representing the result as one number. 

<img width="468" alt="image" src="https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/blob/main/Unet3D_Density.png"><img width="468" alt="image" src="https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/blob/main/Unet3D_Boxplot.jpeg">

## Red Hat OpenShift Benefits 

Red Hat OpenShift made it easy to deploy and monitor the containerized ML applications used in this benchmark.  Red Hat Openshift Operators and the NVIDIA GPU Operator discovered, configured and enabled the GPUs and locally attached storage (NVMe drives) used in this benchmark. 

## Operators
The figure below shows the Operators we installed for the Red Hat/Supermicro MLPerf trianing v3.1 submission.  These Operators automate many tasks associated with discovering and configuring cluster resources making it much easier to operate clusters.



![OC-console-GPU-Util4](https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/blob/main/Operators_screenshot.jpeg)

## NVIDIA GPU Operator Dashboard

As shown in the following figure the NVIDIA GPU Operator dashboard is a useful tool for determining if your GPUs are over or under utilized when tuning an AI/ML application.  This dashboard is a screen available in the Red Hat OpenShift web console: 


![OC-console-GPU-Util4](https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/blob/main/NvidiaGPUOPeratorDashboard.jpeg)


## Conclusions 

This submission demonstrates the delivery of outstanding performance, within the error bar of bare metal, while providing an exceptional developer, user and DevOps experience.
Red Hat OpenShift is now available for a free trial period of 60-days, on premise and in multiple public clouds. 




## Acknowledgements

We would like to thank our partner Supermicro for providing servers and assistance creating this MLPerf Training Submission. 
