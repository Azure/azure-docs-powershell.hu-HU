---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: f2d7c10e29209870d4aa6e5176731b07f7695aff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843958"
---
# <span data-ttu-id="255b2-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="255b2-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="255b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="255b2-102">SYNOPSIS</span></span>
<span data-ttu-id="255b2-103">Beilleszt minden érvényes SKU-t, amelyre a IotHub át tud térni.</span><span class="sxs-lookup"><span data-stu-id="255b2-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="255b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="255b2-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="255b2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="255b2-105">DESCRIPTION</span></span>
<span data-ttu-id="255b2-106">Megkapja az összes érvényes SKU-ot, amelyre a IotHub át lehet térni.</span><span class="sxs-lookup"><span data-stu-id="255b2-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="255b2-107">A IotHub nem tud áttűnést alkalmazni a szabad és a kifizetett SKU között, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="255b2-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="255b2-108">Ha ezt el szeretné érni, törölnie kell a iothub, majd újra létre kell hoznia.</span><span class="sxs-lookup"><span data-stu-id="255b2-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="255b2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="255b2-109">EXAMPLES</span></span>

### <span data-ttu-id="255b2-110">Példa 1 az érvényes SKU-t beolvasása</span><span class="sxs-lookup"><span data-stu-id="255b2-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="255b2-111">A "myiothub" nevű IotHub tartozó összes SKU listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="255b2-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="255b2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="255b2-112">PARAMETERS</span></span>

### <span data-ttu-id="255b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="255b2-113">-DefaultProfile</span></span>
<span data-ttu-id="255b2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="255b2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="255b2-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="255b2-115">-Name</span></span>
<span data-ttu-id="255b2-116">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="255b2-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="255b2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="255b2-117">-ResourceGroupName</span></span>
<span data-ttu-id="255b2-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="255b2-118">Resource Group Name</span></span>

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

### <span data-ttu-id="255b2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="255b2-119">CommonParameters</span></span>
<span data-ttu-id="255b2-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="255b2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="255b2-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="255b2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="255b2-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="255b2-122">INPUTS</span></span>

### <span data-ttu-id="255b2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="255b2-123">System.String</span></span>

## <span data-ttu-id="255b2-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="255b2-124">OUTPUTS</span></span>

### <span data-ttu-id="255b2-125">Microsoft. Azure. Command. Management. IotHub. models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="255b2-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="255b2-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="255b2-126">NOTES</span></span>

## <span data-ttu-id="255b2-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="255b2-127">RELATED LINKS</span></span>
