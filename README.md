# SVNinfo

# Reading SVN External Information
# In your repositories svn external report, you may have many lines that link your repository to old SVN externals.
# If you need to pull in the data from those repositories, it is helpful to understand the information below.
# Here is an example output, and how it can be read.

# OUTPUT EXAMPLE:
# https://svn-url.com/svn/Project/MoreProject/EvenMoreProject - 
# -r 12345 ^/Project/SomeOtherProject@1234 Path/In/Repository
# -r 123 /svn/some/path/to/another/repo@123 Path/in/Repo
# -r 234 /svn/some/path/to/another/repo1@234 Another/Path/in/Repo
# -r 456 /svn/some/path/to/another/repo1@456 Some/Path/in/Repo

# In the EXAMPLE above:
# https://svn-url.com/svn/Project/MoreProject/EvenMoreProject - this is the root repository 
# # -r 12345 ^/Project/SomeOtherProject@1234 Path/In/Repository - This is at what revision of the root repository another project is inserted
# - It also states what revision that code was at, and where it was inserted into the root repository
# Additional information:
# http://svnbook.red-bean.com/en/1.7/svn.advanced.externals.html
# Path information:
# ../ - Relative to the URL of the directory on which the svn:externals property is set
# ^/ - Relative to the root of the repository in which the svn:externals property is versioned
# // - Relative to the scheme of the URL of the directory on which the svn:externals property is set
# / - Relative to the root URL of the server on which the svn:externals property is versioned
