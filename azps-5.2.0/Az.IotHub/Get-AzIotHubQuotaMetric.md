---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363059"
---
# <span data-ttu-id="697c9-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="697c9-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="697c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="697c9-102">SYNOPSIS</span></span>
<span data-ttu-id="697c9-103">Egy IotHub kvótametrikákat kap.</span><span class="sxs-lookup"><span data-stu-id="697c9-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="697c9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="697c9-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="697c9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="697c9-105">DESCRIPTION</span></span>
<span data-ttu-id="697c9-106">Egy IotHub kvótametrikákat kap.</span><span class="sxs-lookup"><span data-stu-id="697c9-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="697c9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="697c9-107">EXAMPLES</span></span>

### <span data-ttu-id="697c9-108">1. példa a kvótametrikák leszerzése</span><span class="sxs-lookup"><span data-stu-id="697c9-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="697c9-109">A "myiothub" nevű IotHub metrikus információinak beszerzése</span><span class="sxs-lookup"><span data-stu-id="697c9-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="697c9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="697c9-110">PARAMETERS</span></span>

### <span data-ttu-id="697c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="697c9-111">-DefaultProfile</span></span>
<span data-ttu-id="697c9-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="697c9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="697c9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="697c9-113">-Name</span></span>
<span data-ttu-id="697c9-114">Az IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="697c9-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="697c9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="697c9-115">-ResourceGroupName</span></span>
<span data-ttu-id="697c9-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="697c9-116">Resource Group Name</span></span>

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

### <span data-ttu-id="697c9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="697c9-117">CommonParameters</span></span>
<span data-ttu-id="697c9-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="697c9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="697c9-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="697c9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="697c9-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="697c9-120">INPUTS</span></span>

### <span data-ttu-id="697c9-121">System.String</span><span class="sxs-lookup"><span data-stu-id="697c9-121">System.String</span></span>

## <span data-ttu-id="697c9-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="697c9-122">OUTPUTS</span></span>

### <span data-ttu-id="697c9-123">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="697c9-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="697c9-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="697c9-124">NOTES</span></span>

## <span data-ttu-id="697c9-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="697c9-125">RELATED LINKS</span></span>
