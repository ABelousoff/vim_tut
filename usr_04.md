*usr_04.txt*	��� Vim version 6.3.  ��������� ���������: 2004 Jan 17

		����������� ������������ VIM - ���� ���������

			 �������� ��������� ���������


��� ����� ������������� ��������� ����� �������� ��������� � �����������
������ ������ ������. ��� ������� ��� �������� �������� ��������� ������:
���������� � �������������, ����������� ������ � ��������� ��������.

|04.1|	��������� � �����������
|04.2|	��������� ������
|04.3|	���������� ���������
|04.4|	���������� �����
|04.5|	����������� ������
|04.6|	����������� ������
|04.7|	������������� ������ ������
|04.8|	��������� �������
|04.9|	����� ������
|04.10|	������

 ��������� �����: |usr_05.txt|  ���������
���������� �����: |usr_03.txt|  ��������� �� ���������
      ����������: |usr_toc.txt|

==============================================================================
*04.1*	��������� � �����������

� ����� 2 �� ���������, ��� ������� "x" ������� ��������� ������, �
������������� �������� ��������� ��������� ������� ��������� ��������: "4x"
������� ������ �������.
   ������� "dw" ������� �����. �� �������, ��� ������� "w" ��� �������
����������� �� �����. �� ����� ����, ������� "d" ����� ���������� � �����
�������� �����������, ��������� �������� ������ �� ������� ������� �� ����
�����, � �������� ������������ ������.
   ���, ������� "3w" ���������� ������ �� ��� �����, � ������� d3w �������
��� �����.

	����������� ������ ���� ����������� ���� (������� � �������) ~
			   ----------------------> 
			             d3w
		    
	����������� ������ (������� � �������) ~
   
Vim ���������� �������� ������ �� �������, � ������� ����������� ������. ���
���������� ������, ��� Vim ����� � ���, ��� �� ������ ����� �� ������ �������
������ ������ �����. ���� �� ����������� "e" ��� ����������� � ����� �����, ��
Vim ��������, ��� �� ������ �������� � ��� ����� � ��������� ������:

	����������� ������ ���� ����������� ���� (������� � �������) ~
			  ---------------->
			        d2e

	����������� ������ ���� (������� � �������) ~
	

���������� ��� ��� ������ ��� �������� � �������� �������� ������� �� �������.
���������� �� Vim �������� ������� ����������� "���������������", ���� ������
��� �������� �� ���������� � �������� ��������, � "��������������", ����
������ ���������� � ��������.

������� "$" ���������� ������ � ����� ������. ������� "d$" ������� �����,
������� � ������� ������� � �� ����� ������. ��� ����������� ��������
�������������, ������� ��������� ������ ����� ����� �����:

	����������� ������ ���� ����������� ���� (������� � �������) ~
	                                        ------------------->
						         d$

	����������� ������ ���� ����������� ���� ~
					         	
������ ���� �������� �������� ��������� �������: ��������-�����������. �������
�� ��������� ������� ���������, �������� "d" ��� �������� ��������. ����� ��
������� ������� �����������, �������� "4l" ��� "w". ����� ������� �� ������
�������� � ����� ���������� ������.

==============================================================================
*04.2*	��������� ������

������ ���������� �������� ������� "c" (change, ��������). ��� �������� �����
��� ��, ��� � �������� "d", �� ��������� �������� � ����� �������. ��������,
"cw" �������� �����. ������ ������, ��� ������� ������� ����� � ���������
�������� � ����� �������.

	����������� ������ ���� ����������� ���� ~
	                   ----------------->
			    c2w����� ���<Esc>

	����������� ������ ����� ��� ���� ~

������� "c2w����� ���<Esc>" ������� �� ��������� ������:

	c	    �������� ���������
	2w	    ����������� �� ��� �����, ������� ��������� � ��������
		    ��������� � ����� �������.
	����� ���   �������� ���� �����
	<Esc>	    ������� � ������� �����

��, ��������, �������� ��������, ��� ������ ����� ������ "����" �� ��� �����.
�������, ��� ��� ������ �������� ���� �������, ������� ������������ �������,
���������� � ������������. �� �� ����� ������� � � ������� � �������� "cw".
�������� c �������� ����� ��� ��, ��� � �������� d, � ����� �����������: "cw".
����������, �� �������� � ������ ������ ��� "ce", ��������� �� ����� �����.
����� �������, ������ ����� ����� �� ����������. ��� ���������� ������������
��� � Vi. ��������� ������ ���� �������� � ������ ���������, ��� ����������� �
� Vim.


������ ���������

������� ���� ��� "dd" ������� ����� ������, "cc" �������� ����� ��� ������
�������. ��� �� �����, "cc" ��������� ������������ ������ (��������� �������). 

��� ��, ��� "d$" ������� ����� �� ����� ������, "c$" �������� ����� �� �������
�� ����� ������ -- �� ����� ��� ������� ����� ��� ������ "d$" � ����� ������
������� "a" ��� �������� � ����� ������� � ���������� ������ ������.


�����٨���� ��������

��������� �������, ����������� � ������� ��������-�����������, �������������
��������� �����, ��� �� ���� ������������ ������������� �������:

	x  ������������ ���  dl	 (������� ������ ��� ��������)
	X  ������������ ���  dh	 (������� ������ ����� �� �������)
	D  ������������ ���  d$	 (������� �� ����� ������)
	C  ������������ ���  c$	 (�������� �� ����� ������)
	s  ������������ ���  cl	 (�������� ���� ������)
	S  ������������ ���  cc	 (�������� ��� ������)
	

��� �������� �����

������� "3dw" � "d3w" ������� ��� �����. ���� ��� ��������� �����������, �� ��
����� ���� ������ �������, "3dw", ������� �� ������ ����� ��� ����; �������
"d3w" ������� ��� ����� ���� ���. ��� �������� �� ����� � ����� ��������
�������. ������, �� ������ ��������� � ������� ��� �����. ��������, "3d2w"
������� �� ��� ����� ��� ����, ����� ����� ����. 


������ ������ �������

������� "r" �� �������� ����������. ��� ������� �� ��� ����� ������� �
�������� �� ���� ������ ������, ����������� ��� ��������. ���� �� �������
����� �������� ��� ������ ������� "cl" ��� "s", �� "r" �� ������� ����� <Esc>

	���� ���-�� ��� ����-��, ������ ���-�� ���-�� ���� ~
	r�	           r�    r�

	���� ���-�� ��� ����-��, ������ ���-�� ���-�� ���� ~
	
������������� �������� ��������� � �������� "r" �������� ������ ����������
���������� �������� �� ���� � ��� �� ������ ������. ��������:

	���� ���-�� ��� ����-��, ������ ���-�� ���-�� ���� ~
	                7r�

	���� ���-�� ��� �������, ������ ���-�� ���-�� ���� ~

��� ������ ������� �� ������� ������ ����������� "r<Enter>". ��� ��������
������� ���� ������ � ��������� ������� ������. ������������� ����� � ����
������ ������ ������ �� ���������� �������� ��������: "4r<Enter>" ��������
������ ������� �� ���� ������� ������.

==============================================================================
*04.3*	���������� ���������

������� "." -- ���� �� ����� �������, �, � �� �� �����, ����� ������ ������ �
Vim. ��� ��������� ��������� ���������. ��������, �����������, ��� ��
������������ ���� HTML � ������ ������� ��� ���� <B>. ��� ����� �� ���������
������ �� ������ < � �������� <B> �������� "df>". ����� �� ���������� � < 
���������� </B> � �������� ��� �������� ".". ������� "." ��������� ���������
������� ���������, � ����� ������ "df>". ��� �������� ���������� ���� ��
������ �������� ������ � ������� < � ���������� ������� ".".

			      
			      ������ <B>��������</B> ���� ���, ��� <B>�� ~
			    
	f<   ����� ������ <   ------->
	df>  ������� �� >	     -->
	f<   ����� ����. <	       --------->
	.    ��������� df>			--->
	f<   ����� ����. <		           ---------------->
	.    ��������� df>					   -->

������� "." �������� ��� ���� ���������, ����� ������� ������ "u", ����������
���������� ���������� ������� CTRL-R, � ������, ������� ���������� � ���������
(:).

������� ��� ���� ������: �������� ��� ���� �������� ����� "������" �� �����
"����" �����, ��� ��� ���������� � ������. ��� ����� ���������� ������
��������� ��������� ������ ������:

	/������<Enter>	����� ������ ����� "������"
	cw����<Esc>	�������� ��� �� "����"
	n		����� ��������� ����� "������"
	.		��������� ������ ����� �� "����"
	n		����� ��������� "������"
	.		��������� ������
			� �.�.

==============================================================================
*04.4*	���������� �����

��� �������� ������� ���������� ������� ���� "��������-�����������" ��������
�������, �� ������ ������ �� ������ ����������, ��� ������ ������� �����
������������ �� ������. � ���� ������ �� ������ �������� ���������� �����.

������� � ���������� ����� �������������� �� ������� "v". � ���������� ������
�� ����������� ������ �� ������, ��� ������� ������ ��������� �������� -- ��
����� ����� �������� ���������� �������� ������ ����� ��������������. �����
��������� ������� ���������.
   ��������, ��� �������� ������ � �������� ������ ����� �� �������� �������
�����:

		������� -- ��� ��� �� �������� ~
		      -------------------->
                          veeeelllllld
		      
		��������� ~

��� ���� ��� ������������� ����� ���� -- ������� ��� ���� ������ "l", �����
������ �������� � ����������� �������. �� ��������� ������ �����, �������
����� �����.

���� � �����-���� ������ �� ������, ��� � ���������� ������ �� ���� ������, ��
������ ������� <Esc> ��� ������ �� ����������� ������.


��������� �����

���� ��� ���������� �������� � ������ ��������, �� ����������� ��� �������� �
���������� ����� ������� "V". �� �������, ��� ������� ������ ����� ����� ��
��������. ����������� ������ ��� ����� �� �������� �� � ����� ����������, ����
����������� ����� ��� ���� ��������� ������� ��������� �� ���� ������ �� ���.
   ��������, ��� ��������� ��� ����� ����� ������ "Vjj":

			  +------------------------+
			  | ����� ����� �����      |
		       >> | ����� ����� ����� ���� | |
     ���������� ������ >> | ����� ����� �����      | | Vjj
		       >> | ����� �����            | V
			  | ����� ����� �����      |
			  +------------------------+


��������� ������

���� �� ������ �������� ��� ������������� �������� ������, �� ����������� ���
�������� � ���������� ����� CTRL-V. ���������� ����� ����� ������� ��� ������
� ���������.

		���    		Q1	Q2	Q3
		����  		123	455	234
		����		0	90	39
		���� 		392	63	334

����� ������� ������� ������� "Q2", ��������� ������ � "Q" � ������� CTRL-V
��� �������� � ����� ����������� �����. ����� ����������� ������ �� ��� ������
����, �������� �������� "3j", � ������ � ���������� �����, �������� "w".
��������� ��������� ����� �������� ������ ������ ��������� �������, ��������
������ ����� �� ���� ������� �������� "h". ������ ������� "d" � �������
������� ��������.


������� �� ������ ������� ���������

������ � �������� ��������� ������ � ���������� ������, �� ���������, ���
������ ��, ����� ������ ��������� � ������ ������� ���������� �������. ���
����������� ������� �� ������ �������, ����������� �������� "o" (other,
������). ������ ������������� � ������ ������� ��������� � �� �������
��������� ������� ��������� � ������ �������. ��������� ������� "o" ���������
������ � ������ �������. 

��� �������� ��������� � ������� ��������� ������ ����. ������� "o" ����������
������ �� ���������, � "O" ���������� ������ � ������� ���� � ��� �� ������.

���������: "o" � "O" � ���������� ������ �������� ������ �� ���, ��� � �������
������, ��� ��� ��������� ����� ������ ����� ��� ������ �� �������.

==============================================================================
*04.5*	����������� ������

��� �������� ������, �������� � ������� ������ "d" ��� "x", �������� �����
����������� � ������. ��� ������ ������� p (put, ���������) ��� ����� �������
� ����� ������ �����.
   ���������, ��� ��� ��������. ������ �����, ������ ����� ������, ��������
�� ��� ������ � ����� ������� "dd". ������, ���������� ������ ����, ��� ��
������ �� ������� ������ � ������� ������� "p". �������� ����� ����� �������
��� ��������.

	������		������	      ������
	������ 2  dd	������ 3  p   ������ 3
	������ 3	    	      ������ 2

��������� �� ������� ����� ������, ������� "p" ��������� ������ � ������� ����
�������. ���� �� ������� ����� ������ (��������, �����), �� ������� "p" ������
��� ����� ����� �������.

	�� ������� ����� �� ������� ~
           -------->
	      dw
	      
	�� ����� �� ������� ~
           ----->
	    whp

	�� ����� ������� �� ������� ~
	

�٨ � ������� ������

������� "P" ����� ��������� �����, �� ����� ��������. ���� �� ������� ������
�������� "dd", �� "P" ������ ������ ��� ��������. ����� �������� ����� ���
������ ������� "dw", "P" ��������� ��� ����� ����� ��������.

�� ������ ��������� ������� ������� ���, ������� ���������. ��� ���� �����
�������������� ���� � ��� �� �����. 

� ��������� "p" � "P" ����� ������������ �������� ���������. ����� �����
����������� ������� ���, ������� ��������� �����. ����� �������, "dd3p"
�������� ����� �� ������� ��� ����� �������� ������.



�������� ������� ��� �������

����� �� ����� ������ ��������� ��������, ��� ������� ��� ������� �����������
��������������� �������. Vim ��������� ����� ���������� ����� ������ -- ������
��������� ������ � ������� ������� � ��������� ������� "xp". ��� ����
���������� ���������: "x" ������� ������ � �������� ��� � �������, � "p"
��������� ����� ����� �������.

	��������   �������   �������� ~
	  x          p

==============================================================================
*04.6*	����������� ������

����� ����������� ����� �� ������ ����� � ������ ����� ���� �� ������� ���,
��������������� �������� "u" ��� ��������������, � ����� ������� ��� � ������
����� ��� ������ ������� "p". ���������� ����� ������� ������ ��������� ������
�������� ������. �������� "y" �������� ����� � �������. ����� ����� �����
������������ �������� "p" � ������� �������.
   Vim �������� ��� �������� "yanking". ���� � ���, ��� ����� "c" ���
������������ ��� ��������� ���������, ������� ��� �������� �����������
��������� ������ ���, ����������� �� ������ � ��������������� ��������� ���
���� ������� ������. (��, ��� �� ������ ����������� ����� ��������).

��������� "y" �������� ����������, �� ����� ������������ ����� �������, ���
�������� "yw" ��� ����������� �����. ������� ��, ����� ����������� � ��������
���������. ��� ����, ����� ����������� ��� �����, ����� ������������ "y2w".
������:

	let sqr = LongVariable * ~
		 -------------->
		       y2w

	let sqr = LongVariable * ~
			       p

	let sqr = LongVariable * LongVariable ~

�������� ��������, ��� "yw" �������� ������ ����� �����. ���� ��� ��� ��
����������, �� ����������� "ye".

������� "yy" �������� ��� ������ �������, ������� ���� ��� ������� "dd"
������� ��� ������. ����������� ��������� ����������� � ���, ��� "Y" ��������
����� ��� ��, ��� � "yy", �� ���� �������� ��� ������ �������, � �� ����� ���
"D" ������� ����� �� ������� �� ����� ������. ������ �����������, ���
����������� ������ �� ������� �� ����� ������ ����������� �������� "y$".

	������ ������      yy	������ ������          ������ ������
	������ 2   	        ������ 2	   p   ������ 2
	��������� ������	��������� ������       ������ ������
						       ��������� ������

==============================================================================
*04.7*	������������� ������ ������

��� ������������� ������ Vim � ����������� ����������� (gvim), � ����
"�������������" ����� ���������� �������� "����������". ��� �������������
���������� ������� ����� � ���������� ������, � ����� ������������ ����
�������������/���������� ��� ����������� ������ � ��������� ����� ������.
������������� ����� ����� ��������� � ������ ���������, � ��� ����� � ��� Vim.

�����, ������������� � ����� ������ � ����� ����������, ����� ��������� ���
������ ���� �������������/�������� ��� � ������� ������, ��� � � ������
�������. � ���������� ������ ����������� ����� ����� �������� ����������
�����.

��� ������ ���� "��������" ����� ����� ����� �� ����� ����� ��������� � �����
������. ���� � ����� ������� ���� ����������� ����, �� "����������",
"��������" � "��������" ����� �������� � �� ����������� ����. ����� ����,
��������������� ������ ����� ����� �� ������ ������������, ���� � Vim ����
������ ������������.

���� �� �� ����������� ������ � ����������� �����������, ��� �� ������
������������ ����, �� ��� ���������� ��� �� �������� ����� ������������ �
������������� ���������. ��� ����� ���� ��������������� �������� ��������� "y"
� "p", �� � ����������� ��������� "* (������� ������� ��������). ��������,
����� ����������� � ��������� ����� ������ ������� ������, ����������� >

	"*yy

� ��� ������� ������ �� ���������� ������ ����������� >

	"*p

��� �������� ������ �� ������� Vim, � ������� ���� ��������� ���������� ������
������. ��������� �� ���� ������� � ������� |09.3| � �����: |�����_������|.

==============================================================================
*04.8*	��������� �������

���� ������ ��������� � �������� �����, ������� �� ������ �������, �� ������
��� ��������� ������� "dw" ������� ����������� ������ � ������ ����� �����.
������� ����� �������� ���� �� ������� �������� "daw".

	�������� - ������ ������ ����������������� ����� ~
		     daw

	�������� - ������ ����������������� ����� ~
	
"d" � "daw" ��� �������� ��������. "aw" ("A Word", �����) ��� ���������
������. ����� �������, "daw" �������� "������� �����". ������ ������, ������
����� ����� ����� ����� ����� (������ ����� ������ "������").

������������� ��������� �������� �������� ������� �������� �������� ���������
� Vim, � ���������� � ��� ��������� "��������� � ������������" � �����������
������.
   ��������� ������� ����� ������ �� ��������� � ������������, ��, ������
���������� �������� ��� ���������� ������ ����� ������� � �����������
�������� �������, ��������� ������ ��������������� ��� �����. ���������
������� ������ ������� �� ����� ��������.

��� ��������� ������ ����������� ����������� �������� "cis". ���������� ��
��������� �����:

	��� ����, � �� ������ ��� ������������-����������. ���� ���� ~
	������ �������� ������������, ��� ������. � ����� �������� ~
	����������. ���� ������ ���� ��� ��������: �������, ������� � ~
    
�������� ������ � ������ ������ ������ � ����� ������� "cis":


	��� ����, � �� ������ ��� ������������-����������.  � ����� �������� ~
	����������. ���� ������ ���� ��� ��������: �������, ������� � ~

������ ����� ���������� ����� ��������� �� ����� ������� �����������. ������
�� ������ �������� �� ��� ����� ����� ������ �����������.
	
"cis" ������� �� ������� ��������� "c" � ���������� ������� "is" (Inner
Sentence, ���������� �����������). ����� ������� ������ "as" (a sentence,
�����������). �������� ����� ����� ����� ����������� � ���, ��� "as" ��������
������ ����� �����������, � "is" �� ��������. ���� �� �� �������� �������
������ � ������������ � ������ ����� ����, �� ����� ���� �� ������������
������� "das". ���� �� ������ �� ����� ������� ����������� ���������� ����
����� � ��������� ������� ����� �����������, �� ����������� ������� "cis".

��������� ������� ����� ������������ � � ���������� ������. � ���� ������
��������� ������ ����� ������� � ���������. ���������� ����� �� ����� �������,
������� ����� ����� ��������� ��� ��������� ���. ��������, ������� �
���������� �����, ���������� ������� ����������� ��� ������ "as". ���
��������� � ��������� ����� ����������� ����� ��������� "as" �� ��� ���, ����
�� ����� �������� ��� �������, ��� ������� �� ������ �������� ��������.

������ ��������� �������� ����� ����� �����: |���������_�������|.

==============================================================================
*04.9*	����� ������

������� "R" ��������� Vim � ����� ������. � ���� ������ �������, ������� ��
���������, �������� �������, ������������� ��� ��������. ��� ������������ ��
��� ���, ���� �� �� ������ <Esc>.
   ������� ������:

	������� � �������� ���� ~
			   R������<Esc>
	
	������� � �������� ������ ~

�������� ��������, ��� � ���� ������� ������� �������� ������ ������� �� �����
������. ������� "R" ������������� ��������� ������, ���� ������������� �������
��� ������. ������� "R" �� ��������� ����� �� ��������� ������.

����� �������� ������� � ������ ����� ������������� ������� <Insert>.

���� � ������ ������ �� �������������� ������� <BS>, �� �������� ��������, ���
������ ����� �����������������. ����� �������, �� �������� ������ �������
������ ��� ���������� ���������� �������.

==============================================================================
*04.10*	������

���������, ������� ����������� � ��������� ������� ������������� ���
����������� ��� ��������� ����������. ���� �� ������ ��� �� ��� ��������, ��
������� ������������ N ���������� � M ������ ����������� ��� ������ N * M
������!

������ ���������� ����� ����� �����:  |��������|

��������, ��� �������� ���������� ������ ���������� ��������� ��������. ���
���� ��������� �������� �����������:

x	������� ������ ��� �������� (���������� ��� "dl")
X	������� ������ ����� �������� (���������� ��� "dh")
D	������� ����� �� ������� �� ����� ������ (���������� ��� "d$")
dw	������� ����� �� ������� �� ������ ���������� �����
db	������� ����� �� ������� �� ������ ����������� �����
diw	������� ����� ��� �������� (�������� ������)        
daw	������� ����� ��� �������� (������� ������)         
dG	������� �� ����� �����          
dgg	������� ����� �� ������� �� ������ �����

���� ������ "d" ������������ "c", �� �� �������� ��������������� �������
������, � � "y" � ��� ����� ����� ������ ��� �������, � �.�.

	~	�������� ������� ������� ��� �������� � ����������� ������ �
		���������� �������. ��� �� �������� (���� ������ �� ��������
		����� 'tildeop'), ������� �� �� ������ ������������ � �������
		������� �����������. ������ ����� �������� � ����������
		������, ��� �������� ������� ���� ���������� ��������.

	I	������� � ����� ������� ����� ����������� � �������
		����������� ������� ������.

	A	������� � ����� ������� ����� ����������� ������� � ����� ������.

==============================================================================

��������� �����: |usr_05.txt|  ���������
��������� �����: ��. |���������_�����_��_������������|  

vim:tw=78:ts=8:ft=help:norl:
