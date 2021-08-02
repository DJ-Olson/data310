# Using the Text generation with an RNN script we developed during today's class, use the shakespeare.txt file to generate your own text that imitates the script from Shakespeare. Produce your generated text and describe how it was produced, addressing the following aspects.

## Generated Text

ROMEO:
No other, wo scact'd fart:
Which it in! Whoo leave secford.
And sack, lere is engreds of yes mones a casulo.

ROMEO:
What, boy, and you, reigh meny thee has warthou,
And yo repliance it you shall peesons you! would my brootion to the were
That know over in please's strembyou:
And yous in give them they life of he dissond.

AUTIDINCRAY:
Ofform,
Dukingwed, und.
Lersure:
She know you keen,
When you have here comfand to fer his boding viman
And, bay shall hagh denere you, cavee of partice
To hear not,--

SIMINLUMER:
You what is the out, tilk; putchim upon my prining.
LEONTES:
I hap, the geate,-stroke peace, what so manter stand,
The worsh therefore tulning Ederid with sim, ighomans,
For make math righrenst not noil fall, good comes to read wither.

LOOND KING EDWARD:
Had cabuly, behoultt, I'll sorether. Maday, then they was woods the meco durn;
In he dest, sir villain too lets us again.

Privond:
He they ready and dir.

LORENTE:
I know you was see my ward, thear notes!


## Processing, vectorizing and predicting text
When processing the imported text it must first be vectorized. This means turning the strings of texts into numeric figures. To predict the text we use training examples and targets. In this model we created input, label pairs from example sequences. Once this is done, training batches are created and we start to train the data. 

## Building and training the model
To build and train the model we used Keras. This model used three Keras layers; an embedding layer, a GRU layer, and the final output layer. Next we applied standard sparse categorical crossentropy to create a loss function before training begins. This sets up the model for training, and then a number of epochs were picked to train the model. This model took a very long time to train, so I only used 3 epochs, although if I had more time or a more powerful computer I could have used more epochs to improve the accuracy. 

## Generating text
To actually generate the text, the model used a loop which generated new characters for the new text based off the training text. This loop was executed with a class called OneStep. After the functions within this class were run, the generated text above was able to be produced by the model. As you can see, the generated text does not make complete sense, but it is definitley not just random. With the few amount of epochs used I am happy with the result. 
