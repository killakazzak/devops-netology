# Описание игнорируемых файлов в .gitignore

В файле .gitignore перечислены файлы и директории, которые будут проигнорированы системой контроля версий Git:

## 1. Директории Terraform
- /.terraform/: Все локальные директории Terraform, содержащие временные и промежуточные файлы, которые не имеют отношения к версии кода.

## 2. Файлы состояния
- *.tfstate: Все файлы состояния Terraform, которые содержат информацию о текущем состоянии инфраструктуры.
- *.tfstate.*: Любые временные или резервные файлы состояния.

## 3. Логи сбоев
- crash.log и crash.*.log: Файлы журналов, создаваемые в случае сбоев Terraform, которые не нужно сохранять в системе контроля версий.

## 4. Файлы с переменными
- *.tfvars и *.tfvars.json: Файлы, содержащие переменные, которые могут включать конфиденциальные данные (например, пароли или ключи). Эти данные могут варьироваться в зависимости от окружения и не должны быть частью версии кода.

## 5. Переопределяющие файлы
- override.tf, override.tf.json, *_override.tf, *_override.tf.json: Эти файлы используются для локального переопределения ресурсов и не должны быть добавлены в версионный контроль.

## 6. Файлы блокировок
- .terraform.tfstate.lock.info: Временные файлы блокировок, которые создаются при применении изменений в Terraform.

## 7. Конфигурационные файлы CLI
- .terraformrc и terraform.rc: Конфигурационные файлы для настройки Terraform, которые не нужно отслеживать в репозитории.
- доп. запись

