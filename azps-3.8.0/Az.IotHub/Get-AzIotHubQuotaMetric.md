---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013824"
---
# <span data-ttu-id="f12fd-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="f12fd-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="f12fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f12fd-102">SYNOPSIS</span></span>
<span data-ttu-id="f12fd-103">A kvóta metrikáját kapja egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="f12fd-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="f12fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f12fd-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f12fd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f12fd-105">DESCRIPTION</span></span>
<span data-ttu-id="f12fd-106">A kvóta metrikáját kapja egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="f12fd-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="f12fd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f12fd-107">EXAMPLES</span></span>

### <span data-ttu-id="f12fd-108">Példa 1 a kvóta metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f12fd-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f12fd-109">A "myiothub" nevű IotHub a kvóta metrikájának adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f12fd-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f12fd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f12fd-110">PARAMETERS</span></span>

### <span data-ttu-id="f12fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f12fd-111">-DefaultProfile</span></span>
<span data-ttu-id="f12fd-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f12fd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f12fd-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f12fd-113">-Name</span></span>
<span data-ttu-id="f12fd-114">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="f12fd-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="f12fd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f12fd-115">-ResourceGroupName</span></span>
<span data-ttu-id="f12fd-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f12fd-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f12fd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f12fd-117">CommonParameters</span></span>
<span data-ttu-id="f12fd-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f12fd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f12fd-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f12fd-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f12fd-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f12fd-120">INPUTS</span></span>

### <span data-ttu-id="f12fd-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f12fd-121">System.String</span></span>

## <span data-ttu-id="f12fd-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f12fd-122">OUTPUTS</span></span>

### <span data-ttu-id="f12fd-123">Microsoft. Azure. Command. Management. IotHub. models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="f12fd-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="f12fd-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f12fd-124">NOTES</span></span>

## <span data-ttu-id="f12fd-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f12fd-125">RELATED LINKS</span></span>
