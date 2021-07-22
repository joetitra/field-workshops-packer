# Packer Workshops FAQ
### Frequently Asked Questions

**Q. How do these Instruqt tracks work?**<br>
A. Instruqt tracks contain a `config.yml` file which builds a student workstation, currently an Ubuntu Linux 18.04 virtual machine of n1-standard-1 size. The workstation has 3.6GB of RAM and the open source version of Visual Studio Code installed as a web application. This makes it very easy for students to edit their packer code using a comfortable and familiar environment.

Other tools included on the workstation are vim, nano, emacs, jq, unzip, curl, wget git, az command line, and some other various tools and easter eggs. Instruqt also provides an AWS account, Azure subscription, or GCP project for each student. These are deleted once the track is stopped or expires.

Students then build and learn packer in these temporary environments using the provided sample code.

**Q. How do credentials get handled? Does anyone clean up these resources when the workshop is over?**<br>
A. Instruqt provides an entire AWS account, Azure subscription, or GCP project for each student. Cleanup is done by Instruqt when the track expires or the student clicks the Stop button.

**Q. What happens if I get stuck or find errors during a workshop?**<br>
A. You can always post in #se-workshops or #proj-instruqt and someone should be able to assist.

**Q. Some of my students are rushing ahead in the lab exercises. How can I get them to stay with the class?**<br>
A. You can share the Packer puzzles git repo with them, and suggest that they work on those when they finish each section. These bite-sized Packer challenges can be done without disrupting the main lab exercises: https://github.com/hashicorp/workshop-puzzles

**Q. My student somehow got their workstation completely stuck and are unable to get past the check script in Instruqt. Help?**<br>
A. Instructors may now override any check script by creating a file at `/tmp/skip-check` on the student workstation. This file will override the check and allow you to skip to the next lab challenge. Use with discretion.

```
touch /tmp/skip-check
```

**Q. How can I start/stop/restart the Code Server text editor?**<br>
A. The new code-server has a standard systemd init script. If a student's editor locks up for some reason you can simply restart it:

```
systemctl restart code-server
```

**Q. Is there a way to fast-forward to a particular part of a track?**<br>
A. Currently this is only possible for members of the HashiCorp Instruqt organization. However, you can use the `/tmp/skip-check` file as mentioned in the previous question to quickly skip past challenges to a particular point in the Intro to Packer tracks. `/tmp/skip-check` must be created for each challenge that you want to skip.

**Q. What is the Bonus Lab?**<br>
A. The bonus lab is meant for intermediate to advanced users who have already completed the main track. The bonus lab is a challenging combination that tests several skills learned in the Packer workshop. Access it here:<br>
https://instruqt.com/trace3/tracks/packer-cloud-bonus-lab
