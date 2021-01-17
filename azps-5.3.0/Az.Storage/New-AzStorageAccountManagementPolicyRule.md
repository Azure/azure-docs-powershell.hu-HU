---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: c2a20d19676cff15ff26792a81bfc09242c5e4c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469265"
---
# <span data-ttu-id="bd0a8-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="bd0a8-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="bd0a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd0a8-102">SYNOPSIS</span></span>
<span data-ttu-id="bd0a8-103">Létrehoz egy ManagementPolicy szabályobjektumot, amely használható a Set-AzStorageAccountManagementPolicy szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="bd0a8-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="bd0a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd0a8-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd0a8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd0a8-105">DESCRIPTION</span></span>
<span data-ttu-id="bd0a8-106">A **New-AzStorageAccountManagementPolicyRule** parancsmag létrehoz egy ManagementPolicy szabályobjektumot, amely használható a Set-AzStorageAccountManagementPolicy-ban.</span><span class="sxs-lookup"><span data-stu-id="bd0a8-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="bd0a8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd0a8-107">EXAMPLES</span></span>

### <span data-ttu-id="bd0a8-108">1. példa: ManagementPolicy szabályobjektum létrehozása, majd tárhelyfiók beállítása</span><span class="sxs-lookup"><span data-stu-id="bd0a8-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
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

<span data-ttu-id="bd0a8-109">Ez a parancs Egy ManagementPolicy szabályobjektumot hoz létre, és a ManagementPolicy műveletcsoport-objektum 4 műveletet, egy ManagementPolicy-szabályszűrő objektumot tartalmaz, majd állítsa be a szabályt Tárfiókra.</span><span class="sxs-lookup"><span data-stu-id="bd0a8-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="bd0a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd0a8-110">PARAMETERS</span></span>

### <span data-ttu-id="bd0a8-111">-Művelet</span><span class="sxs-lookup"><span data-stu-id="bd0a8-111">-Action</span></span>
<span data-ttu-id="bd0a8-112">A műveletkészletet definiáló objektum.</span><span class="sxs-lookup"><span data-stu-id="bd0a8-112">An object that defines the action set.</span></span>
<span data-ttu-id="bd0a8-113">Az Objektum parancsmaggal Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="bd0a8-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

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

### <span data-ttu-id="bd0a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd0a8-114">-DefaultProfile</span></span>
<span data-ttu-id="bd0a8-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd0a8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd0a8-116">-Disabled</span><span class="sxs-lookup"><span data-stu-id="bd0a8-116">-Disabled</span></span>
<span data-ttu-id="bd0a8-117">Ha be van állítva, a szabály le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="bd0a8-117">The rule is disabled if set it.</span></span>

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

### <span data-ttu-id="bd0a8-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="bd0a8-118">-Filter</span></span>
<span data-ttu-id="bd0a8-119">A szűrőkészletet definiáló objektum.</span><span class="sxs-lookup"><span data-stu-id="bd0a8-119">An object that defines the filter set.</span></span>
<span data-ttu-id="bd0a8-120">Az Objektum parancsmaggal New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="bd0a8-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

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

### <span data-ttu-id="bd0a8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bd0a8-121">-Name</span></span>
<span data-ttu-id="bd0a8-122">A szabálynév alfanumerikus karakterek bármilyen kombinációját tartalmazhatja.</span><span class="sxs-lookup"><span data-stu-id="bd0a8-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="bd0a8-123">A szabálynév megkülönbözteti a kis- és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="bd0a8-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="bd0a8-124">Házirenden belül egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="bd0a8-124">It must be unique within a policy.</span></span>

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

### <span data-ttu-id="bd0a8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd0a8-125">CommonParameters</span></span>
<span data-ttu-id="bd0a8-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd0a8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd0a8-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd0a8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd0a8-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd0a8-128">INPUTS</span></span>

### <span data-ttu-id="bd0a8-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="bd0a8-129">None</span></span>

## <span data-ttu-id="bd0a8-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd0a8-130">OUTPUTS</span></span>

### <span data-ttu-id="bd0a8-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="bd0a8-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="bd0a8-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd0a8-132">NOTES</span></span>

## <span data-ttu-id="bd0a8-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd0a8-133">RELATED LINKS</span></span>
