---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 8c378d7f0b1ac7a753f7f270fd3969eb881c7aec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194772"
---
# <span data-ttu-id="d3033-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d3033-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="d3033-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3033-102">SYNOPSIS</span></span>
<span data-ttu-id="d3033-103">A bejárati ajtó betöltője</span><span class="sxs-lookup"><span data-stu-id="d3033-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="d3033-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3033-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3033-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3033-105">DESCRIPTION</span></span>
<span data-ttu-id="d3033-106">A **Get-AzFrontDoor** cmdletGet beilleszti az összes meglévő ajtót az aktuális előfizetésben, amely megfelel a megadott adatoknak.</span><span class="sxs-lookup"><span data-stu-id="d3033-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="d3033-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d3033-107">EXAMPLES</span></span>

### <span data-ttu-id="d3033-108">Példa 1: a jelenlegi előfizetés összes FrontDoors beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d3033-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
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

<span data-ttu-id="d3033-109">A jelenlegi előfizetés összes FrontDoors beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d3033-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="d3033-110">2. példa: a jelenlegi előfizetésben a "rg1" erőforráscsoport minden FrontDoors beolvasása</span><span class="sxs-lookup"><span data-stu-id="d3033-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
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

<span data-ttu-id="d3033-111">A jelenlegi előfizetésben a "rg1" erőforráscsoport minden FrontDoors beolvasása</span><span class="sxs-lookup"><span data-stu-id="d3033-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="d3033-112">3. példa: a "rg1" nevű erőforráscsoport "frontDoor1" nevű FrontDoors beszerzése a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="d3033-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
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

<span data-ttu-id="d3033-113">A FrontDoors "rg1" nevű erőforráscsoport "frontDoor1" nevű csoportjának beszerzése a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="d3033-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="d3033-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3033-114">PARAMETERS</span></span>

### <span data-ttu-id="d3033-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3033-115">-DefaultProfile</span></span>
<span data-ttu-id="d3033-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3033-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3033-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3033-117">-Name</span></span>
<span data-ttu-id="d3033-118">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="d3033-118">Front Door name.</span></span>

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

### <span data-ttu-id="d3033-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3033-119">-ResourceGroupName</span></span>
<span data-ttu-id="d3033-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d3033-120">The resource group name.</span></span>

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

### <span data-ttu-id="d3033-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3033-121">CommonParameters</span></span>
<span data-ttu-id="d3033-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3033-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3033-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d3033-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3033-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3033-124">INPUTS</span></span>

### <span data-ttu-id="d3033-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="d3033-125">None</span></span>

## <span data-ttu-id="d3033-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3033-126">OUTPUTS</span></span>

### <span data-ttu-id="d3033-127">Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d3033-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="d3033-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3033-128">NOTES</span></span>

## <span data-ttu-id="d3033-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3033-129">RELATED LINKS</span></span>

<span data-ttu-id="d3033-130">[Új – AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="d3033-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
