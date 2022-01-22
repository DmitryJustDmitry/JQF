# Natch Quickstart

## 1. Анализ образа системы, содержащего пресобранную с символами версию программы wget

### 1.1 Подготовка стенда 

Подготовить Linux-based рабочую станцию, поддерживающую графический режим выполнения. Рабочая станция может быть реализована в формате виртуальной машины. Проверенной конфигурацией является Ubuntu20:04, 8 ядер, 8 ГБ ОЗУ. 

Установить на хост требуемое системное ПО, в т.ч. qemu: 
```bash
sudo apt install  -y curl qemu-system
```

Получить представление об общих принципах функционирования и командах управления эмулятора qemu - в [первоисточнике](https://qemu-project.gitlab.io/qemu/system/quickstart.html) или в [переводе](http://onreader.mdl.ru/KVMVirtualizationCookbook/content/Ch01.html).

Создать каталог ~/natch_quickstart (название выбрано произвольно), скачать комлпект поставки Natch в данный каталог:
```bas
cd  ~/natch_quickstart && \
curl -o Natch_documentation.pdf 'https://nextcloud.ispras.ru/s/raFWeX6B7XgYWDt/download?path=%2FNatch%20v.1.1&files=Natch_Documentation.pdf&downloadStartSecret=w0qrqfp8d9' && \
curl -o libs.zip 'https://nextcloud.ispras.ru/s/raFWeX6B7XgYWDt/download?path=%2FNatch%20v.1.1&files=libs_1804_natch_release_latest.zip&downloadStartSecret=shqvee1d2de' && \
curl -o plugins.zip 'https://nextcloud.ispras.ru/s/raFWeX6B7XgYWDt/download?path=%2FNatch%20v.1.1&files=qemu_plugins_1804_natch_release_latest.zip&downloadStartSecret=j0vq3mla9o8' && \
unzip libs.zip && \
unzip plugins.zip && \
rm -f libs.zip plugins.zip
```

Ознакомиться с документацией на Natch в файле `Natch_Documentation.pdf`, а также [Natch Wiki](https://fanta.intra.ispras.ru/mediawiki/natch), в частности получить представление:

- об основных принципах работы Natch
- об основных видах анализа и реализующих их плагинах
- о типовых командах Natch

Скачать [обучающий комплект](https://nextcloud.ispras.ru/s/o4w2mSqYAP4xFY3), включающий в себя в том числе qemu-образ, содержащий пресобранную с отладочными символами версию программы wget. Наличие символов позволит Natch формировать более читабельные отчеты, подставляя имена реальных функций анализируемой программы вместо адресов в памяти. Скачать образ можно командой: 

```bash
cd  ~/natch_quickstart && \
curl -o wget_image.zip https://nextcloud.ispras.ru/s/o4w2mSqYAP4xFY3/download && \
unzip wget_image.zip && \
rm -f wget_image.zip && \
mv 'For Dmitriy' wget_image # Временное название каталога на сервере надо будет заменить на что-то общеупотребительное
```

### 1.2 Запись трассы выполнения

1. Выполнить ...

```
Хорошо бы выполнить chmod +x natch_run.sh && ./natch_run.sh
```

### 1.3 Анализ записанной трассы выполнения

1. Выполнить ... 

