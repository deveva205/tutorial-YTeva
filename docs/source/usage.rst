Usage
=====

.. _installation:

Installation
------------

To use YTeva, first install it using pip:

>>> pip install YTeva

Usage
----------------

You can use ``downloa_audio`` to play the song in the call or if you want to make the bot send it you can use ``download_audio_send``.

For example play in call:

>>> from pyrogram import Client
>>> from yteva import YTeva
    app = Client("my_bot", api_id=123456, api_hash="your_api_hash", bot_token="your_bot_token")
    yteva = YTeva(api_key="your_api_key", bot_app=app)
    async def main():
        await app.start()
        result = await yteva.download_audio("your_video_id")
        print("Downloaded:", result)
        await app.stop()


For example send audio:

>>> from pyrogram import Client
>>> from yteva import YTeva
    app = Client("my_bot", api_id=123456, api_hash="your_api_hash", bot_token="your_bot_token")
    yteva = YTeva(api_key="your_api_key", bot_app=app)
    async def main():
        await app.start()
        result = await yteva.download_audio_send("your_video_id")
        print("Downloaded:", result)
        await app.stop()
