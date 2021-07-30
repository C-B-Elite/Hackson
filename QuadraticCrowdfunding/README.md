二次众筹：
总结：
解决的问题：
  在投票时， 避免多数人暴政以及众筹机制中，传统的投入钱多就可以拥有更多的选票，导致无法满足大多数人的想法。
  
机制详述：
每个人初始有100个选票Token，暂且称为XPT（选票Token）
投票时， 每个人投票与消耗的XPT间的关系为 ： 
  投票数 = (XPT)**2

机制设计：
获取初始票数 vote = ( your_money / total_money ) * total_vote
每次对一个proposul进行投票 ： cost = ( vote_number )^2
剩余的vote 数 = vote - cost = vote - vote_number ^ 2
assert(vote >= 0)
每个propusul 的 vote 数 = vote_number
最终胜出的propusul ： max( same_type_propusul )  

设计：

每个propusul : 
type : text
vote_number : uint
proposul head : text
propusul content : text
propusul sponsor ： text
propusul id : uint

发起propusul程序：

upload_propusul(propusul_type : text, vote_number : uint, proposul_head : text, propusul_content : text, propusul_sponsor : text ) -> bool {};

vote_proposul(propusul_id : uint, vote_number : uint, vote_people : addr_ ) : bool{};

propusul_win() : [propusul_id]{
propusul_id = max({same_type_propusuol})
return [propusul_id]
}

distribution_money


众筹：



NFT：信用积累的凭证
NFT可以参考一下NNS投票，神经元跟随这一块儿
NFT - 信誉， 可以颁发NFT信誉奖章， 可以避免有人使用多个账号， 因为如果使用多个账号， 那么就不能
