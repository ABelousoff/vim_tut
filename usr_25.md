*usr_25.txt*	��� Vim version 6.3.  ��������� ���������: 2003 Jun 21

		����������� ������������ VIM - ���� ���������

		    �������������� ���������������� ������


����� ����� ������ ������ ���, ��� ������ ������ ������������� ����
�����������. ��� ����� ��������� �������� ����������� � ������� ��������������
������, ��� ������� ����� ��������� �� ������. � Vim ����� ���� ��������
����������� ��� �������������� �������, ��������� �� ����� ������, � ������.

|25.1|	������� �����
|25.2|	������������ ������
|25.3|	������� � ���������
|25.4|	������ � �������� ��������
|25.5|	�������������� ������

 ��������� �����: |usr_26.txt|  ���������� ������������� ��������
���������� �����: |usr_24.txt|	������� �������
      ����������: |usr_toc.txt|

==============================================================================
*25.1*	������� �����

� Vim ������� ����� ����� �������, ����������� ������ � �������. �� ���������,
�������� �� ��������� ������ �������������. ������� �������, ��� ��������
����� ��� ���������� �������� <Enter>. ��� ������� ��� ��������� ��������,
����� ��� ������ ���� ������, ��� ������������� ���� ������ � ��� ����������
������. �� ���� �� ������� ������������, �� ����� ��������� �������, �����
����� �� ������ ��� �������� 70 ��������.
   ���� �� ���������� �������� ����� 'textwidth' �������� �� ����, �� Vim
����� ������������� ���������� ������, ������� ������� �������� ���� �����.
�����������, ��� �� ������ ������� ����� �������, ������� � 30 ��������.
������ ����� �������� ��������� �������: >

	 :set textwidth=30

������ ������ ����� ������ (� ������� ����� �������� �������):

	         1         2         3
	12345678901234567890123456789012345
	�� �������� ���� ����� �� ���� ~

����� �� ��������� ��������� �����, "�", �� ������ ���������� �������, ���
30 ��������. Vim  ��������� ������� ������ � �� ������ ���������:

		 1	   2	     3
	12345678901234567890123456789012345
	�� �������� ���� ����� �� ~
	����� ~

��������� ����� ������� �� ������ ������� ���� �����:

		 1	   2	     3
	12345678901234567890123456789012345
	�� �������� ���� ����� �� ~
	���������� ����. ������� ��� ~
	����� ������� � ����� ��� ~
	���������� � ���� ������. �  ~
	����� �� �� �������� ������ �� ~
	������ ���������, � � � ~
	����������� ��� ��������� ~
	����� ���. ~

�� ��� �� ��������� ���������� ������ -- Vim �� ������ �������������.

	���������:
	����� 'wrap' ��������� ��������� Vim ���������� ������� ������ �
	����������, �� ��� ���� �������� �� ����� ��������� � �����.


��������� ��������������

� ��������� Vim �������� ����� �� ����� ������������� �����������������, ����
�� ���������� ��� �������� ��������� ����� � ������. ���� �� ������� �� ������
������ ����� "���� �����", �� �������� ������� �������� ������:

		 1	   2	     3
	12345678901234567890123456789012345
	�� �������� �� ~
	���������� ����. ������� ��� ~
	����� ������� � ����� ��� ~
	���������� � ���� ������. �  ~
	����� �� �� �������� ������ �� ~
	������ ���������, � � � ~
	����������� ��� ��������� ~
	����� ���. ~
	
����� ����� �������� ����� ��� ����������, ����������� �������-�������� "gq".
��������� ������������ ��� ����� ���������� ���������. 
   ������� � ������ ������, ��������: >

	v7jgq

"v" ��������� � ���������� �����, "7j" ���������� ������ � ����� ������, �
����� �� ���������� �������� "gq", ������� ����������� � ���������� �������.
��������� �������� ���:

		 1	   2	     3
	12345678901234567890123456789012345
	�� �������� �� ���������� ~
	����. ������� ��� ����� ~
	������� � ����� ��� ���������� ~
	� ���� ������. � ����� �� �� ~
	�������� ������ �� ������ ~
	���������, � � � ����������� ~
	��� ��������� ����� ���. ~

���������: ��������� ���� ������ ��������� ��������� ��������������
��������������, ��. |������������������|.

��������� "gq" �������� ����������, �� �� ������ ������������ ����� �� ���
�������� ������ ��������� ������, ��� ������� �� ����� ��������: ����������
�����, ����������� ������� ��� ��������� ������.
   ��� �� ����� ����������� ����� ���� �� ������� � �������� "gq7j". ���
����������� �� ������ ������� �� ������, �� �� ��� ��������� �����, �� �������
������ ����� ����� ����������� ������. ����� ��������, � ������ ������,
������� �����������: "}". ��� ������� ��������� ����������� ������ � �����
������. ����� �������, ������� "gq}" �������� �������������� ������ �� �������
������� ������� �� ����� �������� ������. 
   ��� ������������� � �������� "gq" ����� ������� ����� ��������� ������
"�����". ���������� ������ �������: >

	gqap

"ap" ��� "�����", "a-paragraph". ��� ������� ����������� ����� �� ��� �������
������. ������ � ������ ����������� ������� ��������.
   ���� ������ � ����� ����� ��������� ���������, �� �� ������
����������������� ���� ���� �� �������: >

	gggqG

"gg" ���������� ������ � ������ ������, "gqG" ��������� �������������� ��
��������� ������. 
   ��������������: � ������, ���� ���� ������ �� ��������� ������� ��������,
��� ����� ��������� � ���� �����. � ������ ������, ����������� ������, ��
������ ���� ������� ��������, � ��� ����� �������� ��������� � ��������.

Vim ��������� ����� �������� ������ �� ������ � �������� ������. ��������� ��
���� �������� |fo-�������|. ����� ��. ������� �� ����� 'joinspaces', �������
��������� ����������� ���������� ��������, ������������ ����� �����. 
   ��� �������������� ����� ����� ������������ ������� ���������, ��� �����
���� ��������, ���� ���������� �������� Vim �� ��������� ���������
��������������� ��� �����. ��. ������� �� ����� 'formatprg'.

==============================================================================
*25.2*	������������ ������

��� ������������ ��������� ����� �� ������, ����������� ������� >

	:{��������}center [������]

� �������� {���������} ������� ������� ��� ��������� ������ �������� �����.
[������] �������� �������������� ����������, ����������� �� ������ ������,
������� ������� ������������ ��� ��������������, �� ��������� ��� �����
�������� 'textwidth'. (���� 'textwidth' ����� 0, �� [������] �� ���������
����������� ������ 80).
   ��������: >

	:1,8center 40

�������� � ���������� ����������:

       �� �������� ���� ����� �� ~
      ���������� ����. ������� ��� ~
       ����� ������� � ����� ��� ~
      ���������� � ���� ������. � ~
     ����� �� �� �������� ������ �� ~
	������ ���������, � � � ~
       ����������� ��� ��������� ~
	       ����� ���. ~


������������ �� ������� ����

������� ":right" ����������� ����� �� ������� ����: >

	:1,8right 30

� ����� ������ �������� � ������ ����������:

	     �� �������� ���� ����� �� ~
	  ���������� ����. ������� ��� ~
	     ����� ������� � ����� ��� ~
	   ���������� � ���� ������. � ~
	����� �� �� �������� ������ �� ~
	      ������ ���������, � � � ~
	     ����������� ��� ��������� ~
			    ����� ���. ~


������������ �� ������ ����

����� ����, ������� ����� �������  >

	:{��������}left [����]

� ������� �� :center" � ":right", ���������� ���� ������� �������� �� �����
������, � ����� ����. ���� ���� �� ���������, �� ����� ����� ������� � �����
����� ������� ����, ����� �������, �������� ���� �� ��������� �����������
������ 0. ���� ����, ��������, ��������� 5, �� ����� ����� �������� � ��������
� ���� ���������� ��������. ��������, ����� ��������� �������: >

	:1left 5
	:2,8left

� ���������� ������� ���������:
	     
	     �� �������� ���� ����� �� ~
	���������� ����. ������� ��� ~
	����� ������� � ����� ��� ~
	���������� � ���� ������. � ~
	����� �� �� �������� ������ �� ~
	������ ���������, � � � ~
	����������� ��� ��������� ~
	����� ���. ~


������ �������� ������

� Vim ��� ���������� ������� ��� ���������� ������ �������� ������ (�.�.
������������ ������ ������ ����� � ������). ������, ���������� ��������
������, ������� ������� ����������� � ���� �������. ��� ������������� �������
���� ��������� ������� >

	:runtime macros/justify.vim

���� �������� Vim ���������� ����� ���������� �������: "_j". ��� ������������
������ �� ����� �����, ��������� �������� ����� � ���������� ������ �
��������� ������� "_j".
   ����� �������� �� ���� ������� ����� ���������� � ����� ����� ��������.
��������� ������� "gf" �� ����� �����: $VIMRUNTIME/macros/justify.vim.

�������������� ��������� ����� ���� ������������� ������� �������-�������,
��������: >

	:%!fmt

==============================================================================
*25.3*	������� � ���������

������� ����� ������������ ��� ��������� ������. ��������, ��� ������� �
������ ����������� ��������� � ��������� � 8 �������� ��� ����� ��������
���������. ��� ����� ������ ��������� ������ ������ ��������� � ������ ������
������. ��������, ��������, ��������� �����:

	������ ������ ~
	������ ������ ~

��� ����� ����� ������ ������������ ������� ������� ���������, ����� ����
������ ������, <Enter>, ���������, ���� ��������� ������ ������ � �.�.
   ����� 'autoindent' ��������� ��������� ������� �������������: >

	:set autoindent

������ ����� ������ ��� ���� ������������� �������� � ��� �� ��������, ��� �
����������. � ���������� ���� �������, ������� ������� ��������� ����� �����
<Enter> ������ �� �����������.


���������� �������

��� ���������� �������, ����������� �������� ">". ����� ����� ������������
������� ">>", ������� ����������� ������ � ������� ������.
   ���������� ��������, ����������� � ������ ������, ������������ ���������
����� 'shiftwidth'. �� ��������� ��� �������� ����� 8. ��� ����, ����� �������
">>" ������ ������� �� 4 �������, ������� ������� >

	:set shiftwidth=4

�������� ������� ">>" �� ������ ������ ������ ������, �� �������:
    
	������ ������ ~
	    ������ ������ ~

"4>>" ��������� ��������� ������ � ������ ����� �����.


������ ���������

���� �� ������ ������� ������� �������� 4, �� ��� ����� ���� ����������
�������� ����� 'shiftwidth' ������ 4. ������, ������� ������ ��������� ��
�������� ����� ��������� � ��������� ������� ������� � 8 ��������. ���
��������� ����� ��������, ����������� ������ 'softtabstop': >

	:set softtabstop=4

������ ������� �� ������ <Tab> ����� ��������� � ������� 4 ��������. ����
����� ���� ��� ������� 4 �������, �� ����� �������� ������ <Tab>, ���
��������� ������� ������ ����� �� 7 ������ ������. ���� ��� �������, ����� ���
������� ��������� ������ ���������� �� �������, �� �������� ����� 'expandtab'.

	���������:
	�� ������ ����� ���������� �������� ����� 'tabstop' ������ 4, �� ����
	������� �� ������ ������������� ���� ���� �� ��������� ����� 'tabstop'
	������ 8, �� ���� ����� ��������� �� ���, ��� �� ��������. ����� ����,
	������� ����� ��������� ����������� ��� ������ � � ������ ����������.
	�������, ������������� ������ ������������� �������� ����� 'tabstop'
	������ 8, ��������� ��� �������� �������� �����������.


��������� ���������

�� ������������ ����, � ������� �������������� �������� ����� 'tabstop',
������ 3. �� ����������� ����������� ��������� ���� �����, 8, � ������� ���� �
��������� �������� ����������. ����� ���� �� ��������� ���������, ��������
��������� �������� ����� 'tabstop' ������ 3, �� ��� �������� �� ������ ������
���, ����� �� ������������ ���� ����.
   Vim ����� �������� �������� ������ ���������, ������������ � �����. ������
����� ���������� �������� 'tabstop', ����� ����������� ������� ":retab": >

	:set tabstop=3
	:retab 8

������� ":retab" ������� �������� 'tabstop' � 8, ������� �������
�������������� ������ ��������������� �������. ��� �������� ���� ����������
��������, ��������� ����������� ��������� �������� ��������� � ��������. �����
���������� ���� �������� ����� ��������� ����, ����� ��� �������������� �
��������� ��� ��� ������� ���� �� �����.
   ��������������: ��� ������������� ������� ":retab" � ������ ���������
�������� ��������, ��� ������� ���������� �������� ����� ������� � ���������
���������. �������, ������ ���������� ������� � ��������� ���������� �����
������������ "\t".

==============================================================================
*25.4*	������ � �������� ��������

������ ��� ������� ����������� � ���������, ����� �� ������������ ����, �
������� ������ �������, ��� ���������� ������� � ����. Vim ����� ����������
������, ����� ��� ��������� � ����.
   ���� �� ��������� ����� 'wrap', �� ������ ������������ �� �����. ���������
������� ����� ����� �������� �� ������ �������� ����.
   ��� ����������� ������� � �������, ������� �� ����� �� ������, Vim �����
������������ ����� �� �����������. ��� ������ �� ����������� ����, �����
������� �� �������������� �����, � ����������� �����������.
   �� ���������, Vim �� ���������� �������������� ������ ��������� �
����������� ����������. ��� ��������� �������������� ������ ��������� �
����������� ����������, ����������� �������: >

	:set guioptions+=b

������ �� ������ ������������ �������������� ������ ���������.

���� � ��� ��� ������ ���������, ��� �� �� ������ � ������������, �� ���
��������� ������ �� ����������� ����� ������������ ���������� ���������. ���
���� ������ ����� ���������� �� ��� �� ����� ����� ������, �� ����� ���
�������� ����� �������������� �� ���� �������������.

	zh		��������� ������
	4zh		��������� �� ������ ������� ������
	zH		��������� ������ �� �������� ������ ������
	ze		��������� ������ �� ��������� �������
	zl		��������� �����
	4zl		��������� �� ������ ������� �����
	zL		��������� ����� �� �������� ������ ������
	zs		��������� ����� �� ��������� �������

���������� ��������, ��� ��� �������� �� �������. ������ ��������� �� �����
"�" ����� "��������". "������� ����" ��� ������� ���������� �����, �������
����� � ���� � ������ ������. "����" ��� ������� ���������� �����, �������
����� ����� � ���� ����� ���������� ��������������� �������, ��������� �����.

			      |<--  ������� ����  -->|
		������� ������ ������, �������� ����������� � ���� ~
	ze	  |<--	   ����      -->|
	zH	   |<--      ����     -->|
	4zh		  |<--	    ����      -->|
	zh		     |<--      ���� 	 -->|
	zl		       |<--	 ���� 	   -->|
	4zl			  |<--	    ����      -->|
	zL				|<--	  ����      -->|
	zs			       |<--	 ���� 	   -->|


����������� � ����������� ��������� �����

����������� ����� �� ����������� ��� ����������� ����� 'wrap', �����
������������ ��������� ������� ��� ����������� ������� � ������ �� �������� ��
������. ��� ������������� ���� ������, �����, ������������� ����� � ������ ��
�������� � ����, ������������. ��� ������� �� �������� ��������� ������:

	g0		� ������� �������� ������� �� ������� ������
	g^		� ������� �������� ������������� ������� �� �������
			   ������
	gm		� �������� ������
	g$		� ���������� �������� ������� � ������� ������

		|<--	  ����     -->|
	������� ������ ������, �������� ����������� � ���� ~
		 g0  g^    gm	     g$


������� �� ������               *edit-no-break* *��������������-���_���������*

���� �� �������� ����� ��� ������������� � ������ ���������, �� ��� ��������
���������, ����� ������ �� ��������� ������ ��������� ������. ���
������������� ����� 'nowrap' �� �� ������� ������ ����������� �������, � ���
���������� ����� 'wrap' ����� ����� ������������ � �������� �����, ���
��������� ������ ��� �������.
   ������� �������� ��� �������������� ������ ������ ����� ������������� �����
'linebreak'. Vim � ���� ������ ����� ���������� ����� ��� ��������� ������ �
���������� ������, ��������, �� ��������, � ����� � ����� ����� ��������� ���
���������.
   ��� ���������� ����� 'linebreak' ����� � ���� ����� ��������� ���:

	+---------------------------------+
	|���������� ������ �� Ը���� � ���|
	|������ ��� �� �������� ���. Ը���|
	|, �� �������, ������� ������ � ��|
	|�������. ������, ����������� ����|
	|, ��������� ���� -- ��� Ը���� � |
	+---------------------------------+

����� ���������� �������: >

	:set linebreak

����� ����� ��������� ��������� �������:

	+---------------------------------+
	|���������� ������ �� Ը���� �    |
	|��������� ��� �� �������� ���.   |
	|Ը���, �� �������, ������� ������|
	|� ���������. ������, ����������� |
	|����, ��������� ���� -- ���      |
	+---------------------------------+

������ �����:
'breakat' ����������� �������, �� ������� �������� ������� ������.
'showbreak' ���������� ������, ������� ������ ���� �������� � ������
����������� ������.
����� ������� ������ � ������� �� ������������, ���������� �������� �����
'textwidth' ������ ����.


����������� �� ������� �������

������� "j" � "k" ���������� ������ � ��������� � ���������� ������. ���
����������� �� ������� ������� ��� ����� �������� � ����������� �� ���������
�� ���� ���. 
   ��� ����������� �� ���� ������ ������ ����� ��� ���� ����� ������������
������� "gj" � "gk". ���� ������ �� �����������, �� ��� ������� �������� �����
��� ��, ��� � ������� "j" � "k". �������� ����������� �� ����������� �������,
� ���� ������ ��� ������� ���������� ������ �� ��������� �� ���� ��������
������, ������ ����������� � ��������� ��� ���������� ������ ������.
   ��� ����� ����������� ������������ ����� �������� ��� ��������
������������� ���� ������: >

	:map <Up> gk
	:map <Down> gj


�������� ��������� ������ ������ ������

���� �� ������ ������������� ����� � MS-Word ��� ������ �������� ���������, ��
��� ����������� ������� ������ ����� ������ ����� �������. ���� ���� ������
��������� ������� ��������, �� ����� ������������ ��� ���� �������� �����
�������: >

	:g/./,/^$/join

������� ���������, ��� ����������. ������� ��� ������� �� ������:

	:g/./		������� ":global" ������� ��� ������, ������� ��������
			   ���� �� ���� ������.
	     ,/^$/	��������, ������������ �� ������� (��������) ������ ��
			   ��������� ������ ������.
		  join	������� ":join" ���������� ��������� � ���������
			   ������ � ���� ������.

���������, ��� ������� ��� ������� � �������, ��������� �� ���� �����,
����������� � 30 ������� �������� �������� ������: 

	+----------------------------------+
	|�������� IPX/SPX �������� ������� |
	|���������������� ���������� ���   |
	|��������� �����, �� � ���� ����   |
	|���������� -- �� ���������� ������|
	|Novell...                         |
	|                 		   |
	|"������� Windows NT 4.0 Server"   |
	+----------------------------------+

� ����� � ��� ��������� ��� ������:

	+----------------------------------+
	|�������� IPX/SPX �������� ������� |
	|���������������� ���������� ��� ��|
	|������� �����, �� � ���� ���� ����|
	|������ -- �� ���������� ������ Nov|
	|ell...                            |
	|"������� Windows NT 4.0 Server"   |
	+----------------------------------+

���������: ��� ������� �� ����� ��������, ���� ����������� ������ ������ ��
������, ���� ���� ��� ������� �� ����� �������� ��� �������� ���������.
�������, ������� �������� � ����������� �������� � �������� ������������
������, �������� ���: >
>
	:g/\S/,/^\s*$/join

� ����� ����� ������ ���������� ������ ��� ���������� ������, ����� ���������
����� ��������� �� �����.

==============================================================================
*25.5*	�������������� ������

��������, �� ������������ ������� � �������� ���������:

	nice table	  test 1	test 2	    test 3 ~
	input A		  0.534 ~
	input B		  0.913 ~

�� ������ �������� ����� � ������ �������. ��� ����� ����� ����������� ������
�� ������ ������, ������ ������� "A", ����� ��������� ���������� �������� �
����������� ����� � ��������� �������. 
   ��� ��������� ���� ������� ���������� ����������� �����: >

	set virtualedit=all

������ �� ������ �������� ������ � ����������� �������, ���� ���� ����� ���
����������� �������. �������������� ������ � ������ "������������ ���������"
������� �����������.
   ����������� ������ � ����������� ������� ����� ������� ������ ���������
��������� �������: >

	/test 3

������ ������� "j" � �� ��������� � �������, ��� ����� ������ �������� ���
������ "input A". ������� "0.693":

	nice table	  test 1     test 2	 test 3 ~
	input A		  0.534			 0.693 ~
	input B		  0.913 ~

Vim ������������� ��������� ������������ ����� ����������� ������� ���������
����������� ��������. ��� ���������� ��������� ������ � ���� ������� �������
������� "Bj". "B" ���������� ������ � ������ �����, "j" �������� ������ ��
���� ������ ����.

	���������:
	� ���� ������ ������ ����� �������� � ����� ����� ������, � ��� �����
	�� ����� ������. ������, Vim ������� � ������ ������� ������ � ���
	������, ���� �� �������� � ���� ������� �����-���� �����.


����������� �������

������ ��� ��������� �������� �������, ������� ������ ���� ������ ���������
�������, �� ��������� ����� �������� "test 1". ��� �������� ����� ���� �����:
1.  ����������� ������ � ����� ������� ���� �������, �������� � �������
    ������� ������ "/test 3".
2.  ��������� � ����� ����������� ����� �� ������� CTRL-V.
3.  ����������� ������ �� ��� ������ ���� �� ������� "2j". �� ���������� ��
    ����� "������������ �������": ������ "input B" ������� "test 3".
4.  ����������� ������ ������, ����� �������� ��� ������� �������, �������
    ����������� ������������ ����� ���������. ��������, ����� ������ ��� ����
    ���� ������� "9l".
5.  ���������� ���������� ���� �������� "y".
6.  ����������� ������ � ������� "test 1", ��� ������ ���� ������� �����
    �������.
7.  ������� "P".

��� ��� ������ ���������� � ����������:

	nice table	  test 3    test 1     test 2	   test 3 ~
	input A		  0.693     0.534		   0.693 ~
	input B			    0.913 ~

�������� ��������, ��� ��� ������� "test 1" ���� �������� ������, ������� ��
������, � ������� � ������� "test 3" �� ���� ������.

����� ����� �� ������ ������������ ��������������, ����������� ������� >

	:set virtualedit=


����� ����������� ������

�������� � ������������� 'virtualedit' ����������� � ���, ��� ���� �����
"���������" �� �����. �� �� ������ ������������ ��������� � ������� �� �����
������ ��� ����������� �������. �� ����� ������������ � ������ �����: �����
����������� ������.
   �����������, ��� � ��� � ������� ���� ������, � ������� ���������� �����
������� �������� � ������� ���������. �������������� �������� "rx" �� �����
������� ������� ���������:

	inp	0.693   0.534	0.693 ~

	       |
	   rx  |
	       V

	inpx0.693   0.534	0.693 ~

��� ������, ��������� ������� ��������� ��������. ����� ����� ��������,
����������� ������� "gr":

	inp	0.693   0.534	0.693 ~

	       |
	  grx  |
	       V

	inpx	0.693   0.534	0.693 ~

������� "gr" ��������� ���������, ��� ����� �������� ������ ��������
����������� ������������. ��� ���������� ������� ������������ �����������
���������� �������� � �������� ���������. � ����������������, ������ ���������
���������� �� "x" � ����� ����������� ����������� ���������� ��������, �����
����� ����� ������� ��������� ��������� �� ���� �����. � ������ ������ �����
�������� ������ ���������.
   ���� ��� ����������� �������� ��������� ��������, �� ����� ������������
������� "R" ��� �������� � ����� ������ (��. |04.9|). �� �� ����� ������������
� ��� �� ���������: ��������� ������� ���������� � ���������� �� �� �������:

	inp	0	0.534	0.693 ~

		|
	 R0.786 |
		V

	inp	0.78634	0.693 ~

������� "gR" ���������� ����� ����������� ������, ������� ��������� ���������
������:

	inp	0	0.534	0.693 ~

		|
	gR0.786 |
		V

	inp	0.786	0.534	0.693 ~

==============================================================================

��������� �����: |usr_26.txt|  ���������� ������������� ��������
��������� �����: ��. |���������_�����_��_������������|  

vim:tw=78:ts=8:ft=help:norl:
