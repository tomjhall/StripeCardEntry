StripeCardEntry
==============

What is this?
-------------

StripeCardEntry takes the simple, elegant credit card entry UI of Stripe and ports this to
the Android Platform. In a nutshell StripeCardEntry has:

* Support for Visa, Mastercard & American Express cards.
* Number validation using Luhn algorithm ensures the user will not enter an invalid number.
* Date validation ensures the user can only enter a valid expiry date.

StripeCardEntry really is just a space saving, intuitive UI for card entry:

.. image:: demo.gif

Installation
------------

Just copy over the StripeCardEntryLibrary to your AndroidStudio project & add as a dependency.

General use
-----------

Simply add the view to your layout file:

.. code:: xml

    <com.rethoughtsolutions.stripecardentry.StripeCardEntry
        android:id="@+id/stripecardentry"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="@android:drawable/editbox_background_normal" />

And add a listener for when the user has successfully entered a credit card:

.. code:: java

    findViewById(R.id.stripecardentry).setListener(new StripeCardEntry.Listener() {
        @Override
        public void onCardEntryCompleted(boolean completed) {
            //...
        }
    });




