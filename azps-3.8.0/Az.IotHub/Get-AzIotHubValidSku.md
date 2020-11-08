---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: e0f178c10fa74d8fa230472397d7bcc835f98bf4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013818"
---
# <span data-ttu-id="e8c7d-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="e8c7d-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="e8c7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c7d-103">Beilleszt minden érvényes SKU-t, amelyre a IotHub át tud térni.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="e8c7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8c7d-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8c7d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8c7d-105">DESCRIPTION</span></span>
<span data-ttu-id="e8c7d-106">Megkapja az összes érvényes SKU-ot, amelyre a IotHub át lehet térni.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="e8c7d-107">A IotHub nem tud áttűnést alkalmazni a szabad és a kifizetett SKU között, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="e8c7d-108">Ha ezt el szeretné érni, törölnie kell a iothub, majd újra létre kell hoznia.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="e8c7d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e8c7d-109">EXAMPLES</span></span>

### <span data-ttu-id="e8c7d-110">Példa 1 az érvényes SKU-t beolvasása</span><span class="sxs-lookup"><span data-stu-id="e8c7d-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e8c7d-111">A "myiothub" nevű IotHub tartozó összes SKU listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e8c7d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8c7d-112">PARAMETERS</span></span>

### <span data-ttu-id="e8c7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c7d-113">-DefaultProfile</span></span>
<span data-ttu-id="e8c7d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e8c7d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8c7d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8c7d-115">-Name</span></span>
<span data-ttu-id="e8c7d-116">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-116">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c7d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8c7d-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8c7d-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e8c7d-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c7d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c7d-119">CommonParameters</span></span>
<span data-ttu-id="e8c7d-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8c7d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c7d-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8c7d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c7d-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8c7d-122">INPUTS</span></span>

### <span data-ttu-id="e8c7d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e8c7d-123">System.String</span></span>

## <span data-ttu-id="e8c7d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8c7d-124">OUTPUTS</span></span>

### <span data-ttu-id="e8c7d-125">Microsoft. Azure. Command. Management. IotHub. models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="e8c7d-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="e8c7d-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8c7d-126">NOTES</span></span>

## <span data-ttu-id="e8c7d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8c7d-127">RELATED LINKS</span></span>
