*os_dos.txt*    ��� Vim version 6.3.  ��������� ���������: 2003 Dec 20


		      ���������� �� VIM - ���� ���������


							           *dos* *DOS*
���� ���� �������� ����� ����������� ������ Vim ��� MS-DOS � Win32. ��. �����
|os_win32.txt| � |os_msdos.txt|.

1. ��������������� ������		|dos-���������������_������|
2. ������������� �������� ����� �����	|dos-��������_�����_�����|
3. ����������� �������� ������		|dos-�����������_��������|
4. ����� �� ����� � �����		|dos-�����|
5. ������ ������			|dos-������_������|
6. ������� :cd				|dos-:cd|
7. ����������� ���������� ������	|dos-CTRL-Break|
8. ��������� �����			|dos-���������_�����|
9. �������� ����� 'shell' �� ���������	|dos-��������|

==============================================================================
1. ��������������� ������         *dos-locations* *dos-���������������_������*

��� �������� ������������ ����� Vim � ��������, � ������� ����������
����������� help � syntax ��� ������ Vim �� ��������� ������� ��������������
��������. �� ��������� ������ ��������� � ��������� ������� ��� �������������
���������� ���������. ������ ���������, ��� ���� ������� ������� � ����������
����, ��� ����������� ������� �� ������� �����.

����� vimrc ("_vimrc" � "_gvimrc") ������ ����������� � ��������, �������
��������� �� ���� ������� ����. ���� �� ������ ��������� �� � ������ �����, ��
������� �� �������������� ��� ������ ���������� ��������� $VIM. ������: >
	
	set VIM=C:\user\piet

����� ������ ���� "c:\user\piet\_vimrc".

���������: ��� ��������� ������ � ��� �������, ����� ����������� ����������
��������� �������. � ������� ������ ���������� ������ ������� ���� _vimrc �
��� �����, ��� �� ������ ��������� �� ���������.

���� �� ��������� ����������� ���� � ������ �����, �� ��� ����� �����������
���������� ���������� ��������� $VIM. ����� ������ ����� ����������� �� ����
"$VIM/vim{������}". ��������: >

	set VIM=E:\vim

����� ������ ����� Vim ������ 5.4 � "e:\vim\vim54".

���������: ������ ��� �� �������������. ���������������� ����� �������
����������� ���� � �������� � ������� ������� ����� Vim.

���� �� ��������� ����������� ���� � ������ ��������� ����� ����-���� �����
"_vimrc" � "_gvimrc", �� ���������� $VIM ������ ��������� �� ������� � �������
vimrc, � ���������� $VIMRUNTIME �� ������� � ������� Vim. ��������: >

	set VIM=C:\usr\piet
	set VIMRUNTIME=E:\vim\vim54

����� �������� "c:\user\piet\_vimrc" � ��������� ����� � "e:\vim\vim54".

��������� �������� |$VIM| � |$VIMRUNTIME|.

��� Windows 95, ���������� $VIM ����� ���������� � ����� C:\autoexec.bat.
��������: >

  set VIM=D:\vim

��� Windows NT ����� ����������� ���������� ��������� �������� ��� �������
������������, � "����/���������/������ ����������->�������", ��� � ����������
� ���� "��� ���������", � ������� "���������".

==============================================================================
                                                    *dos-��������_�����_�����*
2. ������������� �������� ����� �����                          *dos-backslash*

������������� �������� ����� ����� � ������ ������ ����� ������� ��������. Vi
��������� ��� ��������� ������ ���������� �������������� �������� ����� �����.
Vim ��������� ����� ������� � �� ������� �������� ����� �� ����� �����, ���
��� ":e c:\foo\bar" ����� ��������, ��� ����������. ������, ���� ��������
����� ����������� ����� ����������� �������� (������, �������, ���� ��������
�����), �� Vim ������� �������� �����. ����� �������� �������, ����� �����
������������ ������ �����: ":e c:/foo/bar" ������� ��������. �� ���������
������� � ���������� ����������� MS-DOS � Win32, Vim ��� �������������
�������� ������ ����� �� ��������. 

���� �� ������������� ������������ ������ ����� ����� � ����� � ������, ��
��������� ����� 'shellslash'. � ���� ������, Vim ����� �������� �������� �����
�� ������, ����� ����� ������ ����� �� �����. ��� �������� ������� ���
������������� Unix-��������� 'shell'.

==============================================================================
	                                            *dos-�����������_��������*
3. ����������� �������� ������	                       *dos-standard-mappings*

CTRL-PageUp	������ � ������ ������ ������			  *<C-PageUp>*
CTRL-PageDown	������ � ����� ��������� ������ ������    	*<C-PageDown>*

��� ����������� ���������� ����������:

������		��� ������   �������/����������     �������  ~
CTRL-PageUp	<M-N><M-C-D>	    H		    <C-O>H
CTRL-PageDown	<M-N>v		    L$		    <C-O>L<C-O>$

����� ����, ����� �������� ��������� ������ ��� �������� �����������, �������
� ��������. � ������� ��� Win32 � DJGPP ������������ ��������� ����� ������.

Shift-Insert	������� ������ (�� ������ ������)		  *<S-Insert>*
CTRL-Insert	����������� ����������� ������ (� ����� ������)	  *<C-Insert>*
CTRL-Del	��������� ����������� ������ (� ����� ������)	     *<C-Del>*
Shift-Del	��������� ����������� ������ (� ����� ������)	     *<S-Del>*

��� ����������� ���������� ���������� (� ������� ��� Win32 � DJGPP):

������		��� ������   �������	����������  �������~
Shift-Insert	<M-N><M-T>   "*P	"-d"*P      <C-R><C-O>*
CTRL-Insert	<M-N><M-U>		"*y
Shift-Del	<M-N><M-W>		"*d
CTRL-Del	<M-N><M-X>		"*d

���� ���������� (� ��-Win32 �������):

������          ��� ������   �������    ����������  �������~
Shift-Insert	<M-N><M-T>   P		"-dP	    <C-R><C-O>"
CTRL-Insert	<M-N><M-U>		y
Shift-Del	<M-N><M-W>		d
CTRL-Del	<M-N><M-X>		d

���� �������������� ��������� ����� ������, �� ������������ ������� "*.

==============================================================================
4. ����� �� ����� � �����			      *dos-colors* *dos-�����*

�� ���������, ����� �� ����� ���������� ������ bios. ��� �������� ��
����������� ��������������� ������. ��� �� ��������� ������������ �������
ansi.sys. ��� ��������� ������������ ������ ������ ����� ������������ ��������
":mode", ��������� ��. � |:mode|.

��� ��������� ������ ������, ������������ Vim, ����� ��������� �������
|:highlight|. ������ ��������� Normal ��������� �� �����, ������� ������������
Vim ��� �������� ������. ��������, ����� �������� ����� ����� �� ����� ����: >

	:hi Normal ctermbg=Blue ctermfg=grey

� ������ ������� ��������� ������� � |���������-������|.

���������� ���� DOS �� ������������ ����� ��������, ��� ������ ����� �
�������������. �������� ��������, ��� ��� �� �����������, ��������� �� ������
��������� ���� ��������������� � ������� ������� ":highlight"; ��� �����
���������� ��� �������� ������������� �� ������� �������� Vim. �����
|'highlight'| ���������� ���� �� ���� �������, ������������ ��� �������
��������. >

	:set t_mr=^V^[\|xxm		������ ���������� ������
	:set t_md=^V^[\|xxm		������ ������� ������
	:set t_me=^V^[\|xxm		������� � �������� ������

	:set t_so=^V^[\|xxm		������ ������ ���������
	:set t_se=^V^[\|xxm		������� � �������� ������

	:set t_us=^V^[\|xxm		������ ������ �������������
	:set t_ue=^V^[\|xxm		������� � �������� ������

	:set t_ZH=^V^[\|xxm		������ ���������� ������
	:set t_ZR=^V^[\|xxm		������� � �������� ������

^V ��� CTRL-V
^[ ��� <Esc>
��� ����������� �������� xx ���������� �����, ���������� ������ ������ �����
������ � ������ ����� ����:

���� 			���� (�������)		 ��� ������      ��� ����~
Black			׸����			      0		    0
DarkBlue		Ҹ���-�����		      1		   16
DarkGreen		Ҹ���-������		      2		   32
DarkCyan		Ҹ���-��������		      3		   48
DarkRed			Ҹ���-�������		      4		   64
DarkMagenta		Ҹ���-���������		      5		   80
Brown, DarkYellow	����������, ����-�����      6		   96
LightGray		������-�����		      7		  112
DarkGray		Ҹ���-�����		      8		  128 *
Blue, LightBlue		�����, ������-�����	      9		  144 *
Green, LightGreen	������, ������-������	     10		  160 *
Cyan, LightCyan		��������, ������-��������    11		  176 *
Red, LightRed		�������, ������-�������	     12		  192 *
Magenta, LightMagenta	���������, ������-���������  13		  208 *
Yellow, LightYellow	Ƹ����, ������-�����	     14		  224 *
White			�����			     15		  240 *

* � ����������� �� ������, ���� ������ ���� 128 ����� ���� �� ��������, 
  � ��� 128 ����� ��������� � �������� ������.

��� ������������� 0, ���� ����������������� � ��������������� ��� ������� Vim
(������ 7, ������-����� �� ������, �� �� ������ ��� ��������. ���� �� ��������
����� �� ��������� � ��������� ������, �� ���, ��������, ������� ��������
��������� ��������� � ����� vimrc -- ��. ����). 
��� �������� �� ��������� ��� t_me.

�������� �� ��������� ��� ��������� ������� ���������:
	t_mr	112	 ��������� �����: ������ ����� (0) 
			    �� ������-����� (112)
	t_md	 15	 ������: ����� ����� (15) �� ������ (0)
	t_me	  0	 ������� ����� (������� � �������� �� ���������)

	t_so	 31	 ����� ���������: ����� (15) ����� �� ����-����� (16)
	t_se	  0	 ����� ������ ��������� (������� � �������� ��
			    ���������)

	t_czh	225	 ������: ����-����� (1) ����� �� ����� (224)
	t_czr	  0	 ����� ������� (������� � �������� �� ���������)

	t_us	 67	 �������������: ����-�������� (3) ����� ��
			    ����-������� (64)
	t_ue	  0	 ����� ������������� (������� � �������� �� ���������)

��� ����� ���� ������� ������, ��� ��� ����� �������� ������� � ���������
������������, �� �� ������ �������� �� �� ������ ����������.

������: >

  :set t_mr=^V^[\|97m	" ������ ���������� ������: ����-����� (1) ��
			" ���������� (96)
  :set t_md=^V^[\|67m	" ������ �������: ����-�������� (3) �� 
			" ����-������� (64)
  :set t_me=^V^[\|112m	" ������� � ����������� ������: ������ (0) ��
			" ������-����� (112)

  :set t_so=^V^[\|37m	" ������ ������ ���������: ����-��������� (5) ��
			" ����-������ (32)
  :set t_se=^V^[\|112m	" ������� � ����������� ������: ������ (0) ��
			" ������-����� (112)

==============================================================================
5. ������ ������	                *dos-file-formats* *dos-������_������*

���� ����� 'fileformat' ����������� � �������� "dos" (�� ���������), ��
Vim ������������ � �������� �������� ����� ������ (<EOL>) ���� ��������� <NL>,
���� ���� �������� <CR><NL>. ��� ������ ����� Vim ���������� <CR><NL>.
�������, ���� �� ������������ ���� � ���������� ����� � ���� ���������� <NL>,
�� ��� ������ Vim ������� �� �� <CR><NL>.

���� ����� 'fileformat' ����������� � �������� "unix", �� Vim ���������� ���
<EOL> ��������� ������ <NL> � ���������� <CR> ��� ^M.

�� ������ ������������ Vim ��� ������ <NL> �� <CR><NL>, �������� ���� �
�������� � ����� ������ � ��������� ������� � ������ Dos (":se ff=dos").
�� ������ ����� ������������ Vim ��� ������ <CR><NL> �� <NL>, �������� ���� �
�������� � ������ Dos � ��������� ������� � ������ Unix (":se ff=unix").

Vim ������������� ����� 'fileformat' �������������, ���� �������� �����
'fileformats' �� ������, ��� ��� ������� �� ���������, ��� ��� ��� �� �����
������ �������� �� ��� ��������. |'fileformat'| |'fileformats'|

���� �� ������ ������������� ���� �������� ��� �������� ����, �� ��� �������
���������� ����� 'binary' ����� ��������� �����. ����� ��������� � ��������
����� ����� ��������� ��������� ������ <NL>, ������� � ��������� ������ �����
���������� Vim �� <CR><NL>. ����� 'binary' ����� ���� �����������
�������������, ���� �������� ����������� � ������ "-b" (binary).

==============================================================================
6. ������� :cd						             *dos-:cd*

������� ":cd" �������� ��������� �� ���� � ��������� ������ ������� ����. ���
����� �������� ����� �� ���� C, ������� ������� ":cd c:" ��� �������� �
������� "foo" �� ��������� �������� ����� D, ������� ":cd d:\foo". Vim �����
��������� ����� UNC, ���� ��� �������������� ��������, ��������: 
":cd \\server\share\dir". |:cd|

==============================================================================
7. ����������� ���������� ������			      *dos-CTRL-Break*

����������� CTRL-Break ������ CTRL-C ��� ����������� ������. Vim �� ��������� 
CTRL-C � ����� ���������.

==============================================================================
8. ��������� �����			*dos-temp-files* *dos-���������_�����*

������ ��� 16-�� � 32-������ ������ ��� DOS:

Vim �������� ��������� ����� (��� ������-��������) � ������ �� ���������� ����
���������, ������� ������� ����� � � ������� Vim ����� ������� ����:
	$TMP
	$TEMP
	C:\TMP
	C:\TEMP
	������� �������

��� ������ Win32 (���������� � � ����������� �����������):

Vim ���������� ����������� ������� Windows ��� ����������� ����� ����������
����� ��� ������ � ���������-���������. ������������ ������ �� ��������� �
������ ���������, ������� ���������� � � ������� Vim ����� ������� ���������
����:
	$TMP
	$TEMP
	current directory

==============================================================================
9. �������� ����� 'shell' �� ���������		    *dos-shell* *dos-��������*

�������� ����� 'sh' ('shell') �� Windows 95 �� ��������� "command.com", ��
Windows NT -- "cmd.exe". ���� ���������� ���������� SHELL, �� Vim ����������
�������� ���������� SHELL, � ���� SHELL �� ����������, �� ����������
���������� COMSPEC, �� Vim ���������� �������� ���������� COMSPEC. ������
������� �������� ���������� � ������� ������� "<shell> /c <���_�������>".
������� CTRL-Z ��������� ����� ��������� ��������. ������� � Vim
�������������� �� ������� "exit". |'shell'| |CTRL-Z|

���� �� ����������� �������� �� �������� �������������, �� ��� ��������
����������� ��������� ����� |'shellcmdflag'| ('shcf') � |'shellquote'| ('shq')
��� |'shellxquote'| ('sxq'). � ���������, ��� ������� �� ������������ ������
Vim, ��������, ��� ������������� �������� MKS Korn ��� bash, �������� ����
����� ������ ���� ���������:

		DOS 16 ���	    DOS 32 ���		Win32  ~
'shellcmdflag'	   -c			-c		 -c
'shellquote'	   "
'shellxquote'						 "

��� ����, ������ �������� � 16-������ ������ DOS �������������� ��������:
	<shell> -c "���_�������" >����
� Win32:
	<shell> -c "���_������� >����"
� 32-������ ������ DOS ��� ���������� ������ DJGPP.

��� �������, Vim ��������� ����������� "sh" � ������ ����� 'shell'. ����
���������� ����������, �� Vim ������������� ����� 'shellcmdflag' �
'shellquote' ��� 'shellxquote' ��� ������� ����.

==============================================================================
vim:tw=78:ts=8:ft=help:norl:
