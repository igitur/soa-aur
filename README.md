# Squeeze on Arch (SOA) Arch User Repository

Repository for building Squeeze applications on Arch Linux

This repository is made available free of charge for
non-commercial private use. Any commercial usage is strictly
prohibited.

SQUEEZE ON ARCH IS PROVIDED "AS IS" AND ANY EXPRESS OR IMPLIED
WARRANTIES ARE DISCLAIMED. IN NO EVENT SHALL THE SOFTWARE PROVIDER BE
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF
SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR
BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE
OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN
IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

Use of Squeeze on Arch is at your own risk.


## Instructions for initial installation

1) Install a base Linux Arch installtion on your machine and connect to it as root (using ssh or otherwise)

2) Update the base software and install minimal files to build applications:

pacman -Syu --noconfirm

pacman -S --noconfirm git base-devel

3) Create a user with sudo capability (** needed as of makepkg 4.2.0 **) - Note 1

4) As that user clone the soa-aur files and start installation

git clone https://github.com/SqueezeOnArch/soa-aur.git

cd soa-aur

./soa-install.sh

(this will take several minutes to download and build the applications for your device)

5) Connect to the device using a web browser to see the configuration interface and install optional components such as jivelite and squeeze server


Note 1 - user should be "aur" with soa-aur cloned in directory /aur to enable SoA update mechanisms
