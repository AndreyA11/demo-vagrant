<a name="readme-top"></a>
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## Vagrant with ansible demo

Demonstration example of configuring VM using vagrant with ansible for starting Docker containers.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

### Prerequisites

* [Vagrant](https://developer.hashicorp.com/vagrant/downloads)
* [vagrant-supported hypervisor (except Docker)](https://developer.hashicorp.com/vagrant/docs/providers)
* Vagrant provider for your virtualization software (reboot may be required after installation)
* Internet connection without proxy
* Configured user password for SMB sharing on Windows computers

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/AndreiA11/demo-vagrant.git
   ```
2. Change directory 
   ```sh
   cd demo-vagrant
   ```
4. Run VM creation process
   ```sh
   vagrant up
   ```
5. Vagrant may ask your local computer credentials for configuring smb share connection inside the VM
6. Start provisioning again if something like internet connection was broken
   ```sh
   vagrant provision
   ```
7. Open [localhost:3000](http://localhost:3000/) when you'll get "configuration complete" message. Hyper-V provider doesn't support port forwarding. In this case you can use VM's ip address as an alternative: ![complete-screenshot][complete-screenshot]
8. Choose docker-engine job
<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the Apache License 2.0. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Andrei Andriushin - [![LinkedIn][linkedin-shield]](https://linkedin.com/in/andrei-andriushin/)

Project Link: [https://github.com/AndreiA11/demo-vagrant](https://github.com/AndreiA11/demo-vagrant)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* Acme is a fictional name for demonstration purpose
* [Vagrant Quick Start](https://developer.hashicorp.com/vagrant/tutorials/getting-started)
* [Generic boxes (images) for vagrant. Maintaned by community](https://app.vagrantup.com/generic)
* [Grafana Dashboard for Node Exporter](https://grafana.com/grafana/dashboards/1860)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[complete-screenshot]: images/complete-screenshot.png