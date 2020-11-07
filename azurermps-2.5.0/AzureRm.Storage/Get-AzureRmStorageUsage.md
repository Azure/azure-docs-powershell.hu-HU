---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
ms.openlocfilehash: ae6524c46ed97563e7bf6c948f550a393d74f582
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848985"
---
# <span data-ttu-id="41617-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="41617-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="41617-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41617-102">SYNOPSIS</span></span>
<span data-ttu-id="41617-103">A jelenlegi előfizetés tárolási erőforrás-felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41617-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41617-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41617-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41617-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="41617-105">DESCRIPTION</span></span>
<span data-ttu-id="41617-106">A **Get-AzureRmStorageUsage** parancsmag az Azure tárterületének erőforrás-kihasználtságát az aktuális előfizetéshez kapja.</span><span class="sxs-lookup"><span data-stu-id="41617-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="41617-107">Példák</span><span class="sxs-lookup"><span data-stu-id="41617-107">EXAMPLES</span></span>

### <span data-ttu-id="41617-108">Példa 1: a tárolási erőforrások használatba vételének beszerzése</span><span class="sxs-lookup"><span data-stu-id="41617-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="41617-109">Ez a parancs a jelenlegi előfizetés tárolási erőforrásainak felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41617-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="41617-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41617-110">PARAMETERS</span></span>

### <span data-ttu-id="41617-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41617-111">-DefaultProfile</span></span>
<span data-ttu-id="41617-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41617-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41617-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41617-113">CommonParameters</span></span>
<span data-ttu-id="41617-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41617-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41617-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41617-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41617-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41617-116">INPUTS</span></span>

### <span data-ttu-id="41617-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="41617-117">None</span></span>

## <span data-ttu-id="41617-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41617-118">OUTPUTS</span></span>

### <span data-ttu-id="41617-119">Microsoft. Azure. commands. Management. Storage. models. PSUs</span><span class="sxs-lookup"><span data-stu-id="41617-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="41617-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41617-120">NOTES</span></span>

## <span data-ttu-id="41617-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41617-121">RELATED LINKS</span></span>

[<span data-ttu-id="41617-122">Azure Storage Manager-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="41617-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


