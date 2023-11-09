# Quantifying performance of Red Hat OpenShift for Machine Learning (ML) Training on Supermicro  A+ Servers with MLPerf Training v3.1

## Summary:
We are proud to announce the first MLPerf Training submission on OpenShift, which is also the first ever MLPerf training submission on a variant of Kubernetes.  This demonstates the power of OpenShift to solve real world ML problems efficiently while providing all the benefits of enterprise grade container orchestration. We partnered with Supermicro on this submisison and ran the benchmarks on a Supermicro GPU A+ Server with 8XH100 Nvidia GPUs. Red Hat OpenShift is leading the way in making it easier to run, reproduce and monitor your AI/ML workloads, while adding minimal overhead to your training jobs.  

In this blog we provide the performance numbers of our recent submission to MLPerf v3.1 training. 


## MLPerf Training v3.1 performance results:


OpenShift performed excepetionally well when compared to baremetal (Ubuntu only) results, on the same Superimcro GPU A+ Server with 8XH100 GPUs. 

We have two impressive MLPerf training benchmark submissions using Red Hat Openshift 4.13, on a Supermicro GPU A+ Server with 8 directly attached Nvidia H100 GPUs.  The Red Hat/Supermicro MLPerf Training v3.1 benchmark results closely match baremetal results (within the error bar +/- 1 standard deviation of the mean). 


Overall, this shows that running these training benchmarks on OpenShift did not add significant overhead and has time-to-train similar to baremetal. We ran MLPerf training with 8XH100 Nvidia GPU (AMD Epyc CPU), and compared our results with baremetal (Ubuntu results) on the same hardware.   The take away is that Red Hat OpenShift makes it easier to run, reproduce and monitor your AI/ML workloads, while adding minimal overhead to your training jobs.

MLPerf is the industry standard open-source Machine Learning (ML) Benchmark with real world workloads for Natural Languge Processing (NLP), Computer Vision (image classification, object detection & medical image segmentation). The MLPerf Training benchmark suite measures how fast the system can train a model to a target accuracey. We ran MLPerf training with 8XH100 Nvidia GPU (AMD Epyc CPU), and compared our results with baremetal (Ubuntu results) on the same hardware.

## ResNet 50 

ResNet-50 is a popular model for performaing image classifiation.  

The following graphs show ResNet-50 training results.  The Red Hat OpenShift 4.13 training result is within .4% of the baremetal ResNet-50 results. 

<img width="468" alt="image" src="https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/assets/3208719/c494d8c3-903d-4e48-afb4-fd318bd035a4">

<img width="468" alt="image" src="https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/assets/3208719/be2ba6be-d0ce-4a52-b309-0a5cc84e27af">

## Unet3D

The Unet3D model performs a 3D medial image segmentation task using the 2019 Kidney Segmentation Challenge dataset called KiTS19.  The task is carried out using a U-Net3D model variant based on the No New-Net paper. 


The OpenShift Unet3D results are within the error bar (one standard deviation from the mean ) of the baremetal results.  The Unet3D benchmark has a random component which makes it useful to view the results in terms of standard deviation, or spread of the data, rather than representing the result as one number. 

<img width="468" alt="image" src="https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/assets/3208719/2d1ec0b4-0ea7-481a-aee0-406a661b6995">

<img width="468" alt="image" src="https://github.com/openshift-psap/blog-MLPerfTraining-v3.1/assets/3208719/207055aa-55bf-43bb-8179-4e3be27b1350">


## Conclusions 

This submission demonstrates the delivery of outstanding performance, within the error bar of bare metal, while providing an exceptional Developer, User and DevOps experience.
Red Hat OpenShift is now available for a free trial period of 60-days, on premise and in multiple public clouds. 




## Acknowledgements

We would like to thank our partner Supermicro for providing servers and assistance creating this MLPerf Training Submission. 
