# CollectionProgram
package com.PsAssignment;

import java.util.LinkedHashMap;
import java.util.Map.Entry;

public class Problem1 {

	public void stringToCollection() {
		LinkedHashMap<String, String> hm = new LinkedHashMap();
		String s = "FName=Isaac|LName=Newton|Address=UK|Age=20|School=Trinity|Invention=LawsOfMotion";
		String[] arr = s.split("[|]");

		for (String s1 : arr) {
			String nw = s1;
			String[] arr1 = nw.split("[=]");

			hm.put(arr1[0], arr1[1]);

		}

		for (Entry<String, String> entry : hm.entrySet()) {

			System.out.println(entry.getKey() + ":" + entry.getValue());
		}
	}

	public static void main(String[] args) {
		Problem1 p = new Problem1();
		p.stringToCollection();
	}

}
