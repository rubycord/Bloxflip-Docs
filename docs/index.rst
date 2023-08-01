# Bloxflip API - The Official Documentation

About This Doc
--------------
The Official Documentation for `Bloxflip `_
Shoutout to: Jumbo, Vprime

What's Bloxflip?
-----------------
Bloxflip is an online platform that offers an API for developers to integrate gambling functionality into their applications. This documentation is provided solely for educational purposes and is intended for developers seeking to understand and utilize the Bloxflip API. Please note that while the API enables the inclusion of gambling features, we do not endorse or promote gambling activities.

Games API
---------
The `Bloxflip Games API `_ consists of 45 different APIs, each of which will be explained in detail.
The Games API allows you to make GET and POST requests to the API in order to perform various actions.
Click `here <#games-api>`_ to access the Game API section.

Game API
--------
Welcome to the Game API section! Here, you will find detailed information about each of the APIs available in the Bloxflip Games API.
`Click here <#towers-api>`_ for Towers API.

Towers API
----------
`Create a Towers game via API <#towers-create-api>`_

Towers Create API
-----------------
The Towers Create API allows you to create a Towers game using the Bloxflip API.
To create a Towers game, make a POST request to the following endpoint: ``https://api.bloxflip.com/games/towers/create``
The request body should include the necessary parameters for creating the game, such as the game name, game type, and game settings.
Here is an example of how to create a Towers game using the Bloxflip API:

.. code-block:: python

    from zenrows import ZenRowsClient
    client = ZenRowsClient("ZENROWS KEY HERE")
    url = "https://https://api.bloxflip.com/games/towers/create"
    response = client.post(url, headers={"x-auth-token": "bloxflip auth token here", json={
                            "betAmount": str(5),
                            "difficulty": "easy"
                        }
                    )
    )
    # Difficulty Options: easy, normal, hard
    print(response.text)

In the examples above, we are creating a Towers game with the bet amount of 5, the type "towers", and the difficulty options are "easy", "normal" and "hard".

Once the game is created, you will receive a response from the API with the game ID and other relevant information.

Note: The Towers Create API is just one of the APIs available in the Bloxflip Games API. Please refer to the `Games API <#games-api>`_ section for more information on other available APIs.

We hope this documentation helps you in integrating the Bloxflip API into your applications. If you have any further questions or need assistance, feel free to reach out to our support team. Happy coding!

Towers Action API
-----------------
The Towers Create API allows you to create a Towers game using the Bloxflip API.
To create a Towers game, make a POST request to the following endpoint: ``https://api.bloxflip.com/games/towers/create``
The request body should include the necessary parameters for creating the game, such as the game name, game type, and game settings.
Here is an example of how to create a Towers game using the Bloxflip API:

.. code-block:: python

    from zenrows import ZenRowsClient
    client = ZenRowsClient("ZENROWS KEY HERE")
    url = "https://https://api.bloxflip.com/games/towers/action"
    response = client.post(url, headers={"x-auth-token": "bloxflip auth token here", json={
                            "cashout": False,
                            "tile": 3
                        }
                    )
    )
    # Cashout options: False or True
    print(response.text)

In the examples above, we are creating an instance to click a tile, the type "cashout" which is a Boolean, True or False.

Once the game is tile in clicked, you will receive a response from the API with the game ID and other relevant information.

Note: The Towers Action API is just one of the APIs available in the Bloxflip Games API. Please refer to the `Games API <#games-api>`_ section for more information on other available APIs.

We hope this documentation helps you in integrating the Bloxflip API into your applications. If you have any further questions or need assistance, feel free to reach out to our support team. Happy coding!
