# Вход в систему и доступ к ресурсам

#### Как войти в консоль управления?

Перейдите на [страницу консоли управления](https://console.cloud.yandex.ru/). Если вы еще не вошли в ваш аккаунт на Яндексе или Яндекс.Коннекте, нажмите **Войти**. Если у вас еще нет аккаунта, нажмите **Зарегистрироваться**.

Подробнее читайте в [документации Яндекс.Паспорта](https://yandex.ru/support/passport/auth.html).

#### Как проверяются права доступа?

Пользователям назначаются роли на определенный ресурс. Это называется _привязкой прав доступа_. При выполнении операции с ресурсом [!KEYREF iam-short-name] проверяет, обладает ли пользователь необходимой ролью для этой операции. Подробнее читайте в разделе в разделе [[!TITLE]](../concepts/access-control/roles.md).

#### Что такое ресурс?

_Ресурс_ — это сущность Яндекс.Облака, с которой вы можете выполнять операции: создавать, изменять, просматривать или удалять. Примеры ресурсов: виртуальные машины, диски, сервисные аккаунты, облака и каталоги. Подробнее читайте в разделе [[!TITLE]](../../resource-manager/concepts/resources-hierarchy.md) документации сервиса [!KEYREF resmgr-name].

#### Что такое привязка прав доступа?

_Привязка прав доступа_ — это назначение роли пользователю по отношению к указанному ресурсу. Подробнее читайте в разделе [[!TITLE]](../concepts/access-control/access-bindings.md).