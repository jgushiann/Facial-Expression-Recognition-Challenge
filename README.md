# Facial-Expression-Recognition-Challenge
### Kaggle-ს კონკურსის მიმოხილვა
Facial Expression Recognition Challenge პროექტის მთავარი ამოცანაა 48x48 პიქსელის პორტრეტებიდან 7 ემოციის ამოცნობა: გაბრაზება, ზიზღი, შიში, ბედნიერება, მოწყენა, გაკვირვება და ნეიტრალური.

### ჩემი მიდგომა პრობლემის გადასაჭრელად
ამოცანის გადაჭრა დავიწყე მარტივი cnn არქიტექტურით. ნელნელა ვართულებდი შრეების დამატებით, რაც აისახა მოდელის პერფორმანსზეც (გაუმჯობესდა). ყველა ექსპერიმენტი დავლოგე wandb-ზე შემდეგი ანალიზისათვის.

### რეპოზიტორიის სტრუქტურა
1. FRE Report_facial-expression-recognition - Weights&Biases.pdf - wandb-ის რეპორტი
2. facialRecognition.ipynb - ძირითადი ფაილი, სადაც მოდელს ვატრენინგებთ
3. README.md - ინსტრუქცია

### Feature Engineering
feature engineering-ის ეტაპზე სურათები დავაედითე, "გადავაკეთე" ისე, რომ ერთი და იგივე ზომის იყოს ყველა. კლასები რომ ნაკლებად არაბალანსირებული ყოფილიყო, თითოეულ კლასი შევზღუდე მაქს. 1000 სემპლამდე. 

### Feature Selection
დატას ვიზუალიზაცია-ანალიზისათვის გამოვიყენე bar chart-ები, რათა მენახა როგორ იყო კლასები განაწილებული (დისბალანსის სანახავად). გამოვიყენე სამი სახის არქიტექტურა - simpleCNN, improvedCNN და deepCNN. 

### Model Training
1. simpleCNN მოდელისთვის (დატესტილი 3 მოდელიდან) საუკეთესო შედეგი ჰქონდა მოდელს პარამეტრებით:
  model = simple_cnn
  learning rate = 0.001
  batch size = 64
  Train Loss: 1.4220, Train Acc: 45.04%
  Val Loss: 1.4448, Val Acc: 44.79%
  Learning Rate: 0.000100
 
2. imporovedCNN მოდელისთვის (დატესტილი 3 მოდელიდან) საუკეთესო შედეგი ჰქონდა მოდელს პარამეტრებით:
   model = improved_cnn
   learning rate = 0.001
   batch size = 64
   Train Loss: 1.2624, Train Acc: 52.71%
   Val Loss: 1.2949, Val Acc: 50.72%
   Learning Rate: 0.000100

3. deepCNN მოდელისთვის (დატესტილი 2 მოდელიდან) საუკეთესო შედეგი ჰქონდა მოდელს პარამეტრებით:
   model = deep_cnn
   learning rate = 0.001
   batch size =  64
   Train Loss: 0.9462, Train Acc: 65.43%
   Val Loss: 1.1624, Val Acc: 57.01%
   Learning Rate: 0.000100

  
