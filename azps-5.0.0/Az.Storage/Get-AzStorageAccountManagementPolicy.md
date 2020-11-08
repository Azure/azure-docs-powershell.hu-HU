---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b27d6e8bec4dda2ba87a0b38a9b37a8d4739ae00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195470"
---
# <span data-ttu-id="44a40-101">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="44a40-101">Get-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="44a40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44a40-102">SYNOPSIS</span></span>
<span data-ttu-id="44a40-103">Az Azure Storage-fiók kezelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44a40-103">Gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="44a40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44a40-104">SYNTAX</span></span>

### <span data-ttu-id="44a40-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="44a40-105">AccountName (Default)</span></span>
```
Get-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44a40-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="44a40-106">AccountResourceId</span></span>
```
Get-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44a40-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="44a40-107">AccountObject</span></span>
```
Get-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44a40-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="44a40-108">DESCRIPTION</span></span>
<span data-ttu-id="44a40-109">A **Get-AzStorageAccountManagementPolicy** parancsmag egy Azure-tárterületet tároló fiók kezelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44a40-109">The **Get-AzStorageAccountManagementPolicy** cmdlet gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="44a40-110">Példák</span><span class="sxs-lookup"><span data-stu-id="44a40-110">EXAMPLES</span></span>

### <span data-ttu-id="44a40-111">Példa 1: a tárolási fiók kezelési házirendjének beszerzése.</span><span class="sxs-lookup"><span data-stu-id="44a40-111">Example 1: Get the management policy of a Storage account.</span></span>
```
PS C:\>Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 7:04:05 AM
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

<span data-ttu-id="44a40-112">Ez a parancs a tárolási fiók kezelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44a40-112">This command gets the management policy of a Storage account.</span></span>

## <span data-ttu-id="44a40-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44a40-113">PARAMETERS</span></span>

### <span data-ttu-id="44a40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44a40-114">-DefaultProfile</span></span>
<span data-ttu-id="44a40-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44a40-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44a40-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44a40-116">-ResourceGroupName</span></span>
<span data-ttu-id="44a40-117">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="44a40-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a40-118">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="44a40-118">-StorageAccount</span></span>
<span data-ttu-id="44a40-119">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="44a40-119">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44a40-120">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="44a40-120">-StorageAccountName</span></span>
<span data-ttu-id="44a40-121">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="44a40-121">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a40-122">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="44a40-122">-StorageAccountResourceId</span></span>
<span data-ttu-id="44a40-123">Tárolási fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="44a40-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44a40-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a40-124">CommonParameters</span></span>
<span data-ttu-id="44a40-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44a40-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a40-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44a40-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a40-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44a40-127">INPUTS</span></span>

### <span data-ttu-id="44a40-128">System. String</span><span class="sxs-lookup"><span data-stu-id="44a40-128">System.String</span></span>

## <span data-ttu-id="44a40-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44a40-129">OUTPUTS</span></span>

### <span data-ttu-id="44a40-130">Microsoft. Azure. Management. Storage. models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="44a40-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="44a40-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44a40-131">NOTES</span></span>

## <span data-ttu-id="44a40-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44a40-132">RELATED LINKS</span></span>