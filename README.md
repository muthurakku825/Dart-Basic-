void main(){
  Map<String, double> products={
    "Notebook":35.0, "Pen":10.3, "Bag":350.5, "Bottle":90.9, "Pencil":20.00
  };
  products.forEach((name, price) {
    showProduct(name,price);
  });
  double total=0;
  for(var price in products.values){
    total=total+price;
  }
  print("Total All product:$total");
  int count=0;
  for(var price in products.values){
    if(price>100){
      count++;
    }
  }
  print("100 more than product cost: $count");
  double average=total/products.length;
  print("Average:$average");
  
  
  if(total>=500){
    double discount=total*0.20;
    print("Discount:$discount");
    total=total-discount;
    print("Final Amount: $total");
  }
  
}
void showProduct(String name,double price){
  print("Product name: $name");
  print("Product price:$price");
  
}
