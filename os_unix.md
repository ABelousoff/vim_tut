*os_unix.txt*   ��� Vim version 6.3.  ��������� ���������: 2003 Mar 15


		      ���������� �� VIM - ���� ���������


							         *unix* *Unix*
� ���� ����� ���������� ���������, ������� ��������� � ������ Vim ��� Unix.

��������� �� ���������� Vim ��� Unix ������� � ������ "INSTALL" � "Makefile" �
�������� src.

���� ������� �� ��������� -- "/usr/local/lib/vim/help.txt". ������ "s:.vimrc"
� "s:.exrc" ������������ �������������� ����� "$HOME/.vimrc" � "$HOME/.exrc".
����� ����, ������ ����� ������������ ���� "/usr/local/etc/vimrc". ����
���������� ������� "/usr/local/share", �� �� ������������ ������
"/usr/local/lib".

��������� ����� (��� ��������-��������) ���������� � "/tmp". ���� �� ������
�������� �� � ������ �������, �� ���������� ���������� ��������� $TMPDIR ���,
����� ��� ��������� �� ������ �������. 

��� ���������� ����������� ����� ������������ ����� '~' (�������� �������) �
'$' (���������� ���������).

					                        *fork* *spoon*
��� ���������� ������� �������� �� ����������� ������������ fork()/exec(), �
������ ����� ������������� ���� ������� ����������, �� ������������ �����
system(), ������� ��������� ����� ��������� � ������. ���� ������������
fork()/exec(), �� � ������ ������� ":version" ���� �������� |+fork()|, ����
������������ system(), �� � ������ ������� ":version" ���� ��������
|+system()|. ��� ��������� ����� �������� ��� ����������.
(�� ������������ fork() � ������ � ����������� �����������, ��. |gui-fork|).

��������� ���������� ��������� � Unix ����� ���� ��������� (��������, ��������
��������, ���� �������� � suntools), �� �� ��������� ����� 'showcmd' � 'ruler'
���������. ���������� �������� ��, ���� � ��� ������� ��������. ����� ����, ��
������ ����������� ���������� ����� 'ttyfast'.

��� ������������� Vim � xterm ����� ������������ �����, ��������� ��������
'mouse' � "a". ��� �������� ������� � ������� X ����� �������� ����������� �
������� � ����� ������������ ����������, � ����� ����� �������� ����������
�������� ����� ��� �������� �����. ���� ��� ��� �� ����� ��������� �����������
� ������� � ������� ���� � ����� xterm, �� ����������� ������� shift ���
������������� ����. �������� |����-�������������|. ���� ��� xterm ����������
�����, �� ���������� �������� ����� ��� �������� ���� ����� ���� �����
����������� � ������� ����� 'ttymouse'.

							     *terminal-colors*
��� ������������� ����� � Vim ����� ������������ �������������� ��������
�������� (� ��� ������, ����� �������� ������������ �����, �� "T_Co" ������
��� ����� ����): >
   :set t_me=^[[0;1;36m     " normal mode (undoes t_mr and t_md)
   :set t_mr=^[[0;1;33;44m  " reverse (invert) mode
   :set t_md=^[[1;33;41m    " bold mode
   :set t_se=^[[1;36;40m    " standout end
   :set t_so=^[[1;32;45m    " standout mode
   :set t_ue=^[[0;1;36m     " underline end
   :set t_us=^[[1;32m       " underline mode start
[ ^[ ��� <Esc>, ��� ����� ��������� CTRL-V <Esc> ]

� ���������� �������� ����������� ����� ������������ ������� ":highlight".

���� "tools/Vim132" ��� �������� ��������, ������� ��������� ��������� Vim �
132-���������� ����� �� ���������� ���� vt100.

vim:tw=78:ts=8:ft=help:norl:
