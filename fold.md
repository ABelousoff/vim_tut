*fold.txt*      ��� Vim version 6.3.  ��������� ����������: 2004 May 20


		      ���������� �� VIM - ���� ���������


�������			               *Folding* *folding* *�������* *�������*

��������� �������� �� ������������� ������� ���������� � ����� 28 �����������
������������, ��. |usr_28.txt|.

1. ������� �������� �������	    |�������-������|
2. ������� ��� ������ �� ���������  |�������-�������|
3. ����� ��� ������ �� ���������    |�������-�����|
4. ��������� �������		    |�������-���������|

{Vi �� ����� �������� �� ���������}
{�������� ������ � ��� ������, ���� Vim ������������� � ������������
|+folding|}

==============================================================================
1. ������� �������� �������  		       *fold-methods* *�������-������*

������ �������� ������� ����� ���� �������� ��� ������ ����� 'foldmethod'.

���� ����� �������� ����� 'foldmethod' ���������� �� "manual", �� ���
������������ ������� ��������� � ��������� ����� �������. ��� ������������ �
������ "manual" ������������ ������� �� ���������. ���� ����� ���������������,
����� ���������� ������� � �������������� ������, � ����� �������� �� �������.

��� �������� ������� ����������� ����� �������:

	manual		������� ������������ �������
	indent		������� �������� ������� �������� ������� �������
			�������
	expr		��� ����������� ������� ������������ ���������
	syntax		������� ������������ � ������������ � ���������
			��������� ����������
	diff		����������� ����� ������� ��� ��������� �������� �
			������
	marker		������� ������������ � ������� ����������� �������� �
			������


������ ������ (MANUAL)		         *fold-manual* *�������-������_������*

��� ����������� �������� ������� ������������ ����������� �������. ���� ������
����� ����� ������������ � ��������, ������� ������������� ����� ���
���������� � ��� �������.

������� ������� ������������ ������ � ������������. ��� ���������� ������
������� ��� ��������� �����, ���������� ������ ���� ������� ��� ���� �������,
������� ��������������� �� ���� �� ������ ��������� �����.

������ ������� �������� ��� ������ �� �������� ����. ��� ����������
����������� ������� ������� ����� ������������ �������� |:mkview|. 
��� ����� ���� ������������ ����� �� ������� |:loadview|.


����������� ������� �� �������� (INDENT)       *fold-indent* *�������-�������*

��� ������������� ����� ������ ������� ������� ������������� ������������ ��
�������� ������� � ������.

�������� ������ ������� ����������� ���� ������� �������� ������� �� ��������
����� 'shiftwidth' (���������� �� �������� ������). ������������������ �����
� ���������� ��� ����� �������� ������� ������� �������� �������, ������
������ � ����� �������� ������� �������� �� ��������� �������.

����������� ������� �������������� ��������� ����� 'foldnestmax'.

��� ���������� ������� ������� ������ � ��������� ������� ������������, �
��������������� �������� ����������� �� ���������� ��� ����������� ������, �
����������� �� ����, ����� �� �������� ����� ����� ���������� ������� �������.
� ����� ������� ��������� ������ ������, ������, ��������� �� ��������, �
������, ������� ���������� � ������ �� ��������, �������� � �������� �����
'foldignore'. ����� ���������, ������������ � �������� ����� 'foldignore'
����� ��������� ����� ���������� ���������� ��������. ��� �������������
������� ������ � ������ ��������� ���� �� ����� C ������ �������� ������ "#" 
� �������� �������� ����� 'foldignore' -- ��� ��������� ���������� ������ �
��������� �������������.

������ �������� �������� ����� � �������� �������� ������������� ������
'expr'. �� ������� �� ������������� ���������, ������� ������������ � ��������
����� 'foldexpr'. � ���� ��������� ����� ������������ ������� |indent()| ���
��������� �������� ������� � ������.


����������� ������� � ������� ��������� (EXPR) *fold-expr* *�������-���������*

��� � ��� ������������� ������ "indent" ������� ������������� ��������� �
������������ � ����������� �������� �������. ��� ��������� �������� �������
������� ��� ������ ������ ������������ ���������, �������� � �������� �����
'foldexpr'. ������� ��������� ��������:

�������� �������, ���������� ��� ����������� ������, ������������ � �������
���������:
>
	:set foldexpr=getline(v:lnum)[0]==\"\\t\"

������������� ������ ������� ��� ���������� ������� �������:
>
	:set foldexpr=MyFoldLevel(v:lnum)
	
�������� ������� �� ��������� �������, ���������� ������� ��������: 
>
	:set foldexpr=getline(v:lnum)=~'^\\s*$'&&getline(v:lnum+1)=~'\\S'?'<1':1

��� ���� ������ �������� ���� �� ������ �������:
>
	:set foldexpr=getline(v:lnum-1)=~'^\\s*$'&&getline(v:lnum)=~'\\S'?'>1':1

�������� ��������, ��� ��� ������������� ����������� ��� ������� ":set"
�������� (�������, �������� ����� �����, ������� ������� � �.�., 
��. |�����-��������_�����|) ����������� ������ �������� ����� �����.

��� ���������� ��������� ����������� �� �������� ��������� �������:

- ������� ����� � �������� ����, � ������� ��������� ��������������� ������;
- �������� ���������� "v:lnum", ������� ������������� ����� ���������������
  ������.

��������� ��������� ������������ ��� ����������� ������� ������� ���������
�������:

  ��������		����� ~
  0			������ �� ��������� � �������
  1, 2, ..		������ ��������� � ������� � ��������������� �������
                        �������
  -1			������� ������� �� ����������, ������������ ��������
			������� ������� ���������� ��� ����������� ������, 
			� ����������� �� ����, ����� ������ ����� ����������
			�������� ������� �������
  "="			������������ ������� ������� ���������� ������
  "a1", "a2", ..	� �������� ������� ������� ���������� ������
			����������� 1, 2 � �.�.
  "s1", "s2", ..	�� �������� ������� ������� ���������� ������
			���������� 1, 2 � �.�.
  "<1", "<2", ..	������� � ��������� ������� ������� ������������� ��
			���� ������
  ">1", ">2", ..	������� � ��������� ������� ������� ���������� ��
			���� ������

�������� ������ � ����� ������� � ������� ">1" � "<1" �� ��������
������������, ������� ������������� ����� ���������� � ������������� � ���
������, ���� �������� ������� ������� ������ ��� ������, ��� �������� �������
������� ���������� ������.

��������� �� ������ ��������� �������� ��������. ����� � ������, �������
�������, ������� ��� ������, �������� ����� � �.�. �� ������ ���������� 
� �������� ���������� ���������.

���� � ��������� ������� �����-���� ������, ���� ��������� ����������
��������� �� �������� ���������� ��� ������ ��������, �� ��������� �� ������
�� ���������, � ������� ������� ��������������� ������ ����. ��� �������
��������� ��� ������ �� ��������� ����� ��������� ����� 'debug' ��������
"msg": � ���� ������ ��������� �� ������� ����� ����������.

���������: ��������� ��������� ������ ����������� ��� ������ ������,
������������� ����� ������ ����������� ������� ����� ���� �����
������������������ ��������!

������������ �������� ������������ �������� "=", "a" � "s", ��������� ��� ��
������������� ����� ���������� ��������� ����� ���������� ������ �
����������� ��������� ������� �������, ��� ����� ����� ��������� ������ Vim.

������� |foldlevel()| ����� ����������� ��� ���������� ������ ������� �������
�� ��������� � ����������� ������. �������, ������, ����� � ����, ��� ���
������� ����� ���������� �������� -1, ���� ������� ������� �� ��������. �����
����, ��� ������� ���������� �������� ������� ������� ��� ������ ������, � ��
����� ��� ������� ����� ������������� � ���� ������.


					     *fold-syntax* *�������-���������*
����������� ������� � ������������ � ��������� ���������� (SYNTAX)

��� ������������� ������� �������, ������� ������������ �� ��������������
���������, � ������� ������ �������� "fold", ��. |:syn-fold|.

������� ������� ��������������� � ������������ � ���������� ���������.
����������� ������� ����� ���� ���������� ��� ������ ����� 'foldnestmax'.

������ �����������: ������������� ���������� ������ ���� ������ ���������.
���� ������������� ���������� ����������� �����������, �� ������� ����� �����
��������� � ������������ ���������� ����������. ��� �������� ����� ���
������������� ��������, ������� ����� ��������������� ��������� �����. ���� ��
����������� ��������, �� ����������� ��������������� �������������:
>
	:syn sync fromstart
<

						    *fold-diff* *�������-diff*
����������� ������� ��� ��������� �������� ����� �������� (DIFF)

��� ������������� ������� ������� ������� ��������� ������������� ��� ������,
������� ��������� � ��������� ������ � ��������� ���������� ������ ��
������������� ����������.

���� ����� �������� ������ � ��� ������, ���� � �������� ���� �������� �����
'diff' � ��� ������������ ��� ����������� �������� � ������ �������. �
��������� ������ ���� ����� ����� ����� ������� ��������.

����� 'diffopt' ����� ����������� ��� ��������� ���������� ����� ���������.
���� ��� � ����� ����� ����� �������� � �������������� ����������� ������,
������� � ������� �� ����������. ��������, ��� ������������� 8 �����
���������:
>
	:set diffopt=filler,context:8

�� ��������� ��� ��������� ������������ 6 �����.

���� �������� ����� 'scrollbind', �� Vim ����� �������� ��������� ���
������������� ��������������� ������� � ������ �����, ������������ ���
��������� ��������, ����� ����� ����������� ���� � ��� �� �����.


                                               *fold-marker* *�������-�������*
����������� ������� ��� ������ �������� (MARKER) 

��� ������������� ������� ������� ������ � ����� ������� ���������� � ������
��� ������ ����������� ��������. ��� ��������� ���������� ������� �
������������ ���������, ������� � ��������� ������� ��� ����� ���������
��������� �������. ����� 'foldtext' ������ ������������� ����� �������, ���
����� ����� �������� ������������ � ������ �������, ��� ��������� ������
�������� �����.

������� ����� �������� �������� �� ������� �������. �������� ����� ����������
������ ��������. ����� �������� ������� ������� �������� �����
�������, ��������� � ���� ������ �� �� ������� ������������ ������� ��� �����
������� � � ��� �� ����� ������ � ���������� ������ ��������. ��������:
>
	/* ���������� ���������� {{{1 */
	int varA, varB;

	/* ������� {{{1 */
	/* funcA() {{{2 */
	void funcA() {}

	/* funcB() {{{2 */
	void funcB() {}

������� ���������� � ������� "{{{". ��������� �� ���� �������� ����� ���������
�� ������� �������. ��������� Vim ������� �� ����, ��� ���������� ���� ��
����� ������� ������� ��� ������ ������ � �������, �������� � �������
�������:

1. ���� �� ������ ����������� ����� ������ � ��� �� ����� ��������, ��
   ���������� ������� ����������� � ���������� ����� ������� � ��� �� �����
   ������� �������.
2. ���� �� ������ ����������� ������ � ����� �������� �������, �� ��������
   ��������� �������.
3. ���� �� ������ ����������� ������ � ����� �������� �������, �� �����������
   ��� ������� � ������� ��� ������ ������� ������� � �������� ����� �������
   � �������� �������.

����� ����� ������� ��������� �� ������� �������. ���� �� ������������. ��
������ ��������� ������ "}}}" � ������ ��� �������� ������ �������, �������
������ ���� �������� � ���� �����. ������� ������� ��� ��������� ������ � ����
������ ����� �� ������� ������, ��� �������� �����. �������� ��������, ��� Vim
�� ��������� ������� ������� ���������� �������, ��������� ��� ���� �� ������
������������. ������� ��� �� �������:
>
	{{{1
	������� ������� ����� 1
	{{{3
	������� ������� ����� 3
	}}}3
	������� ������� ����� 2

����� ����, �� ����� ������ �������� ������� � ������� ������ �������� "{{{" �
"}}}". ������ ������ "{{{" ����������� ������� ������� �� �������, � ������
"}}}" ��������� � �� �� �� ����� ��������. ������� �� ��������� ��������!

������:
>
	{{{
	������� ������� ����� 1
	{{{
	������� ������� ����� 2
	}}}
	������� ������� ����� 1

�� ������ �������� ��������� � ������ ������� � ������ � ��� �����. ��������,
������� ������������ ������� � ������ ��� ������� �������, � �� ����� ���
������ ���� ������� ��������� ��������� ����� ���������� ��������� ��� �����.
����������� ������� 1 ��� ����� �������� ������, ��� "����������� ��������
������", "������� ����������", "�������"; ������� 2 ����� ��������� ���
��������� ����������� � �������. ������ ������� ����� ������������
��������������� ���������, ����� ��� �� ����� ����� �������� ����� �����
�������� � ��� ������, ���� ������� ����� ������� ��� �������� ��������� � ���
�������.

�������, ����������� � �������� ��������, ����� ���� ������ � ������� �����
'foldmarker'. ����� �������, ���������� � Vim � �������������� �������� ���
����������� �������, ����� ���� ������������ � ������� ��������������, �����
�� �������� �������� �� ��������� �������� ���� ����� "{{{,}}}" ��� ������
�������������. ��������� �������� ���� ����� ����� ������������� � ���
�������, ����� ��� ��������� ��������� �������������� ����� (��������, ���� ��
�������� ������� ��� ������� ���������, ��� ���� �������� �� ��������� �������
�� ����������� ��������� ���������� ����� ����� �����).

			       *fold-create-marker* *�������-��������_�������*
������� "zf" ����� ����������� ��� �������� �������, ����������� ��� ������
��������. Vim ������������� ������� ����������� ������� � �����, ��������
������� ������ � ����� ������� � ������������ �� ��������� ����� 'foldmarker'.
������� ����������� � ����� ��������������� ������. ���� �������� �����
'commentstring' �� �������� ������ �������, �� ��� ����� ������ ��� ����������
��������.

��� ����������� �� �������� ��� ������� � ��������� �������:

- ������ ��� �������� ������ � ��������� ������ ������� �������. � ���� ������
  Vim �� �����, ��� ��� ������.
- ����������� ������� ���������� ����� ��� �������� �� �������� ������
  ������� �������, ������� ������������ ������� �������.
- ������ ��������� ������ �����������, �������� ����� 'commentstring' ��
  �������� ������ �������, � ��������� ����������� �� �����������. ��������, �
  ������ ��������� ���� ��������� �� ����� C: ��� ���������� /* {{{ */ ������
  ����������� ���������� ��� ������������ �����������. � ���� ������ �����
  ����� ��������� ������ ���� �� �����������, ���� �����, ��� �������� ������
  �������.
  
��� ������� �� ������� ��������� Vim'� ��������� �������, ���� � ��� ��� ����
�������, ������������ ����� ��� �������� �������� ������ �������.

			       *fold-delete-marker* *�������-��������_�������*
��� �������� �������, ����������� ��� ������ ��������, ����� �����������
������� "zd". ��� ���������� ���� ������� Vim ������ ��������������� �������
��� ������ � ����� �������, ��� ��� ������ � �������� ����� 'foldmarker', ��
������. ���� ����� ������ ������� ��������� �� ��������� �����
'commentstring', �� �� ����� ����� �����.

��� ����������� �� �������� ��� ������� � ��������� �������:

- � ������ ���������� ��������� ��������, ���� �� ������� ���������� ����� ���
  �������� ������ ������� �������. � ���� ������ ��������� ������ ������
  ������, �� �������� ����������� �������� ������� �� �����������.
- ������ �������� ����� ��� �������� ������ ������� ������� � ������������ ���
  �������� ������ ��� ����� ����� ���������� ������� ������������.

==============================================================================
2. ������� ��� ������ �� ���������    *fold-commands* *E490* *�������-�������*

��� ������� ��� ������ �� ��������� ���������� � ����� "z". ������, ����� "z"
������ �� ��������� ���� ������, ���� ���������� �� ���� �� �������.


�������� � �������� ������� ~
							           *zf* *E350*
zf{�����������} ���
{���������}zf	
		�������-�������� ��� �������� �������.
		����������� ������ ��� ������������� �������� �����
		'foldmethod' "manual" � "marker". ��� ������������� �������
		"manual" ��������� ������� ����� �������.
		������� �������� ����� 'foldenable'.
		��. ����� |�������-��������_�������|.

							                  *zF*
zF		������� ������� ��� N �����. �������� ��� ��, 
                ��� ������� "zf".

:{��������}fo[ld]						 *:fold* *:fo*
		������� ������� ��� ����� � �������� {���������}. �������� ���
		��, ��� ������� "zf".

							           *zd* *E351*
zd		������� ������� ���� ������� � ������� �������. ���� ������
		��������� �� ������ � �������� ��������, �� ��������� ���
		�������. ��� ���� ��������� ������� ������������ �� ����
		������� ������� ������� ����. � ���������� ������ ��� �������,
		��������� ��� �������� ���������� � ���������� �������,
		���������. ������ �����������, ��� ���� ����� ���� �������
		������ �������, ��� �� ��������, � ������ �������� ��
		�������������.
		����������� ������ ��� ������������� �������� �����
		'foldmethod' "manual" � "marker".
		��. ����� |�������-��������_�������|.

							                  *zD*
zD		���������� ������� ��� ������� � ������� �������. � ����������
		������ ��������� ��� �������, ��������� ��� ��������
		���������� � ���������� �������, � ����� ��� ���������
		�������.
		����������� ������ ��� ������������� �������� �����
		'foldmethod' "manual" � "marker".
		��. ����� |�������-��������_�������|.

							           *zE* *E352*
zE		������� ��������� ���������� (���������: "eliminate") ��� ����
		������� � �������� ����.
		����������� ������ ��� ������������� �������� �����
		'foldmethod' "manual" � "marker".
		��. ����� |�������-��������_�������|.


�������� � �������� ������� ~

�������, ������� �������� ������ �����, ��� ������� � �������� �����
'foldminlines', ������ ������������ �� ������ � �������� ���������. �������,
������� ����������� ����, ����� �������� �����, ���� ��� ����������� ���
���������� ���������.

							                  *zo*
zo		������� ���� ������� � ������� �������. ���� ������
		�����-���������, �� ����������� ��������������� ����������
		�������. � ���������� ������ ����������� ���� ������� �������
		��� ���� �����, ���������� � ���������� �������.

							                  *zO*
zO		������� ��� ������� � ������� ������� ����������. �������,
		������� �� �������� ������ � ������� �������, �� �������������
		���� ��������.
		� ���������� ������ ��� ������� ��������� ��� �������,
		��������� ��� �������� ���������� � ������� ���������.

							                  *zc*
zc		������� ���� ������� � ������� �������. ���� ������ �����, ��
		����� ������� ��������� ������� �� ��������������� �������. 
		� ���������� ������ ����������� ���� ������� ������� ��� ����
		�����, ���������� � ���������� �������.
		��� ���������� ���� ������� ���������� ����� 'foldenable'.

							                  *zC*
zC		���������� ������� ��� ������� � ������� �������. �������, ��
		���������� ������, � ������� ��������� ������, ��
		������������� ���� ��������. � ���������� ������ �����������
		��� �������, ��������� ��� �������� ���������� � ����������
		�������.
		��� ���������� ���� ������� ���������� ����� 'foldenable'.

							                  *za*
za		���� ������� ����������� �� �������� �������: ������� �������.
		� ��� ������, ���� � ���� ������ ������� ��������� �������,
		����� ������������� ��������� ������� "za" ��������� ���. ���
		�������� �����-��������� ����������� ���������������
		���������� �������� �������.
		
		���� ������� ����������� �� �������� �������: ������� �������
		� �������� ����� 'foldenable'. ������� ��������� ������ ����
		������� �������, ��������� ��� ��������� ������������� �������
		"za" ����������� �������� �������� �������. ��� �������������
		�����-��������� ����� ������� ��������������� ����� �������
		(��� �� �� �� �����, ��� ���������� ������� "za"
		��������������� ���������� ���).

							                  *zA*
zA		�� �������� �������: ���������� ������� �������.
		�� �������� �������: ���������� ������� ������� � ��������
		����� 'foldenable'.

							                  *zv*
zv		���������� ������ � ������� �������: ������� ����� �������
		�������, ������� ���������� ��� ��������� ������, � �������
		��������� ������. ���������: ����. "view", "����������".

							                  *zx*
zx		�������� �������: ���������� ��������� � ��������� �������,
		�������� �������, ����������� ����� 'foldlevel' � �����
		����������� ������� "zv" (�������� ������ � ������� �������).

							                  *zX*
zX		�������� ������� �������� ��������� � ��������� ������� �
		��������� ����� 'foldlevel'.

							                  *zm*
zm		������� ������ ("more"): ������� ��������� �������� �����
		'foldlevel' �� 1. ���� ����� 'foldlevel' ����� �������
		��������, �� ������ �� ����������.
		��� ���������� ���� ������� ���������� ����� 'foldenable'.

							                  *zM*
zM		������� ��� �������: ���������� �������� 'foldlevel' ������ 0.
		��� ���������� ���� ������� ���������� ����� 'foldenable'.

							                  *zr*
zr		������� ������ ("reduce"): �������� 1 � �������� �����
		'foldlevel'.

							                  *zR*
zR		������� ��� �������. �������� ����� 'foldlevel'
		��������������� ������ ����������� ������ ������� �������.

							  *:foldo* *:foldopen*
:{��������}foldo[pen][!]
		������� ������� � ��������� {���������}. ��� ���������� [!]
		����������� ��� �������. ������� ��� ��������� ����� ������ �
		�������� {���������}. ��� [!] ����������� ������ ���� �������
		������� �������.

							 *:foldc* *:foldclose*
:{��������}foldc[lose][!]
		������� ������� � ��������� {���������}. ��� ���������� [!]
		����������� ��� �������, ��� ������� � ��� �������, ����� ����
		�������� ���� ����� � ��������� {���������}. 
		��� [!] ����������� ������ ���� ������� �������.

							                  *zn*
zn		��� �������: ��������� ����� 'foldenable'. ��� ������� �����
		�������.

							                  *zN*
zN		�� ���������: �������� ����� 'foldenable'. ��������� �������
		����� �������������.

							                  *zi*
zi		����������� �������� ����� 'foldenable'.


����������� �� �������� ~
							                  *[z*
[z		����������� ������ � ������ ������� �������� �������. ����
		������ ��� ��������� � ������ �������, �� ����������� ������ �
		������ ������� �� ��������� � ������� �������. � ���������
		������, ���� ������� ������� �� ����������, �������
		����������� ��������.
		��� ������������� �����-���������, ������� ����������� N ���.

							                  *]z*
]z		����������� ������ � ����� ������� �������� �������. ����
		������ ��� ��������� � ����� �������, �� ����������� ������ �
		����� ������� �� ��������� � ������� �������. � ���������
		������, ���� ������� ������� �� ����������, �������
		����������� ��������.
		��� ������������� �����-���������, ������� ����������� N ���.

							                  *zj*
zj		����������� ������ ���� � ������ ��������� �������. ��� ����
		�������� ������� �������������� ��� ���� �������.
		��� ������������� �����-���������, ������� ����������� N ���.
		��� ������� ����� �������������� � �������� |��������|�.

							                  *zk*
zk		����������� ������ ����� � ����� ���������� �������. ��� ����
		�������� ������� �������������� ��� ���� �������.
		��� ������������� �����-���������, ������� ����������� N ���.
		��� ������� ����� �������������� � �������� |��������|�.


���������� ������ � ��������� ������� ~

:[��������]foldd[oopen] {�������}			*:foldd* *:folddoopen*
		��������� ��������� {�������} � ��������� ���� �����, �������
		�� ������ � �������� �������.
		��� ������������� [���������] ������� ����������� ������ �
		�������� ��������� �����.
		��� ������ ���������� {�������} ������ ���������� � ������,
		��� ������� ��� �����������.
		��� ������ �� ������ ������� ":global": ������� ���������� ���
		������, ������� �� ��������� � �������� ��������. ����� ���
		������ ���������� ����� ������� ������ ����������� ���������
		{�������}. ���� � �������� ���������� {�������} ���������
		������� ����������, �� ��� �� ��������� ������� �� ��, � �����
		������� ��� ����� ��������� (����, �������, ������ ��� ���� 
		�� ���������). 
		
		������: >
		
			:folddoopen s/end/loop_end/ge
<		
		�������� �������� �� ������������� ����� "e" � ������� ������,
		������� ��������� �������� ������ ��������� �� ������ � ���
		������, ���� ������������ ������� "end" �� ����������.

:[��������]folddoc[losed] {�������}		    *:folddoc* *:folddoclosed*
		��������� ��������� {�������} � ��������� ���� �����, �������
		��������� � �������� ��������. �� ��� ��������� �������
		�������� ��� ��, ��� ":folddoopen".

==============================================================================
3. ����� ��� ������ �� ���������	        *fold-options* *�������-�����*

�����					         *fold-colors* *�������-�����*

����� ��������� �������� ������� ������������� � ������� ������ Folded, ��.
|���������-Folded|.  ����� ������� ������� ������������� � ������� ������
FoldColumn, ��. |���������-FoldColumn|.

������ ��������� ������: >

	:highlight Folded guibg=grey guifg=blue
	:highlight FoldColumn guibg=darkgrey guifg=white

<
                                                     *�������-�������_�������*
			                             *�������-�������_�������*
������� ������� (FOLDLEVEL)		  *fold-foldlevel* *�������-foldlevel*

��������� ����� 'foldlevel' �������� �����: ��� ��� ����, ��� ������ �������
����� �������.
��� �������� ����� 'foldlevel' ������ 0 ��� ������� ����� �������.
��� ������������� �������� ����� 'foldlevel' ����������� ��������� �������, �
������������ � ������� �������.
��� ����� ������� �������� ����� 'foldlevel' ����� ������� ��� �������.
�������� ����� 'foldlevel' ����������� ��� ��� ���������. ����� ����� �������
����� ����������� � ����������� �������.
��� ���������� �������� ����� 'foldlevel' ����������� �������, ������� �������
������ ������ ��������. ��� ���� �������, �������� �������, �� �����������.
��� ���������� �������� ����� 'foldlevel' ����������� �������, ������� �������
������ ������ ��������. �������, �������� �������, �� �����������.

                                                       *�������-�����_�������*
                                                         *�������-���_�������*
��� ������� (FOLDTEXT)		            *fold-foldtext* *�������-foldtext*

��������� ��������� ����� 'foldtext' �������� ���������, ������� �����������
��� ��������� ����� �������. ������ ������� ���������� �����, �������
������������ � ������ �������� �������. ������� ������:
>
    :set foldtext=v:folddashes.substitute(getline(v:foldstart),'/\\*\\\|\\*/\\\|{{{\\d\\=','','g')

� ������ ������ � �������� ����� ������� ������������ ������ ������ ������� �
��������� ��������� "/*", "*/" � "{{{".
�������� �������� �� ������������� �������� ����� ����� ��� �������������
��������, ������� ����� ����������� �������� ��� ������������� � �������
":set". ������� ����� ���������� ������� � ������� � �� ��������� � ��������
������ �����:
>
    :set foldtext=MyFoldText()
    :function MyFoldText()
    :  let line = getline(v:foldstart)
    :  let sub = substitute(line, '/\*\|\*/\|{{{\d\=', '', 'g')
    :  return v:folddashes . sub
    :endfunction

���������� ��������� ��� 'foldtext' ����������� � |���������|. �������� �����
��� ���������� ��������� ���������� ����, � ������� ������������
��������������� ������. ������ ������������.

�� ��������� ��������� � ������ ����� �������� ������� |foldtext()|. ���
������� ���������� ���������� ��� ����������� ������� ���. ���� ��� ��
���������� �������� �� ���������, �� �� ������ ������ ����������� ���������
'foldtext', ������� ����� ������������ ��� ����������� ���������� Vim:

	v:foldstart	����� ������ ������ �������
	v:foldend	����� ��������� ������ �������
	v:folddashes	������, ������� ������������ �������� ������ �������
			������� � ���� ������������������ �������
	v:foldlevel	������� ������� �������

������� ��������� � ���������� ���������� ��������� ���������� ���������, �
���������� ������� ������������ � �������� �������.

���������� � ���������� ������ ����������, ����� � ����� ���� ��������� �
����. ��� ������ ������� �� �����������. ���� ����� ����� ������� ������
�����, �� ��� ����������� ��������, ��������� � �������� ����� 'fillchars'.

�������� ��������, ��� ��� ������������� ����������� ��� ������� ":set"
�������� (�������, �������� �����, ������� �������) ������� ������������
������ �������� ����� �����. ��. |�����-��������_�����|.

                                                     *�������-�������_�������*
������ ������� ������� (FOLDCOLUMN)     *fold-foldcolumn* *�������-foldcolumn*

��������� ����� 'foldcolumn' �������� �����, ������� ����� ������ �������
����� �� ����, ������� ������������ ��� ����������� �������. ���� ��������
���� ����� ����� ����, �� ������� ������� �� ������������. ������ �����������
�������� 4 ��� 5. ����������� �������� �������� ���� ����� ����� 2, �
����������� ��������� -- 12.

�������� ������� � ������� ������� ���������� �������� '-' � ������� ������
������� � ��������� '|' � ����������� �������, ������ �� ��������� ������
�������� �������. ���� ������� ��������� ��������� �������, �� ���������
������� ������������ � ������� ������� ���������, �������������� ������ ��
�������� ������� �������.

�������� ������� ������������ � ������� � ������� ������� '+'.

���� ������ ������� ������� ������������ ��� ����������� ���� ���������
�������, �� ��� ����������� ������ ����������� ������������ �����.

������� ������� ����� ��������� ������������ ���� ��� �������� � ��������
��������������� �������:

- ������ ����� �� ������� '+' ��������� �������� ������� � ���� ������.
- ������ ����� �� ����� ������ ������������ ������� ��������� �������� �������
  � ���� ������.


������ �����

'foldenable'  'fen':	��������� ��� ������� ��� ���������.
'foldexpr'    'fde':	���������, ����������� ��� ������� ������� "expr".
'foldignore'  'fdi':	�������, ������������ �������� "indent".
'foldmarker'  'fmr':	�������, ����������� ��� ������� "marker".
'foldmethod'  'fdm':	�������� �������� ������� ����������� �������.
'foldminlines' 'fml':	����������� ���������� ����� ������, �����������
			���������� ������� � �������� ���������
'foldnestmax' 'fdn':	������������ ������� ��� �������� "indent" � "syntax".
'foldopen'    'fdo':	����� �������, ���������� ������� �������� � ��������
			�������� �������.
'foldclose'   'fcl':	������������ ��� �������� ������� ��� �����������
			������� �����.

==============================================================================
4. ��������� �������		           *fold-behavior* *�������-���������*

��� ����������� ������� �� ������ ����� ��� ���� ��� ��� ���������� ���������,
������ ������������ � ������ ������ �������� �������. ���� ������ ���
��������� �� ������ � �������� ��������, �� �� ������������ � ���������
��������� ������ ��� � ��������� �������� �������.

���� ������ ��������� �� ��������� ������, �� ������ ���������� � ������
�������. ������� ���������� ����������� ������� �������, �� ��������� ������
�������, �� ������ �� ����� ���� ������� � ���� �������.

������ ������� ����������� ������������� ������������������ ����� � ��������
������� ��� ������ ������. ��������, ������� "w" ��������������� � ������
�������.

� ������ ������� ������, � ������� ��������� ������, ������� �� ������ �
�������� �������. ��� ��������� ��� ������ ����� � �������� �����!

��� ������������� ���������, �������� ������� ���������� � �������� ��� ����
�����. ��������, ������� "dl" ��� �������� �������� ������� ��� ������ � ����
�������.

��� ���������� ������ Ex �������� ���������� ����� �������, ����� �� ���������
�� ������ ������ �������, � ������������ ��������� ������� �������. �����
�������, ��� ������������� �������
>
	:s/���/���/g
<
� ��������, ���������� �� �������� �������, ����� ��������� ������ "���" ��
"���" �� ���� ������� �������.
��� �� �������� ������ |:folddoopen| � |:folddoclosed|.

��� �������������� ������ ������������ ������ ������������ ��������� �������,
������� ����������� � ��������� ���. ��� ������������� ������� �������
����������� ������� ����������������� ������ ����������� �������. �� ����
������� ����������������� ��������� �������, �������� ��� ��������. ����
������ ����� �������������� � ���� ����, �� ������������ �������� ��� �������
����, � ��������� ������ ����������������� ��������, ������� ���� � ���� � ���
����, ��� ����� �������������� � ��������� ���.

==============================================================================
 vim:tw=78:ts=8:ft=help:norl:
