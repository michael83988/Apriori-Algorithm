# Apriori-Algorithm

"Apriori algorithm" is a method in the region of association rule analysis. One can find some rules which may be like 'if A happens, then B will probably happen too with a probability over xx%' through this algorithm. Here are functions in this module:

## for_test(*args):
Just to show that the module is imported properly if the result is "成功引用Apriori module囉!" and arguments will be shown meanwhile.

## show_param(*args):
Show all global variables in the module:
+ support: The frequency that X -> Y association happens in the dataset. Default value is 0.6.
+ confidence: The probability that X -> Y happens when X happens in the dataset. Default value is 0.6.
+ size: The item count in the frequent itemset. Frequent itemset will increase by 1 through each iteration of the algorithm. Default value is 2.
+ itemset_dict: The dictionary to store the frequent itemset through each iteration of the algorithm. Default is a null dictionay ({}).
+ frequent_itemset_list: The list that store the final frequent itemsets. Default value is a null list ([]).

## clear_param(*args):
To set all global parameters to the default value. This function will be called automatically when `apriori(df)` is called. The purpose of calling this function is to avoid 'ValueError: The truth value of an array with more than one element is ambiguous. Use a.any() or a.all()' error.

## set_param(sup = 0.6, con = 0.6):
Set `support` and `confidence` to specific value according to the argument. If no parameter is delivered, then the default value is 0.6 for both `support` and `confidence`.

## apriori(df):
The main function in this module. To conduct the apriori algorithm, you need to put a `pandas.Dataframe` object as an argument.</br>
The function will return a `pandas.Dataframe` object with columns: ['frequent itemset',  'support', 'antecedent', 'consequent', 'confidence', 'lift'].
