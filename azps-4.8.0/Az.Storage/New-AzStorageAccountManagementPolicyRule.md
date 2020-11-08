---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: c2a20d19676cff15ff26792a81bfc09242c5e4c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183804"
---
# <span data-ttu-id="36e73-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="36e73-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="36e73-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36e73-102">SYNOPSIS</span></span>
<span data-ttu-id="36e73-103">Létrehoz egy ManagementPolicy-szabályt, amelyet a set-AzStorageAccountManagementPolicy használhat.</span><span class="sxs-lookup"><span data-stu-id="36e73-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="36e73-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36e73-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36e73-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36e73-105">DESCRIPTION</span></span>
<span data-ttu-id="36e73-106">A **New-AzStorageAccountManagementPolicyRule** parancsmag létrehoz egy ManagementPolicy szabály-objektumot, amelyet a set-AzStorageAccountManagementPolicy használhat.</span><span class="sxs-lookup"><span data-stu-id="36e73-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="36e73-107">Példák</span><span class="sxs-lookup"><span data-stu-id="36e73-107">EXAMPLES</span></span>

### <span data-ttu-id="36e73-108">Példa 1: ManagementPolicy szabály objektum létrehozása, majd tárolási fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="36e73-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2

PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name rule1 -Action $action -Filter $filter
PS C:\>$rule

Enabled    : True
Name       : rule1
Definition : {
                 "Actions":  {
                                 "BaseBlob":  {
                                                  "TierToCool":  {
                                                                     "DaysAfterModificationGreaterThan":  30
                                                                 },
                                                  "TierToArchive":  {
                                                                        "DaysAfterModificationGreaterThan":  50
                                                                    },
                                                  "Delete":  {
                                                                 "DaysAfterModificationGreaterThan":  100
                                                             }
                                              },
                                 "Snapshot":  {
                                                  "Delete":  {
                                                                 "DaysAfterCreationGreaterThan":  100
                                                             }
                                              }
                             },
                 "Filters":  {
                                 "PrefixMatch":  [
                                                     "blobprefix1",
                                                     "blobprefix2"
                                                 ],
                                 "BlobTypes":  [
                                                   "blockBlob"
                                               ]
                             }
             }

PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="36e73-109">Ezzel a paranccsal létrehozhatja a ManagementPolicy szabály objektumát, és egy ManagementPolicy-műveleti csoport objektum négy műveletet tartalmaz, amely egy ManagementPolicy szabály szűrő objektuma, majd a szabály beállítása egy tárterület-fiókra.</span><span class="sxs-lookup"><span data-stu-id="36e73-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="36e73-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36e73-110">PARAMETERS</span></span>

### <span data-ttu-id="36e73-111">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="36e73-111">-Action</span></span>
<span data-ttu-id="36e73-112">Egy objektum, amely meghatározza a Művelettípus beállítását.</span><span class="sxs-lookup"><span data-stu-id="36e73-112">An object that defines the action set.</span></span>
<span data-ttu-id="36e73-113">Az objektum lekérése parancsmaggal Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="36e73-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36e73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e73-114">-DefaultProfile</span></span>
<span data-ttu-id="36e73-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36e73-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e73-116">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="36e73-116">-Disabled</span></span>
<span data-ttu-id="36e73-117">A szabály a beállítás letiltása esetén le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="36e73-117">The rule is disabled if set it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e73-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="36e73-118">-Filter</span></span>
<span data-ttu-id="36e73-119">Egy objektum, amely meghatározza a szűrő halmazát.</span><span class="sxs-lookup"><span data-stu-id="36e73-119">An object that defines the filter set.</span></span>
<span data-ttu-id="36e73-120">Az objektum lekérése parancsmaggal New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="36e73-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36e73-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36e73-121">-Name</span></span>
<span data-ttu-id="36e73-122">Egy szabály neve alfa-numerikus karakterek tetszőleges kombinációját tartalmazhatja.</span><span class="sxs-lookup"><span data-stu-id="36e73-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="36e73-123">A szabály neve megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="36e73-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="36e73-124">Egy házirenden belül egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="36e73-124">It must be unique within a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e73-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e73-125">CommonParameters</span></span>
<span data-ttu-id="36e73-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36e73-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e73-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36e73-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e73-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36e73-128">INPUTS</span></span>

### <span data-ttu-id="36e73-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="36e73-129">None</span></span>

## <span data-ttu-id="36e73-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36e73-130">OUTPUTS</span></span>

### <span data-ttu-id="36e73-131">Microsoft. Azure. Command. Management. Storage. models. PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="36e73-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="36e73-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36e73-132">NOTES</span></span>

## <span data-ttu-id="36e73-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36e73-133">RELATED LINKS</span></span>
