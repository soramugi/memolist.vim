# memolist.vim

This is a vimscript for create and manage memo.  
memolist.vim is inspired by [jekyll.vim](https://github.com/csexton/jekyll.vim).

## Setup

Set the path to your memo directory in your .vimrc.(default directory `$HOME/memo`)

    let g:memolist_path = "path/to/dir"

You may also want to add a few mappings to stream line the behavior:

    nnoremap <Leader>mn  :MemoNew<CR>
    nnoremap <Leader>ml  :MemoList<CR>
    nnoremap <Leader>mg  :MemoGrep<CR>

## Commands

Create New Memo:

    :MemoNew

Show Memo List:

    :MemoList

Grep Memo Directory:

    :MemoGrep

## Options

    let g:memolist_memo_suffix = "markdown"
    let g:memolist_memo_suffix = "txt"
    let g:memolist_memo_date = "%Y-%m-%d %H:%M"
    let g:memolist_memo_date = "epoch"
    let g:memolist_memo_date = "%D %T"
    let g:memolist_prompt_tags = 1
    let g:memolist_prompt_categories = 1
    let g:memolist_qfixgrep = 1
    let g:memolist_vimfiler = 1

you can use other format and custom template.
(default memo format is `markdown`.)

if you use custom template file(`~/memotemplates/rdoc.txt`).  
add the following lines to your `.vimrc`

    let g:memolist_memo_suffix = "rdoc"
    let g:memolist_template_dir_path = "~/memotemplates`

## Install

Copy it to your plugin and autoload directory.

## License

Lcense: Same terms as Vim itself (see [license](http://vimdoc.sourceforge.net/htmldoc/uganda.html#license))
