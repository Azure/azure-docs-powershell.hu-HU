---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
ms.openlocfilehash: 5d44fa0a3e0ead373a822ae91080df9bdc60cc50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501335"
---
# <span data-ttu-id="cd983-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="cd983-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="cd983-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd983-102">SYNOPSIS</span></span>
<span data-ttu-id="cd983-103">A jelenlegi előfizetés tárolási erőforrás-felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cd983-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd983-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd983-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd983-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd983-105">DESCRIPTION</span></span>
<span data-ttu-id="cd983-106">A **Get-AzureRmStorageUsage** parancsmag az Azure tárterületének erőforrás-kihasználtságát az aktuális előfizetéshez kapja.</span><span class="sxs-lookup"><span data-stu-id="cd983-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="cd983-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cd983-107">EXAMPLES</span></span>

### <span data-ttu-id="cd983-108">Példa 1: a tárolási erőforrások használatba vételének beszerzése</span><span class="sxs-lookup"><span data-stu-id="cd983-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="cd983-109">Ez a parancs a jelenlegi előfizetés tárolási erőforrásainak felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cd983-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="cd983-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd983-110">PARAMETERS</span></span>

### <span data-ttu-id="cd983-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd983-111">-DefaultProfile</span></span>
<span data-ttu-id="cd983-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd983-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd983-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd983-113">CommonParameters</span></span>
<span data-ttu-id="cd983-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd983-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd983-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd983-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd983-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd983-116">INPUTS</span></span>

### <span data-ttu-id="cd983-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="cd983-117">None</span></span>
<span data-ttu-id="cd983-118">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cd983-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cd983-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd983-119">OUTPUTS</span></span>

### <span data-ttu-id="cd983-120">Microsoft. Azure. commands. Management. Storage. models. PSUs</span><span class="sxs-lookup"><span data-stu-id="cd983-120">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="cd983-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd983-121">NOTES</span></span>

## <span data-ttu-id="cd983-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd983-122">RELATED LINKS</span></span>

[<span data-ttu-id="cd983-123">Azure Storage Manager-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="cd983-123">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


