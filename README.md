#14. Longest Common Prefix

class Solution {
    func longestCommonPrefix(_ strs: [String]) -> String {
        if strs.isEmpty { return "" }
        
        var prefix = strs[0]
        
        for str in strs.dropFirst() {
            while !str.hasPrefix(prefix) {
                prefix.removeLast()
                if prefix.isEmpty { return "" }
            }
        }
        
        return prefix
    }
}
