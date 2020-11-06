---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: fd4a06375a4dfab7f8b8cd4b08a2112310e99b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504223"
---
# <span data-ttu-id="b54e3-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="b54e3-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="b54e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b54e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b54e3-103">Az összes számítási erőforrás listázása</span><span class="sxs-lookup"><span data-stu-id="b54e3-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b54e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b54e3-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b54e3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b54e3-105">DESCRIPTION</span></span>
<span data-ttu-id="b54e3-106">Az összes számítási erőforrás listázása</span><span class="sxs-lookup"><span data-stu-id="b54e3-106">List all compute resource Skus</span></span>

## <span data-ttu-id="b54e3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b54e3-107">EXAMPLES</span></span>

### <span data-ttu-id="b54e3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b54e3-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="b54e3-109">Az összes számítási erőforrás listázása a Nyugat-amerikai régióban</span><span class="sxs-lookup"><span data-stu-id="b54e3-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="b54e3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b54e3-110">PARAMETERS</span></span>

### <span data-ttu-id="b54e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b54e3-111">-DefaultProfile</span></span>
<span data-ttu-id="b54e3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b54e3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b54e3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b54e3-113">CommonParameters</span></span>
<span data-ttu-id="b54e3-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b54e3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b54e3-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b54e3-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b54e3-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b54e3-116">INPUTS</span></span>

### <span data-ttu-id="b54e3-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="b54e3-117">None</span></span>

## <span data-ttu-id="b54e3-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b54e3-118">OUTPUTS</span></span>

### <span data-ttu-id="b54e3-119">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="b54e3-119">System.Object</span></span>

## <span data-ttu-id="b54e3-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b54e3-120">NOTES</span></span>

## <span data-ttu-id="b54e3-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b54e3-121">RELATED LINKS</span></span>
