# Втора лабораториска вежба по Софтверско инженерство

## Вања Петрушевски, бр. на индекс 162004

###  Control Flow Graph

Фотографија од control flow graph-ot:


![162004-CFG](https://user-images.githubusercontent.com/102427437/171392921-18f1f3ce-3e26-421f-a814-9c5d597ae9d6.png)

Код и ознаки што се користени за нодовите во горниот CFG:


```
public class SILab2 {
//1 Start    public static List<String> function(List<String> list) { 			
//2        if (list.size() <= 0) { 																	
//3            throw new IllegalArgumentException("List length should be greater than 0");				
        }
//4        int n = list.size();																		
//5        int rootOfN = (int) Math.sqrt(n);															
//6        if (rootOfN * rootOfN  != n) {																
//7            throw new IllegalArgumentException("List length should be a perfect square");			
        }
//8        List<String> numMines = new ArrayList<>();													
//9 (int i=0 -> 9.1 | i<n -> 9.2 | i++ -> 9.3)        for (int i = 0; i < n; i++) {																
//10            if (!list.get(i).equals("#")) {															
//11                int num = 0;																		
//12                if ( (i % rootOfN != 0 && list.get(i - 1).equals("#")) || (i % rootOfN != rootOfN - 1 && list.get(i + 1).equals("#")) ) {    	
//13                    if ( (i % rootOfN != 0 && list.get(i - 1).equals("#")) && (i % rootOfN != rootOfN - 1 && list.get(i + 1).equals("#")) ){		
//22                        num += 2;																												
                    }
                    else {
//14                        num  += 1;																												
                    }
                }
//15                if (i - rootOfN >= 0 && list.get(i - rootOfN).equals("#")){																		
//19                    num++;																														
                }
//16                if (i + rootOfN < n && list.get(i + rootOfN).equals("#")){																		
//18                   num++;																														
                }
//17                numMines.add(String.valueOf(num));																								
            }
            else {
//20                numMines.add(list.get(i));																										
            }
        }
//21        return numMines;																														
//23 End    }																																			
						}
```
    

																	 
### Цикломатска комплексност

Цикломатската комплексност на овој код е 9, добиена е преку формулата P+1, каде што P е бројот на предикатни јазли. Во случајoв P=8, па цикломатската комплексност изнесува 9.
