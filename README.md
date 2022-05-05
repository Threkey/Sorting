# 정렬 알고리즘

## 평균시간복잡도

버블 정렬 (Bubble Sort) : O(n^2)

삽입 정렬 (Insertion Sort) : O(n^2)

선택 정렬 (Selection Sort) : O(n^2)

힙 정렬 (Heap Sort) : O(nlogn)

쉘 정렬 (Shell Sort) : 설정한 간격(gap)에 따라 다르다. Hibbard Sequence를 사용하면 O(n^1.5)가 된다고 알려져있다. 이 글에선 Ciura Sequence를 사용했다.

퀵 정렬 (Quick Sort) : O(nlogn)

## 입력데이터

아래는 입력데이터에 사용된 코드이다.

```
    public static int[] input(int mode, int power)
    {
    	int[] arr = new int[(int)Math.pow(2.0, (double)power)];
    	
    	switch(mode) {
    	
    	case 0 : //정렬된 데이터
    		for(int i = 0 ; i < arr.length ; i++)
    			arr[i] = i;
    		
    		break;
    		
    	case 1 : //랜덤 데이터
    		Random rand = new Random();
    		for(int i = 0 ; i < arr.length ; i++)
    			arr[i] = rand.nextInt(arr.length);
    		
    		break;
    		
    	case 2 : //역 정렬 데이터
    		for(int i = 0 ; i < arr.length ; i++)
    			arr[arr.length - 1 - i] = i;
    		
    		break;
    		
    	default : break;
    	
    	}
    	
    	return arr;
    }
```

## 입력데이터에 따른 시간

시간단위는 밀리세컨(ms)이다.


정렬된 데이터
![image](https://user-images.githubusercontent.com/101376843/166920499-396c2e73-02dd-43e6-917a-1774703b8e94.png)


![image](https://user-images.githubusercontent.com/101376843/166920274-5061b64b-e1d4-41bd-8466-2731756028d5.png)



랜덤 데이터
![image](https://user-images.githubusercontent.com/101376843/166920776-afdb1e72-2c7c-43cc-8d68-16a1368f9f38.png)


![image](https://user-images.githubusercontent.com/101376843/166920897-94b86507-8ad8-49a6-83de-7346cf091d12.png)



역정렬 데이터
![image](https://user-images.githubusercontent.com/101376843/166921086-35dd02b3-c1b7-41b9-9853-cdfa17a74543.png)


![image](https://user-images.githubusercontent.com/101376843/166921179-bfd8689a-f02c-4859-afab-1be05e532728.png)
