---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 6cc7de36f51bc2fcb61950aa112c2f426358a506
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209526"
---
# <span data-ttu-id="413cf-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="413cf-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="413cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="413cf-102">SYNOPSIS</span></span>
<span data-ttu-id="413cf-103">Get Front Door load balancer</span><span class="sxs-lookup"><span data-stu-id="413cf-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="413cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="413cf-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="413cf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="413cf-105">DESCRIPTION</span></span>
<span data-ttu-id="413cf-106">A **Get-AzFrontDoor** parancsmagGet az aktuális előfizetés összes meglévő, a megadott információknak megfelelő előlapi ajtókat kap.</span><span class="sxs-lookup"><span data-stu-id="413cf-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="413cf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="413cf-107">EXAMPLES</span></span>

### <span data-ttu-id="413cf-108">1. példa: Az aktuális előfizetés összes FrontDoors-ának lekérte.</span><span class="sxs-lookup"><span data-stu-id="413cf-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
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
FrontDoorId           : {guid}
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

<span data-ttu-id="413cf-109">Szerezze be az aktuális előfizetés összes FrontDoors-ját.</span><span class="sxs-lookup"><span data-stu-id="413cf-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="413cf-110">2. példa: Az aktuális előfizetésben az "rg1" erőforráscsoport összes FrontDoorja lekérte.</span><span class="sxs-lookup"><span data-stu-id="413cf-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
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
FrontDoorId           : {guid}
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

<span data-ttu-id="413cf-111">Szerezze be az aktuális előfizetésben az "rg1" erőforráscsoport összes FrontDoorját.</span><span class="sxs-lookup"><span data-stu-id="413cf-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="413cf-112">3. példa: A FrontDoors lekérte az "rg1" erőforráscsoportot "frontDoor1" névvel az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="413cf-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
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

<span data-ttu-id="413cf-113">Szerezze be a FrontDoorsot az aktuális előfizetésben az "rg1" erőforráscsoport "frontDoor1" névvel.</span><span class="sxs-lookup"><span data-stu-id="413cf-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="413cf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="413cf-114">PARAMETERS</span></span>

### <span data-ttu-id="413cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="413cf-115">-DefaultProfile</span></span>
<span data-ttu-id="413cf-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="413cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="413cf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="413cf-117">-Name</span></span>
<span data-ttu-id="413cf-118">Front Door name.</span><span class="sxs-lookup"><span data-stu-id="413cf-118">Front Door name.</span></span>

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

### <span data-ttu-id="413cf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="413cf-119">-ResourceGroupName</span></span>
<span data-ttu-id="413cf-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="413cf-120">The resource group name.</span></span>

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

### <span data-ttu-id="413cf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413cf-121">CommonParameters</span></span>
<span data-ttu-id="413cf-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="413cf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413cf-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="413cf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413cf-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="413cf-124">INPUTS</span></span>

### <span data-ttu-id="413cf-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="413cf-125">None</span></span>

## <span data-ttu-id="413cf-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="413cf-126">OUTPUTS</span></span>

### <span data-ttu-id="413cf-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="413cf-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="413cf-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="413cf-128">NOTES</span></span>

## <span data-ttu-id="413cf-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="413cf-129">RELATED LINKS</span></span>

<span data-ttu-id="413cf-130">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="413cf-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
