# Assignment 2 Question 2
##TODO

- [x] Add regularization
- [x] Add dropout

## Running time comparisons with AWS p2 instance
### 1 Epoch
Training loss: 0.402585595846595846
Training acc: 0.874025763551
Validation loss: 0.291980147362

[[41939   151   105   219   345]
 [  403  1439    45   132    75]
 [  485    53   612    70    48]
 [  886   153    57   843   153]
 [  948    81    18   147  1955]]
Tag: O - P 0.9391 / R 0.9808
Tag: LOC - P 0.7666 / R 0.6872
Tag: MISC - P 0.7312 / R 0.4826
Tag: ORG - P 0.5974 / R 0.4030
Tag: PER - P 0.7589 / R 0.6208
Total time: 105.241132975
Test
=-=-=

### Another restart gives a better total time

[[42050   129    99   228   253]
 [  214  1683    23   120    54]
 [  244    35   905    56    28]
 [  586   100    40  1269    97]
 [  513    39    11    99  2487]]
Tag: O - P 0.9643 / R 0.9834
Tag: LOC - P 0.8474 / R 0.8037
Tag: MISC - P 0.8395 / R 0.7137
Tag: ORG - P 0.7161 / R 0.6066
Tag: PER - P 0.8520 / R 0.7898
Total time: 85.1370520592
Epoch 5
Training loss: 0.0791734457016457016
Training acc: 0.974315026446
Validation loss: 0.22555449605

### A test run with dropout and regularization
Epoch 0
Training loss: 0.446270912886912886
Training acc: 0.867474376415
Validation loss: 0.322937309742

[[41772   167   226   276   318]
 [  311  1389    56   197   141]
 [  366    46   737    83    36]
 [  853   114    76   849   200]
 [  957    80    27   211  1874]]
Tag: O - P 0.9438 / R 0.9769
Tag: LOC - P 0.7734 / R 0.6633
Tag: MISC - P 0.6569 / R 0.5812
Tag: ORG - P 0.5254 / R 0.4058
Tag: PER - P 0.7295 / R 0.5951
Total time: 152.228859901
Test
=-=-=

# Assignment 2 Question 3
## TODO
- [ ] Tweak the logging so that we're not opening more file handles than the default OS allows (1024 is the soft limit)
- [ ] Find better parameters the homework promises we can get to 175 perplexity
- [ ] Finish the generator model
## Results
With pretty default parameters the final test set perplexity is 650
=-==-==-==-==-=
Test perplexity: 650.187072754
=-==-==-==-==-=

## Sentences
Before training
<eos>
in palo alto even nahb years decades ssangyong that kent brief cluett reported asbestos rake high ipo this later nov. mr. rudolph said up banknote
 kia memotec nov. decades berlitz group memotec british <eos>

After training for 32 epochs

<eos>
in palo alto cigarette cancer aer chairman brief mr. sim ipo reported causing the than up caused unusually former ipo pierre kent pierre mr. reported hydro-quebec will make causing said ago centrust gitano it deaths later berlitz nahb show group has fiber chairman ssangyong named causing consolidated fromstein brief mlx wachter N centrust N named board dutch former rubens more gitano has deaths exposed even named rubens inc. high swapo high punts once centrust pierre used plc group up pierre even n.v. ssangyong nahb form said gitano <eos>

Example "conversation"

in palo alto fromstein fiber gold this and
> that there too
that there too the decades cancer more publishing
> about this research
about this research show more fiber ipo nonexecutive
> where do you
where do you regatta fiber N and unusually
> how long is the lake
how long is the lake join make than rake this
> what is jam made of?
what is <unk> made <unk> this pierre regatta hydro-quebec memotec
> do you think you are doing well?
do you think you are doing <unk> nov. of <eos>
> 


## Running Time
On a p2.8xlarge it is minutes :)
