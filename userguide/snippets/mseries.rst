#include snippets/copyright.rst

.. index:: M-Series Unified Storage Array

.. _M-Series Unified Storage Array:

M-Series Unified Storage Array
------------------------------

The %brand% M-Series Unified Storage Array is a 4U, 24-bay, hybrid
data storage array.


#include snippets/perfect.rst


.. index:: M-Series Unified Storage Array Contents

Carefully unpack the shipping boxes and locate these components:

.. figure:: images/tn_m_parts.png


M-Series Unified Storage Array, M-Series Bezel, set of rackmount
rails, up to 24 drive trays populated with drives, DB9 to 3.5mm serial
cable, and an accessory kit with 2 IEC C13 to NEMA 5-15P power cords,
2 IEC C14 to C13 cords, velcro cable ties, M4x4L screws, M5x18 screws,
screw posts, and alternate pins for round hole racks.


.. raw:: latex

   \newpage


.. index:: Become Familiar with the M-Series System
.. _Become Familiar with the M-Series System:

Become Familiar With the M-Series System
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The M-Series has front panel indicators for power, locate ID, and
fault. The fault indicator is on during the initial power-on self-test
(POST) and turns off during normal operation. It turns on if the
%brand% software issues an
`alert <%docurl%/%brandlower%/tn_options.html#alert>`__.


.. _m_indicators:

.. figure:: images/tn_m_indicators.png
   :width: 30%


.. raw:: latex

   \newpage


The M-Series has one or two storage controllers in an over-and-under
configuration. Examples of typical M40 (top) and M50 (bottom) models
are shown here.

.. _m_back:

.. figure:: images/tn_m_back.png
   :width: 97%


.. tabularcolumns:: |>{\RaggedRight}p{\dimexpr 0.5\linewidth-2\tabcolsep}
                    |>{\RaggedRight}p{\dimexpr 0.5\linewidth-2\tabcolsep}|

.. table::
   :class: longtable

   +----------------------------------------------+----------------------------------------------+
   | 1: Redundant power supplies                  | 8: ID LED                                    |
   +----------------------------------------------+----------------------------------------------+
   | 2: Serial port                               | 9: HD Mini SAS3 connectors                   |
   +----------------------------------------------+----------------------------------------------+
   | 3: 1Gb Ethernet Out of Band (OOB) dedicated  | 10: Networking port                          |
   | management port, dual USB 2.0 ports          |                                              |
   +----------------------------------------------+----------------------------------------------+
   | 4: Dual USB 3.0 ports                        | 11: Asterisk slot: Fibre Channel or          |
   |                                              | additional networking                        |
   +----------------------------------------------+----------------------------------------------+
   | 5: 10Gb Ethernet port                        | 12: Storage controller management port       |
   +----------------------------------------------+----------------------------------------------+
   | 6: 10Gb Ethernet port                        | 13: NVMe activity indicators                 |
   +----------------------------------------------+----------------------------------------------+
   | 7: VGA monitor port                                                                         |
   +---------------------------------------------------------------------------------------------+


**M-Series systems with only a single storage controller must be shut
down and powered off before removing the controller, or data stored
in the NVDIMM SLOG will be lost! Dual storage controller systems
synchronize data between each NVDIMM, but can lose data if both
controllers are removed before being properly shut down.**

For remote management with IPMI, the 1 Gb Ethernet Out of Band
management port (#3) must be connected to a network.


.. raw:: latex

   \newpage


#include snippets/es24m_rails.rst


.. raw:: latex

   \newpage


#include snippets/es24m_drivetrays.rst


Connect Expansion Shelves
~~~~~~~~~~~~~~~~~~~~~~~~~

Refer to the installation instructions included with expansion
shelves for details on connecting them.


Connect Network Cables
~~~~~~~~~~~~~~~~~~~~~~

Note: Network cables vary by configuration and are not included.
Please contact :ref:`iX Support <Contacting iXsystems>` with any
questions.

Connect network cables to the Ethernet ports and Out-of-Band (OOB)
management port before attempting to power on and configure the
M-Series for the the first time.


Connect Power Cords
~~~~~~~~~~~~~~~~~~~

**Do not plug the power cords into a power outlet yet.**
Connect a power cord to the back of one power supply. Place the cord
into the plastic clamp and press the tab into the latch to lock it in
place. Repeat the process for the second power supply and cord.

.. _power_cord_connection:

.. figure:: images/tn_m_powerclip.png
  :width: 35%


After both power cords have been connected to the M-Series, they can
be plugged into power outlets. The system is configured to
automatically power on when connected to a power outlet. This design
ensures that the M-Series comes back on when power is restored after a
power failure.


Install Bezel (Optional)
~~~~~~~~~~~~~~~~~~~~~~~~

The included bezel is not required for operation.


Perform %brand% Initial Software Configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The console displays the IP address of the %brand% M-Series graphical
web interface, *192.168.100.231* in this example:


.. code-block:: none

   The web user interface is at:

   http://192.168.100.231


Enter the IP address into a browser on a computer on the same network
to access the web user interface.

.. _User Guide:

User Guide
~~~~~~~~~~

#include snippets/userguide.rst
