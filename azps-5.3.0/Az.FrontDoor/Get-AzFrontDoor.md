---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 8c378d7f0b1ac7a753f7f270fd3969eb881c7aec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469814"
---
# <span data-ttu-id="e0809-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="e0809-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="e0809-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0809-102">SYNOPSIS</span></span>
<span data-ttu-id="e0809-103">Get Front Door load balancer</span><span class="sxs-lookup"><span data-stu-id="e0809-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="e0809-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0809-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0809-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0809-105">DESCRIPTION</span></span>
<span data-ttu-id="e0809-106">A **Get-AzFrontDoor** parancsmagGet az aktuális előfizetés összes meglévő, a megadott információknak megfelelő előlapi ajtókat kap.</span><span class="sxs-lookup"><span data-stu-id="e0809-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="e0809-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0809-107">EXAMPLES</span></span>

### <span data-ttu-id="e0809-108">1. példa: Az aktuális előfizetés összes FrontDoors-ának lekérte.</span><span class="sxs-lookup"><span data-stu-id="e0809-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid1}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid2}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="e0809-109">Szerezze be az aktuális előfizetés összes FrontDoors-ját.</span><span class="sxs-lookup"><span data-stu-id="e0809-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="e0809-110">2. példa: Az aktuális előfizetésben az "rg1" erőforráscsoport összes FrontDoorja lekérte.</span><span class="sxs-lookup"><span data-stu-id="e0809-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor2
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="e0809-111">Szerezze be az aktuális előfizetésben az "rg1" erőforráscsoport összes FrontDoorját.</span><span class="sxs-lookup"><span data-stu-id="e0809-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="e0809-112">3. példa: A FrontDoors lekérte az "rg1" erőforráscsoportot "frontDoor1" névvel az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e0809-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="e0809-113">Szerezze be a FrontDoorsot az aktuális előfizetésben az "rg1" erőforráscsoport "frontDoor1" névvel.</span><span class="sxs-lookup"><span data-stu-id="e0809-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="e0809-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0809-114">PARAMETERS</span></span>

### <span data-ttu-id="e0809-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0809-115">-DefaultProfile</span></span>
<span data-ttu-id="e0809-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0809-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0809-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e0809-117">-Name</span></span>
<span data-ttu-id="e0809-118">Front Door name.</span><span class="sxs-lookup"><span data-stu-id="e0809-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0809-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0809-119">-ResourceGroupName</span></span>
<span data-ttu-id="e0809-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0809-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0809-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0809-121">CommonParameters</span></span>
<span data-ttu-id="e0809-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0809-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0809-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0809-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0809-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0809-124">INPUTS</span></span>

### <span data-ttu-id="e0809-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="e0809-125">None</span></span>

## <span data-ttu-id="e0809-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0809-126">OUTPUTS</span></span>

### <span data-ttu-id="e0809-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="e0809-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="e0809-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0809-128">NOTES</span></span>

## <span data-ttu-id="e0809-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0809-129">RELATED LINKS</span></span>

<span data-ttu-id="e0809-130">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="e0809-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
