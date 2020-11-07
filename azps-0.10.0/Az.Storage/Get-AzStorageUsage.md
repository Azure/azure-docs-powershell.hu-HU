---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: edf78ad4022b29251d78e976ff7e5d66ae67bb69
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843033"
---
# <span data-ttu-id="ffd2a-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ffd2a-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="ffd2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffd2a-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd2a-103">A jelenlegi előfizetés tárolási erőforrás-felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ffd2a-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="ffd2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffd2a-104">SYNTAX</span></span>

```
Get-AzStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffd2a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffd2a-105">DESCRIPTION</span></span>
<span data-ttu-id="ffd2a-106">A **Get-AzStorageUsage** parancsmag az Azure tárterületének erőforrás-kihasználtságát az aktuális előfizetéshez kapja.</span><span class="sxs-lookup"><span data-stu-id="ffd2a-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="ffd2a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ffd2a-107">EXAMPLES</span></span>

### <span data-ttu-id="ffd2a-108">Példa 1: a tárolási erőforrások használatba vételének beszerzése</span><span class="sxs-lookup"><span data-stu-id="ffd2a-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzStorageUsage
```

<span data-ttu-id="ffd2a-109">Ez a parancs a jelenlegi előfizetés tárolási erőforrásainak felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ffd2a-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="ffd2a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffd2a-110">PARAMETERS</span></span>

### <span data-ttu-id="ffd2a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd2a-111">-DefaultProfile</span></span>
<span data-ttu-id="ffd2a-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffd2a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffd2a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd2a-113">CommonParameters</span></span>
<span data-ttu-id="ffd2a-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffd2a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd2a-115">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffd2a-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd2a-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffd2a-116">INPUTS</span></span>

### <span data-ttu-id="ffd2a-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="ffd2a-117">None</span></span>

## <span data-ttu-id="ffd2a-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffd2a-118">OUTPUTS</span></span>

### <span data-ttu-id="ffd2a-119">Microsoft. Azure. commands. Management. Storage. models. PSUs</span><span class="sxs-lookup"><span data-stu-id="ffd2a-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="ffd2a-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffd2a-120">NOTES</span></span>

## <span data-ttu-id="ffd2a-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffd2a-121">RELATED LINKS</span></span>

[<span data-ttu-id="ffd2a-122">Azure Storage Manager-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ffd2a-122">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


