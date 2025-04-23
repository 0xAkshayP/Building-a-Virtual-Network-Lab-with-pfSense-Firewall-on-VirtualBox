# Building-a-Virtual-Network-Lab-with-pfSense-Firewall-on-VirtualBox
<h1>🧱 pfSense Firewall Project in VirtualBox</h1>

<p>A step-by-step lab setup to install and configure pfSense as a firewall/router in a virtual network using VirtualBox.</p>

<h2>📋 Requirements</h2>
<ul>
  <li>VirtualBox (latest)</li>
  <li>pfSense ISO: <a href="https://www.pfsense.org/download/">Download here</a></li>
  <li>Ubuntu or Windows ISO (for client machine)</li>
  <li>4GB RAM (minimum)</li>
</ul>

<h2>📁 Project Setup Overview</h2>
<ol>
  <li>Download pfSense ISO</li>
  <li>Create VMs for pfSense and LAN client</li>
  <li>Configure networking using NAT and Internal Network</li>
  <li>Install and configure pfSense</li>
  <li>Test connectivity and implement firewall rules</li>
</ol>

<h2>⚙️ Steps to Install pfSense</h2>
<h3>1. Download pfSense ISO</h3>
<p>Go to the <a href="https://www.pfsense.org/download/">official site</a> and download the ISO (AMD64).</p>

<h3>2. Create pfSense VM in VirtualBox</h3>
<ul>
  <li><strong>Name:</strong> pfSense</li>
  <li><strong>Type:</strong> BSD</li>
  <li><strong>Version:</strong> FreeBSD (64-bit)</li>
  <li><strong>Memory:</strong> 1024–2048 MB</li>
  <li><strong>Network:</strong> Adapter 1 = NAT, Adapter 2 = Internal Network (<code>intnet</code>)</li>
</ul>

<h3>3. Install pfSense</h3>
<p>Boot the ISO and follow the installation wizard:</p>
<ul>
  <li>Select "Install", use default options</li>
  <li>Auto partition and install</li>
  <li>Reboot and assign interfaces</li>
</ul>

<h3>4. Set Interfaces</h3>
<ul>
  <li><strong>WAN:</strong> Adapter 1 (NAT)</li>
  <li><strong>LAN:</strong> Adapter 2 (Internal)</li>
</ul>

<h3>5. Create LAN Client VM</h3>
<ul>
  <li>Use Ubuntu or Windows ISO</li>
  <li>Set network adapter to Internal Network (<code>intnet</code>)</li>
  <li>Boot and connect to pfSense LAN (via DHCP)</li>
</ul>

<h3>6. Access pfSense Web UI</h3>
<ul>
  <li>Open <code>http://192.168.1.1</code> in the LAN Client browser</li>
  <li>Login with <code>admin / pfsense</code></li>
  <li>Run the initial setup wizard</li>
</ul>
