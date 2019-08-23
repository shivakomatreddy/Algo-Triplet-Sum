object Solution extends App {
  
  def find3NumberSum(listOfNums: Seq[Int], targetNumber: Int,
                     combinations: Seq[Int] = Seq(), carryingSum: Int = 0): Seq[Int] = {
    
      if(listOfNums.size == 0) {        
        combinations         
      } else {
        
        val diff = targetNumber - carryingSum 
        
        if(carryingSum <= targetNumber) {
          
          val currentSum = listOfNums.head + carryingSum
          println(listOfNums.head)
          println(currentSum)
          println(targetNumber)
          
          if(currentSum <= targetNumber) {
              find3NumberSum(listOfNums.tail,
                            targetNumber,
                            combinations = Seq(listOfNums.head) ++ combinations,
                            carryingSum = currentSum)
          } else {
            find3NumberSum(listOfNums.tail,
                            targetNumber,
                            combinations,
                            carryingSum)
          }
          
        } else combinations
      }
  }
  
  val combinations = find3NumberSum(Seq(12, 3, 4, 1, 6, 9).sorted(Ordering.Int.reverse), 24)
  println(combinations)
  println(combinations.sum)

}
