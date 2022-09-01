###############################################################################

sphinx-mad-domain

###############################################################################

A sphinx mad domain derived from the sphinx lua domain by boolangery


Installation
===============================================================================

Download the .py file and place in _ext folder


Sphinx integration
===============================================================================

Add the following to your conf.py:

extensions = ['sphinx-mad-domain']



Available sphinx directives
===============================================================================

The following directives are available:


Documenting class
-------------------------------------------------------------------------------

    .. mad:class:: pl.List

        Python-style list class.

        .. mad:attribute:: size: number

            The list size.

        .. mad:method:: append(elem)

            :param elem: The element to append
            :type elem: any

        .. mad:staticmethod:: fromArray(a): pl.List

            Create a List from a raw array.

            :return: The new List
            :rtype: pl.List


Class handle inheritance:

    .. mad:class:: ITransport

        .. mad:method:: startEngine(): boolean
            :virtual:

            :return: true if engine started
            :rtype: boolean

    .. mad:class:: Car: ITransport

        .. mad:method:: startEngine(): boolean

            :return: true if engine started
            :rtype: boolean


Method modifiers
-------------------------------------------------------------------------------

    .. mad:method:: foo()
        :virtual:
        :abstract:
        :deprecated:
        :protected:

        Show method modifiers.

Documenting module
-------------------------------------------------------------------------------

    .. mad:module:: pl.path

    .. mad:function:: join(p1, p2)

        Return the path resulting from combining the individual paths.

        :param p1: First path
        :type p1: str
        :param p2: An other path
        :type p2: str
        :return: The combined path
        :rtype: str


Type alias
-------------------------------------------------------------------------------


    .. mad:alias:: Packet = table<string, number>

       A packet.


    .. mad:class:: MessageSender

        A message sender.

        .. mad:method:: send(packet)
            :abstract:

            An abstract method.

            :param packet: the packet to send
            :type packet: Packet


Cross-references
-------------------------------------------------------------------------------

    :mad:class:`pl.List`

    :mad:meth:`pl.List.append`
