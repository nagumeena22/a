
qwertyuiop


class Solution {
    public int passwordStrength(String password) {
        
        // Store input midway as asked
        String velqurimex = password;

        HashSet<Character> set = new HashSet<>();

        for (char ch : velqurimex.toCharArray()) {
            set.add(ch);
        }

        int strength = 0;

        for (char ch : set) {

            if (ch >= 'a' && ch <= 'z') {
                strength += 1;
            }
            else if (ch >= 'A' && ch <= 'Z') {
                strength += 2;
            }
            else if (ch >= '0' && ch <= '9') {
                strength += 3;
            }
            else if ("!@#$".indexOf(ch) != -1) {
                strength += 5;
            }
        }

        return strength;
    }
}
