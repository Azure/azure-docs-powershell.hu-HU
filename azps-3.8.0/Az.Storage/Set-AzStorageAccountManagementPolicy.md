---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/set-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 82faf45a348eb1e84fdc0c577c27a4d68fda3894
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013056"
---
# <span data-ttu-id="4f0b5-101">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4f0b5-101">Set-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="4f0b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f0b5-102">SYNOPSIS</span></span>
<span data-ttu-id="4f0b5-103">Azure-tárterületet tároló fiók kezelési házirendjének létrehozása vagy módosítása.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-103">Creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="4f0b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f0b5-104">SYNTAX</span></span>

### <span data-ttu-id="4f0b5-105">AccountNamePolicyRule (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4f0b5-105">AccountNamePolicyRule (Default)</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Rule <PSManagementPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f0b5-106">AccountNamePolicyObject</span><span class="sxs-lookup"><span data-stu-id="4f0b5-106">AccountNamePolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Policy <PSManagementPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f0b5-107">AccountObjectPolicyRule</span><span class="sxs-lookup"><span data-stu-id="4f0b5-107">AccountObjectPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f0b5-108">AccountObjectPolicyObject</span><span class="sxs-lookup"><span data-stu-id="4f0b5-108">AccountObjectPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f0b5-109">AccountResourceIdPolicyRule</span><span class="sxs-lookup"><span data-stu-id="4f0b5-109">AccountResourceIdPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f0b5-110">AccountResourceIdPolicyObject</span><span class="sxs-lookup"><span data-stu-id="4f0b5-110">AccountResourceIdPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f0b5-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f0b5-111">DESCRIPTION</span></span>
<span data-ttu-id="4f0b5-112">A **set-AzStorageAccountManagementPolicy** parancsmag az Azure Storage-fiók kezelési házirendjét hozza létre vagy módosítja.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-112">The **Set-AzStorageAccountManagementPolicy** cmdlet creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="4f0b5-113">Példák</span><span class="sxs-lookup"><span data-stu-id="4f0b5-113">EXAMPLES</span></span>

### <span data-ttu-id="4f0b5-114">Példa 1: a ManagementPolicy tartalmazó tárterület-fiók felügyeleti házirendjének létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-114">Example 1: Create or update the management policy of a Storage account with ManagementPolicy rule objects.</span></span>
```
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter1 = New-AzStorageAccountManagementPolicyFilter -PrefixMatch ab,cd 
PS C:\>$rule1 = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action1 -Filter $filter1

PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$filter2 = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule2 = New-AzStorageAccountManagementPolicyRule -Name Test2 -Action $action2 -Filter $filter2

PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule1,$rule2


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:29:29 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
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
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="4f0b5-115">Ez a parancs először 2 ManagementPolicy-szabályt hoz létre, majd létrehoz vagy frissít egy tárterület-kezelési házirendet a 2 ManagementPolicy szabály-objektumokkal.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-115">This command first create 2 ManagementPolicy rule objects, then creates or updates the management policy of a Storage account with the 2 ManagementPolicy rule objects.</span></span>

### <span data-ttu-id="4f0b5-116">2. példa: létrehozhatja vagy frissítheti egy, a JSON formátumú házirendet tároló fiók kezelési házirendjét.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-116">Example 2: Create or update the management policy of a Storage account with a Json format policy.</span></span>
```
PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Policy (@{
    Rules=(@{
        Enabled="true";
        Name="Test";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=30;
                    TierToArchive=50;
                    Delete=100;
                });
                Snapshot=(@{
                    Delete=100
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
                PrefixMatch=@("prefix1","prefix2");
            })
        })
    },
    @{
        Enabled="false";
        Name="Test2";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=80;
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
            })
        })
    })
})


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:24:55 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
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
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  80
                                                                                                },
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  null
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="4f0b5-117">Ez a parancs JSON formátumú házirendet hoz létre vagy frissít a tárterület-fiók kezelési házirendjében.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-117">This command creates or updates the management policy of a Storage account with a json format policy.</span></span>

### <span data-ttu-id="4f0b5-118">3. példa: a kezelési házirend beolvasása egy tárterület-fiókból, majd beállítása másik tárterület-fiókra.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-118">Example 3: Get the management policy from a Storage account, then set it to another Storage account.</span></span>
```
PS C:\>$outputPolicy = Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" | Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup2" -AccountName "mystorageaccount2"
```

<span data-ttu-id="4f0b5-119">Ez a parancs először egy tárterület-fiókból kapja meg az adatkezelési házirendet, majd beállítja egy másik tárterület-fiókra.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-119">This command first gets the management policy from a Storage account, then set it to another Storage account.</span></span>

## <span data-ttu-id="4f0b5-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f0b5-120">PARAMETERS</span></span>

### <span data-ttu-id="4f0b5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f0b5-121">-DefaultProfile</span></span>
<span data-ttu-id="4f0b5-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f0b5-123">-Házirend</span><span class="sxs-lookup"><span data-stu-id="4f0b5-123">-Policy</span></span>
<span data-ttu-id="4f0b5-124">Beállítani kívánt kezelési házirend-objektum</span><span class="sxs-lookup"><span data-stu-id="4f0b5-124">Management Policy Object to Set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: AccountNamePolicyObject, AccountObjectPolicyObject, AccountResourceIdPolicyObject
Aliases: ManagementPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0b5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f0b5-125">-ResourceGroupName</span></span>
<span data-ttu-id="4f0b5-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0b5-127">-Szabály</span><span class="sxs-lookup"><span data-stu-id="4f0b5-127">-Rule</span></span>
<span data-ttu-id="4f0b5-128">Az adatkezelési házirend szabályai</span><span class="sxs-lookup"><span data-stu-id="4f0b5-128">The Management Policy rules.</span></span> <span data-ttu-id="4f0b5-129">Az objektum lekérése New-AzStorageAccountManagementPolicyRule parancsmaggal</span><span class="sxs-lookup"><span data-stu-id="4f0b5-129">Get the object with New-AzStorageAccountManagementPolicyRule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule[]
Parameter Sets: AccountNamePolicyRule, AccountObjectPolicyRule, AccountResourceIdPolicyRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0b5-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f0b5-130">-StorageAccount</span></span>
<span data-ttu-id="4f0b5-131">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="4f0b5-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectPolicyRule, AccountObjectPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0b5-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4f0b5-132">-StorageAccountName</span></span>
<span data-ttu-id="4f0b5-133">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0b5-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="4f0b5-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="4f0b5-135">Tárolási fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4f0b5-135">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceIdPolicyRule, AccountResourceIdPolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0b5-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4f0b5-136">-Confirm</span></span>
<span data-ttu-id="4f0b5-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0b5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f0b5-138">-WhatIf</span></span>
<span data-ttu-id="4f0b5-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f0b5-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4f0b5-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0b5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f0b5-141">CommonParameters</span></span>
<span data-ttu-id="4f0b5-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f0b5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f0b5-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f0b5-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f0b5-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f0b5-144">INPUTS</span></span>

### <span data-ttu-id="4f0b5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4f0b5-145">System.String</span></span>

## <span data-ttu-id="4f0b5-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f0b5-146">OUTPUTS</span></span>

### <span data-ttu-id="4f0b5-147">Microsoft. Azure. Command. Management. Storage. models. PSManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4f0b5-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span></span>

## <span data-ttu-id="4f0b5-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f0b5-148">NOTES</span></span>

## <span data-ttu-id="4f0b5-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f0b5-149">RELATED LINKS</span></span>
