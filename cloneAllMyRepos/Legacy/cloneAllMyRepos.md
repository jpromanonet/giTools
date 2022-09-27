# Clone all repos for Users

'''
CNTX={users}; NAME={username}; PAGE=1
curl "https://api.github.com/$CNTX/$NAME/repos?page=$PAGE&per_page=100" |
  grep -e 'clone_url*' |
  cut -d \" -f 4 |
  xargs -L1 git clone
'''

# Clone all repos for orgs

'''
CNTX={orgs}; NAME={orgname}; PAGE=1
curl "https://api.github.com/$CNTX/$NAME/repos?page=$PAGE&per_page=100" |
  grep -e 'clone_url*' |
  cut -d \" -f 4 |
  xargs -L1 git clone
'''