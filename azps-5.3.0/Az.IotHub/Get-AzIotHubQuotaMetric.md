---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480238"
---
# <span data-ttu-id="db161-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="db161-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="db161-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db161-102">SYNOPSIS</span></span>
<span data-ttu-id="db161-103">Egy IotHub kvótametrikákat kap.</span><span class="sxs-lookup"><span data-stu-id="db161-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="db161-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db161-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db161-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db161-105">DESCRIPTION</span></span>
<span data-ttu-id="db161-106">Egy IotHub kvótametrikákat kap.</span><span class="sxs-lookup"><span data-stu-id="db161-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="db161-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db161-107">EXAMPLES</span></span>

### <span data-ttu-id="db161-108">1. példa a kvótametrikák leszerzése</span><span class="sxs-lookup"><span data-stu-id="db161-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="db161-109">A "myiothub" nevű IotHub metrikus információinak beszerzése</span><span class="sxs-lookup"><span data-stu-id="db161-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="db161-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db161-110">PARAMETERS</span></span>

### <span data-ttu-id="db161-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db161-111">-DefaultProfile</span></span>
<span data-ttu-id="db161-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="db161-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db161-113">-Name</span><span class="sxs-lookup"><span data-stu-id="db161-113">-Name</span></span>
<span data-ttu-id="db161-114">Az IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="db161-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="db161-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db161-115">-ResourceGroupName</span></span>
<span data-ttu-id="db161-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="db161-116">Resource Group Name</span></span>

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

### <span data-ttu-id="db161-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db161-117">CommonParameters</span></span>
<span data-ttu-id="db161-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db161-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db161-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db161-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db161-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db161-120">INPUTS</span></span>

### <span data-ttu-id="db161-121">System.String</span><span class="sxs-lookup"><span data-stu-id="db161-121">System.String</span></span>

## <span data-ttu-id="db161-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db161-122">OUTPUTS</span></span>

### <span data-ttu-id="db161-123">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="db161-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="db161-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db161-124">NOTES</span></span>

## <span data-ttu-id="db161-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db161-125">RELATED LINKS</span></span>
