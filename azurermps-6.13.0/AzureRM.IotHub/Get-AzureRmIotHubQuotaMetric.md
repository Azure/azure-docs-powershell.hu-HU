---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: 1de2d49d6e914635f8fc0d38ffa81755cc622481
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680102"
---
# <span data-ttu-id="4fbbd-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="4fbbd-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="4fbbd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fbbd-102">SYNOPSIS</span></span>
<span data-ttu-id="4fbbd-103">A kvóta metrikáját kapja egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="4fbbd-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fbbd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fbbd-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fbbd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fbbd-105">DESCRIPTION</span></span>
<span data-ttu-id="4fbbd-106">A kvóta metrikáját kapja egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="4fbbd-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="4fbbd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4fbbd-107">EXAMPLES</span></span>

### <span data-ttu-id="4fbbd-108">Példa 1 a kvóta metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4fbbd-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4fbbd-109">A "myiothub" nevű IotHub a kvóta metrikájának adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4fbbd-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="4fbbd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fbbd-110">PARAMETERS</span></span>

### <span data-ttu-id="4fbbd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fbbd-111">-DefaultProfile</span></span>
<span data-ttu-id="4fbbd-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4fbbd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fbbd-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4fbbd-113">-Name</span></span>
<span data-ttu-id="4fbbd-114">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="4fbbd-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="4fbbd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fbbd-115">-ResourceGroupName</span></span>
<span data-ttu-id="4fbbd-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="4fbbd-116">Resource Group Name</span></span>

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

### <span data-ttu-id="4fbbd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fbbd-117">CommonParameters</span></span>
<span data-ttu-id="4fbbd-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fbbd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fbbd-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fbbd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fbbd-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fbbd-120">INPUTS</span></span>

### <span data-ttu-id="4fbbd-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4fbbd-121">System.String</span></span>

## <span data-ttu-id="4fbbd-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fbbd-122">OUTPUTS</span></span>

### <span data-ttu-id="4fbbd-123">Microsoft. Azure. Command. Management. IotHub. models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="4fbbd-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="4fbbd-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fbbd-124">NOTES</span></span>

## <span data-ttu-id="4fbbd-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fbbd-125">RELATED LINKS</span></span>
