---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: 1ef273329634e080c4117b9ddd0d1eaf8d91bb0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680733"
---
# <span data-ttu-id="cf68b-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="cf68b-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="cf68b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf68b-102">SYNOPSIS</span></span>
<span data-ttu-id="cf68b-103">A jelenlegi előfizetés tárolási erőforrás-felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cf68b-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf68b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf68b-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf68b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf68b-105">DESCRIPTION</span></span>
<span data-ttu-id="cf68b-106">A **Get-AzureRmStorageUsage** parancsmag az Azure tárterületének erőforrás-kihasználtságát az aktuális előfizetéshez kapja.</span><span class="sxs-lookup"><span data-stu-id="cf68b-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="cf68b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cf68b-107">EXAMPLES</span></span>

### <span data-ttu-id="cf68b-108">Példa 1: a tárolási erőforrások használatba vételének beszerzése</span><span class="sxs-lookup"><span data-stu-id="cf68b-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="cf68b-109">Ez a parancs a jelenlegi előfizetés tárolási erőforrásainak felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cf68b-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="cf68b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf68b-110">PARAMETERS</span></span>

### <span data-ttu-id="cf68b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf68b-111">-DefaultProfile</span></span>
<span data-ttu-id="cf68b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf68b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf68b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf68b-113">CommonParameters</span></span>
<span data-ttu-id="cf68b-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf68b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf68b-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf68b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf68b-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf68b-116">INPUTS</span></span>

## <span data-ttu-id="cf68b-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf68b-117">OUTPUTS</span></span>

## <span data-ttu-id="cf68b-118">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf68b-118">NOTES</span></span>

## <span data-ttu-id="cf68b-119">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf68b-119">RELATED LINKS</span></span>

[<span data-ttu-id="cf68b-120">Azure Storage Manager-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="cf68b-120">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


