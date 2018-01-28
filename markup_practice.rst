==============================
rstファイルの書き方の練習(h1)
==============================

インラインマークアップ(h2)
==========================

**太文字**

*斜体*

``リテラル``

`リンク付きテキスト <http://docs.sphinx-users.jp/rest.html>`_

---------------------
コードブロック(h3)
---------------------

.. code-block:: java

        final Notification.Builder builder = new Notification.Builder(context)
            .setContentTitle("Show Notification by App's Receiver")
            .setContentText(message)
            .setSmallIcon(R.drawable.ic_launcher)
            .setAutoCancel(true);

        Intent resultIntent = createIntent(context, extras);

        if (extras.containsKey(EXTRAS_KEY)) {
            resultIntent.putExtra(EXTRAS_KEY, extras.getString(EXTRAS_KEY));
        }

        if (extras.containsKey(io.repro.android.GCMReceiver.NOTIFICATION_ID_KEY)) {
            resultIntent.putExtra("repro-notification-id", extras.getString(io.repro.android.GCMReceiver.NOTIFICATION_ID_KEY));
        }

        PendingIntent resultPendingIntent = PendingIntent.getActivity(context, identifier, resultIntent, PendingIntent.FLAG_CANCEL_CURRENT);
        builder.setContentIntent(resultPendingIntent);

        Notification notification = builder.getNotification();

        final NotificationManager notificationManager = (NotificationManager)context.getSystemService(Context.NOTIFICATION_SERVICE);
        notificationManager.notify(identifier, notification);


リスト(h4)
--------------

箇条書き

* あれや
- これや
+ どれや
手順

#. あれをして
#. これをして
#. ああする
定義
	tabで区切ると定義になるようだ
ジャズ
	宇都宮はジャズの街として売り出し中。

	楽器メーカーを多数抱える静岡の浜松がライバル

ディレクティブ
-----------------

.. image:: ./img/うまるちゃん.jpg




