---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
ms.openlocfilehash: 20021b2d557b4590a9853d3124930db27286313a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151906"
---
# <span data-ttu-id="8c68d-101">Get-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="8c68d-101">Get-AzRouteServer</span></span>

## <span data-ttu-id="8c68d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c68d-102">SYNOPSIS</span></span>
<span data-ttu-id="8c68d-103">Azure RouteServer-kiszolgáló kérése</span><span class="sxs-lookup"><span data-stu-id="8c68d-103">Get an Azure RouteServer</span></span>

## <span data-ttu-id="8c68d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c68d-104">SYNTAX</span></span>

### <span data-ttu-id="8c68d-105">RouteServerSubscriptionIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c68d-105">RouteServerSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzRouteServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c68d-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c68d-106">RouteServerNameParameterSet</span></span>
```
Get-AzRouteServer -ResourceGroupName <String> [-RouteServerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c68d-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c68d-107">RouteServerResourceIdParameterSet</span></span>
```
Get-AzRouteServer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c68d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c68d-108">DESCRIPTION</span></span>
<span data-ttu-id="8c68d-109">A **Get-AzRouteServer** parancsmag egy Azure RouteServer-kiszolgálót kap</span><span class="sxs-lookup"><span data-stu-id="8c68d-109">The **Get-AzRouteServer** cmdlet gets an Azure RouteServer</span></span>

## <span data-ttu-id="8c68d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c68d-110">EXAMPLES</span></span>

### <span data-ttu-id="8c68d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8c68d-111">Example 1</span></span>
```powershell
Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="8c68d-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="8c68d-112">Example 2</span></span>
```powershell
$routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Get-AzRouteServer -ResourceId $routeServerId
```
## <span data-ttu-id="8c68d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c68d-113">PARAMETERS</span></span>

### <span data-ttu-id="8c68d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c68d-114">-DefaultProfile</span></span>
<span data-ttu-id="8c68d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c68d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c68d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c68d-116">-ResourceGroupName</span></span>
<span data-ttu-id="8c68d-117">Az útvonal-kiszolgáló erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="8c68d-117">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="8c68d-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c68d-118">-ResourceId</span></span>
<span data-ttu-id="8c68d-119">Az útvonalkiszolgáló Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="8c68d-119">ResourceId of the route server.</span></span>

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

### <span data-ttu-id="8c68d-120">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="8c68d-120">-RouteServerName</span></span>
<span data-ttu-id="8c68d-121">Az útvonalkiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="8c68d-121">The name of the route server.</span></span>

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

### <span data-ttu-id="8c68d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c68d-122">CommonParameters</span></span>
<span data-ttu-id="8c68d-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c68d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c68d-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c68d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c68d-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c68d-125">INPUTS</span></span>

### <span data-ttu-id="8c68d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8c68d-126">System.String</span></span>

## <span data-ttu-id="8c68d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c68d-127">OUTPUTS</span></span>

### <span data-ttu-id="8c68d-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="8c68d-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="8c68d-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c68d-129">NOTES</span></span>

## <span data-ttu-id="8c68d-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c68d-130">RELATED LINKS</span></span>
