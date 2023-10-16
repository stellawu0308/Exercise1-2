# Exercise1-2
#練習1
def displayInventory(inventory):
    print("裝備：")
    total_items = 0 #裝備總數先預設為0
    for item, quantity in inventory.items():
        print(f"{quantity}  {item}")#f表示在字符串中插入 quantity 和 item 的值
        total_items += quantity #裝備總數等於裝備數量累加
    print(f"裝備總數：{total_items}")

#練習2
def addToInventory(inventory, addedItems):
    for item in addedItems:
        inventory[item] = inventory.get(item, 0) + 1
        #如果 item 在 inventory 这个字典中存在，將返回對應鍵的值。
        #如果 item 在 inventory 中不存在，將返回默認值，即 0。
    return inventory
inventory = {'索仔': 1, '火把': 6, '銀角仔': 42, '刀仔': 1, '箭': 12}
dragonLoot = ['銀角仔', '刀仔', '銀角仔', '銀角仔', '紅寶石']
inventory= addToInventory(inventory, dragonLoot)
displayInventory(inventory)

    
