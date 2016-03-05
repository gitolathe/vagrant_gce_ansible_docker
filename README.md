# Docker enabled VM on GCE
Vagrant + Ansible provisioning for a Docker machine on GCE.

The prerequisite is to enable Vagrant to provisioning an instance on GCE as described in [Setup Development Environment with Vagrant on Google Compute Engine](https://realguess.net/2015/09/07/setup-development-environment-with-vagrant-on-google-compute-engine/).

An "admin" instance on GCE is used to host the Ansible playbooks as well as Vagrant. Ansible is installed following the procedure for Ubuntu at [Latest Releases Via Apt (Ubuntu)](http://docs.ansible.com/ansible/intro_installation.html#latest-releases-via-apt-ubuntu).
