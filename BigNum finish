//U10416016張哲瑋
import java.util.ArrayList;
import java.util.Collections;

public class BigNum{
    //Datafield
    String SaveNum1;
    String SaveNum2;
    ArrayList<Character> list1 = new ArrayList();
    ArrayList<Character> list2 = new ArrayList();
    ArrayList<Integer> list3 = new ArrayList();
    int digit;
    int bigdigit;
    int LackNum = 0;
    int Carry = 0;
    
    BigNum(String num1,String num2){
        SaveNum1 = num1;
        SaveNum2 = num2;
    }

    
    private void setList1() {
        for(int i = 0;i<SaveNum1.length();i++){
            list1.add(SaveNum1.charAt(i));
        }
    }
    private void setList2() {
        for(int i = 0;i<SaveNum2.length();i++){
            list2.add(SaveNum2.charAt(i));
        }
    }
    
    private void ReverseList(ArrayList<Character> list){
        Collections.reverse(list);
    }
    
    //Main calculate here
    void PrintAnswer(){
        LackNum = SaveNum1.length()-SaveNum2.length();
        if(SaveNum1.length()>SaveNum2.length()) {
			digit = SaveNum2.length();
			bigdigit = SaveNum1.length();
		}
		else if(SaveNum1.length()==SaveNum2.length()) {
			digit = SaveNum2.length();
		}
		else {
			digit = SaveNum1.length();
			bigdigit =SaveNum2.length();
		}
        setList1();
        setList2();
        ReverseList(list1);
        ReverseList(list2);
        list3.add((Character.getNumericValue(list1.get(0))+Character.getNumericValue(list2.get(0)))%10);
        if((Character.getNumericValue(list1.get(0))+Character.getNumericValue(list2.get(0)))>=10) {
            Carry = 1;
        }
        
        for(int i =1; i<digit&&digit>1;i++){
           if(Carry!=0) {
				list3.add((Character.getNumericValue(list1.get(i))+Character.getNumericValue(list2.get(i))+Carry)%10);
				if((Character.getNumericValue(list1.get(i))+Character.getNumericValue(list2.get(i))+Carry)>=10) {
					Carry =1;
				}
				else {
					Carry = 0;
				}
			}
			else{
				list3.add(Character.getNumericValue(list1.get(i))+Character.getNumericValue(list2.get(i))%10);
				if((Character.getNumericValue(list1.get(i))+Character.getNumericValue(list2.get(i)))>=10) {
					Carry = 1;
				}
			}
		} 
        
        if(SaveNum1.length()>SaveNum2.length()) {
            if(Carry!=0&&(bigdigit-digit)==1) {
		list3.add(Carry);
			}
            for(int i = digit;i<bigdigit&&(bigdigit-digit)>1;i++) {
		if(Carry!=0) {
                    list3.add(Character.getNumericValue((list1.get(i))+Carry)%10);
                    if(Character.getNumericValue(list1.get(i+1))+Carry>=10) {
			Carry = 1;
                    }
                    else {
                    Carry = 0;
                    }
		}
                    else {
			list3.add(Character.getNumericValue(list1.get(i)));
                    }
            }
	}
        
        if(list1.size()<list2.size()) {
            if(Carry!=0&&(bigdigit-digit)==1) {
		list3.add(Carry);
            }
            for(int i = digit;i<bigdigit&&(bigdigit-digit)>1;i++) {
                if(Carry!=0) {
                    list3.add((Character.getNumericValue(list2.get(i))+Carry)%10);
			if(Character.getNumericValue(list2.get(i+1))+Carry>=10) {
                            Carry = 1;
			}
			else {
                            Carry = 0;
			}
		}
                else {
                    list3.add(Character.getNumericValue(list2.get(i)));
		}
            }
	}
        Collections.reverse(list3);
        for(int i = 0;i<list3.size();++i) {
			System.out.print(list3.get(i));
	}
    }    
}

        
    


