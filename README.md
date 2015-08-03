# Demonstrating Switching Jekyll Themes using github remotes

1. Forked [Dr. Jekyll's Bootstrap Theme](https://github.com/drjekyllthemes/jekyll-bootstrap-theme)
2. Clone the theme locally:  
   ```bash
   git clone https://github.com:radumas/theme-switch-test.git
   cd theme-switch-test/
   ```
3. But, for the sake of this example, I didn't really like that one so I wanted to try out [Dr. Jekyll's minimal theme](https://github.com/drjekyllthemes/jekyll-minimal-theme). So I a branch for the new theme.  
   ```bash
   git checkout -b newtheme
   ```  
4. And then add the new theme as a remote 
   ```bash
   git remote add jekyll-minimal-upstream https://github.com:drjekyllthemes/jekyll-minimal-theme.git
   git pull jekyll-minimal-upstream HEAD 
   ```
5. The messy part, you're going to have a bunch of merge conflicts. Check which files have merge conflicts with `git status`, hopefully these conflicts should only be in style files that you want to overwrite. If there any files you want to keep you can either edit them with a text editor: git will have labelled the changes in the file 
5. Push to your origin
   ```bash
   git push origin newtheme 
   ```
6. Go to your project's page on github and you'll notice something like this:  
   ![](/images/Selection_004.png)
7. Create a pull-request and merge the new changes in.
