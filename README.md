# What
This was created using readthedocs and mkdown for the SCAG SPM user manual.

# How
1. Create a python virtualenv
2. `pip install -r requirements.txt`
3. run `mkdocs serve` to run a local version of the docs while editing
4. newest commits once pushed to bitbucket repo should appear at https://spm-dm-documentation-update.readthedocs.io/en/latest/
5. if not check the latest build message at https://readthedocs.org/projects/spm-dm-documentation-update/builds/ under the build tab

# Note
- For the email link in `user_support.md` we use the Markdown.pl 1.0.1 plain text conversion from [http://johnmacfarlane.net/babelmark2/?text=User+support+is+available+at+%3Cspm%40scag.ca.gov%3E](http://johnmacfarlane.net/babelmark2/?text=User+support+is+available+at+%3Cspm%40scag.ca.gov%3E) due to a bug in the mkdocs version we use described at [https://github.com/mkdocs/mkdocs/issues/646](https://github.com/mkdocs/mkdocs/issues/646)
