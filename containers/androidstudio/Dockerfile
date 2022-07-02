FROM ubuntu:latest

# you can change this with a newer/older android studio version !
ARG ANDROIDSTUDIO_DOWNLOAD_LINK=https://redirector.gvt1.com/edgedl/android/studio/ide-zips/2021.2.1.15/android-studio-2021.2.1.15-linux.tar.gz

# Installing android studion and other dependencies
RUN dpkg --add-architecture i386
RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install -y libc6 libncurses5 libstdc++6 lib32z1 libbz2-1.0
RUN apt-get install -y wget
RUN apt-get install -y default-jdk
RUN apt-get install -y libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386
RUN wget -O android.tar.gz ${ANDROIDSTUDIO_DOWNLOAD_LINK}
RUN tar -xf android.tar.gz -C /opt
RUN apt-get install -y x11-apps

# Cleaning up
RUN apt purge
RUN apt autoremove
RUN rm android.tar.gz

# running android studio on starting
CMD ["/opt/android-studio/bin/studio.sh"]