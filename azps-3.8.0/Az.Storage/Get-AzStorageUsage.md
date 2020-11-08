---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012266"
---
# <span data-ttu-id="d68a4-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d68a4-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="d68a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d68a4-102">SYNOPSIS</span></span>
<span data-ttu-id="d68a4-103">A jelenlegi előfizetés tárolási erőforrás-felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d68a4-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="d68a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d68a4-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d68a4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d68a4-105">DESCRIPTION</span></span>
<span data-ttu-id="d68a4-106">A **Get-AzStorageUsage** parancsmag az Azure tárterületének erőforrás-kihasználtságát az aktuális előfizetéshez kapja.</span><span class="sxs-lookup"><span data-stu-id="d68a4-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="d68a4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d68a4-107">EXAMPLES</span></span>

### <span data-ttu-id="d68a4-108">Példa 1: meghatározott hely tárolási erőforrásainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="d68a4-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="d68a4-109">Ez a parancs a megadott hely tárolási erőforrásait a jelenlegi előfizetés alatt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d68a4-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="d68a4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d68a4-110">PARAMETERS</span></span>

### <span data-ttu-id="d68a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68a4-111">-DefaultProfile</span></span>
<span data-ttu-id="d68a4-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d68a4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d68a4-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="d68a4-113">-Location</span></span>
<span data-ttu-id="d68a4-114">Jelezze a tárolási erőforrások felhasználását a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="d68a4-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="d68a4-115">Ha nem adja meg, a program az előfizetés alatti minden helyen megkapja a tárterület-erőforrások használatát.</span><span class="sxs-lookup"><span data-stu-id="d68a4-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d68a4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68a4-116">CommonParameters</span></span>
<span data-ttu-id="d68a4-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d68a4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68a4-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d68a4-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68a4-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d68a4-119">INPUTS</span></span>

### <span data-ttu-id="d68a4-120">System. String</span><span class="sxs-lookup"><span data-stu-id="d68a4-120">System.String</span></span>

## <span data-ttu-id="d68a4-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d68a4-121">OUTPUTS</span></span>

### <span data-ttu-id="d68a4-122">Microsoft. Azure. commands. Management. Storage. models. PSUs</span><span class="sxs-lookup"><span data-stu-id="d68a4-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="d68a4-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d68a4-123">NOTES</span></span>

## <span data-ttu-id="d68a4-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d68a4-124">RELATED LINKS</span></span>

[<span data-ttu-id="d68a4-125">Azure Storage Manager-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d68a4-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


