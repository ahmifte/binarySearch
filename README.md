def search(self, nums: List[int], target: int) -> int:
        left = 0 
        right = len(nums)-1
        while left<=right:
            mid_idx = left + (right-left)//2
            if nums[mid_idx]==target:
                return mid_idx
            elif nums[mid_idx]<target:
                left = mid_idx+1
            elif nums[mid_idx]>target:
                right = mid_idx-1
        return -1
