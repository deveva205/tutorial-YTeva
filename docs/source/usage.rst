Usage
=====

.. _installation:

Installation
------------

To use YTeva, first install it using pip:

>>> pip install yteva

Usage
----------------

You can use ``play_audio`` to play the audio song in the call or you can play a video using ``play_video`` or if you want to make the bot send it, you can use ``download_send_audio`` it will send it audio. If you want a video use ``download_send_video``.


For example play in call:

>>> PLAY AUDIO
    from pyrogram import Client
    from yteva import YTeva
    app = Client("my_bot", api_id=123456, api_hash="your_api_hash", bot_token="your_bot_token")
    yteva = YTeva(api_key="your_api_key", bot_app=app)
    async def main():
        await app.start()
        result = await yteva.play_audio("your_video_id")
        print("Downloaded:", result)
        await app.stop()


>>> PLAY VIDEO
    from pyrogram import Client
    from yteva import YTeva
    app = Client("my_bot", api_id=123456, api_hash="your_api_hash", bot_token="your_bot_token")
    yteva = YTeva(api_key="your_api_key", bot_app=app)
    async def main():
        await app.start()
        result = await yteva.play_video("your_video_id")
        print("Downloaded:", result)
        await app.stop()


For example send:

>>> SEND AUDIO
    from pyrogram import Client
    from yteva import YTeva
    app = Client("my_bot", api_id=123456, api_hash="your_api_hash", bot_token="your_bot_token")
    yteva = YTeva(api_key="your_api_key", bot_app=app)
    async def main():
        await app.start()
        result = await yteva.download_send_audio("your_video_id")
        print("Downloaded:", result)
        await app.stop()


>>> SEND VIDEO
    from pyrogram import Client
    from yteva import YTeva
    app = Client("my_bot", api_id=123456, api_hash="your_api_hash", bot_token="your_bot_token")
    yteva = YTeva(api_key="your_api_key", bot_app=app)
    async def main():
        await app.start()
        result = await yteva.download_send_video("your_video_id")
        print("Downloaded:", result)
        await app.stop()
