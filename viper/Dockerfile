FROM neriberto/viper

RUN mkdir -p /root/.viper && \
    cp /usr/share/viper/viper.conf.sample /root/.viper/viper.conf && \
    sed -i 's/#admin/admin/' /root/.viper/viper.conf
