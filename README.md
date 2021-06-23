README.md

1 - Setup Webhook pointing to the jenkins job
II - Create a Jenkins job to build base image:
    • Give the following are the build steps for the Job echo "triggering image build for Wezva CICD... "sh /buildimage.sh$Baselmage
      $Buildimage $registrypassword echo "Completed image build for Wezva CICD.."


    • Set Job Parameters ie string parameter for Baselmage, BuildImage & password parameter for registrypassword & set the following as
      default values BASEIMAGE="jboss/base-jdk11" BuildImage="wildfly"

    • Source Code Management, git repo as "https://gitlab.com/scmlearningcentre/demo.git"


    • Build when a change is pushed to GitLab under "Build Triggers"
