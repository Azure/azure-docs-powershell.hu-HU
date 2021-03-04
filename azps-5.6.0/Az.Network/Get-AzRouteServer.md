---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
ms.openlocfilehash: ef5609a34104ca8502b8e4ce96fe294a4714366d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919649"
---
# <span data-ttu-id="f2076-101">Get-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="f2076-101">Get-AzRouteServer</span></span>

## <span data-ttu-id="f2076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2076-102">SYNOPSIS</span></span>
<span data-ttu-id="f2076-103">Azure RouteServer-kiszolgáló kérése</span><span class="sxs-lookup"><span data-stu-id="f2076-103">Get an Azure RouteServer</span></span>

## <span data-ttu-id="f2076-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2076-104">SYNTAX</span></span>

### <span data-ttu-id="f2076-105">RouteServerSubscriptionIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2076-105">RouteServerSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzRouteServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2076-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2076-106">RouteServerNameParameterSet</span></span>
```
Get-AzRouteServer -ResourceGroupName <String> [-RouteServerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2076-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2076-107">RouteServerResourceIdParameterSet</span></span>
```
Get-AzRouteServer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2076-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2076-108">DESCRIPTION</span></span>
<span data-ttu-id="f2076-109">A **Get-AzRouteServer** parancsmag egy Azure RouteServer-kiszolgálót kap</span><span class="sxs-lookup"><span data-stu-id="f2076-109">The **Get-AzRouteServer** cmdlet gets an Azure RouteServer</span></span>

## <span data-ttu-id="f2076-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2076-110">EXAMPLES</span></span>

### <span data-ttu-id="f2076-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f2076-111">Example 1</span></span>
```powershell
Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="f2076-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="f2076-112">Example 2</span></span>
```powershell
$routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Get-AzRouteServer -ResourceId $routeServerId
```
## <span data-ttu-id="f2076-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2076-113">PARAMETERS</span></span>

### <span data-ttu-id="f2076-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2076-114">-DefaultProfile</span></span>
<span data-ttu-id="f2076-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2076-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2076-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2076-116">-ResourceGroupName</span></span>
<span data-ttu-id="f2076-117">Az útvonal-kiszolgáló erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="f2076-117">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2076-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2076-118">-ResourceId</span></span>
<span data-ttu-id="f2076-119">Az útvonalkiszolgáló Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="f2076-119">ResourceId of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2076-120">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="f2076-120">-RouteServerName</span></span>
<span data-ttu-id="f2076-121">Az útvonalkiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f2076-121">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2076-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2076-122">CommonParameters</span></span>
<span data-ttu-id="f2076-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2076-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2076-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2076-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2076-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2076-125">INPUTS</span></span>

### <span data-ttu-id="f2076-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f2076-126">System.String</span></span>

## <span data-ttu-id="f2076-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2076-127">OUTPUTS</span></span>

### <span data-ttu-id="f2076-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="f2076-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="f2076-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2076-129">NOTES</span></span>

## <span data-ttu-id="f2076-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2076-130">RELATED LINKS</span></span>
