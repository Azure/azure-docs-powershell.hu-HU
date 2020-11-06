---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: c63573da3c12eb54329d05f49615057d0595b77c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498163"
---
# <span data-ttu-id="db7d4-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="db7d4-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="db7d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db7d4-102">SYNOPSIS</span></span>
<span data-ttu-id="db7d4-103">A jelenlegi előfizetés tárolási erőforrás-felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="db7d4-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db7d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db7d4-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db7d4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db7d4-105">DESCRIPTION</span></span>
<span data-ttu-id="db7d4-106">A **Get-AzureRmStorageUsage** parancsmag az Azure tárterületének erőforrás-kihasználtságát az aktuális előfizetéshez kapja.</span><span class="sxs-lookup"><span data-stu-id="db7d4-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="db7d4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="db7d4-107">EXAMPLES</span></span>

### <span data-ttu-id="db7d4-108">Példa 1: a tárolási erőforrások használatba vételének beszerzése</span><span class="sxs-lookup"><span data-stu-id="db7d4-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="db7d4-109">Ez a parancs a jelenlegi előfizetés tárolási erőforrásainak felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="db7d4-109">This command gets the Storage resources usage of the current subscription.</span></span>
 

### <span data-ttu-id="db7d4-110">2. példa: meghatározott hely tárolási erőforrásainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="db7d4-110">Example 2: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzureRmStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="db7d4-111">Ez a parancs a megadott hely tárolási erőforrásait a jelenlegi előfizetés alatt kapja.</span><span class="sxs-lookup"><span data-stu-id="db7d4-111">This command gets the Storage resources usage of the specified location under the current subscription.</span></span>

## <span data-ttu-id="db7d4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db7d4-112">PARAMETERS</span></span>

### <span data-ttu-id="db7d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db7d4-113">-DefaultProfile</span></span>
<span data-ttu-id="db7d4-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db7d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7d4-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="db7d4-115">-Location</span></span>
<span data-ttu-id="db7d4-116">Jelezze a tárolási erőforrások felhasználását a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="db7d4-116">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="db7d4-117">Ha nem adja meg, a program az előfizetés alatti minden helyen megkapja a tárterület-erőforrások használatát.</span><span class="sxs-lookup"><span data-stu-id="db7d4-117">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db7d4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db7d4-118">CommonParameters</span></span>
<span data-ttu-id="db7d4-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db7d4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db7d4-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db7d4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db7d4-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db7d4-121">INPUTS</span></span>

### <span data-ttu-id="db7d4-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="db7d4-122">None</span></span>

## <span data-ttu-id="db7d4-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db7d4-123">OUTPUTS</span></span>

### <span data-ttu-id="db7d4-124">Microsoft. Azure. commands. Management. Storage. models. PSUs</span><span class="sxs-lookup"><span data-stu-id="db7d4-124">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="db7d4-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db7d4-125">NOTES</span></span>

## <span data-ttu-id="db7d4-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db7d4-126">RELATED LINKS</span></span>

[<span data-ttu-id="db7d4-127">Azure Storage Manager-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="db7d4-127">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


