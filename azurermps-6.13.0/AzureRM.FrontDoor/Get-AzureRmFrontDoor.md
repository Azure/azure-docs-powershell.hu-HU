---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
ms.openlocfilehash: ca54e2cc86daca89a9872366dea32b375080c63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672934"
---
# <span data-ttu-id="83b45-101">Get-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="83b45-101">Get-AzureRmFrontDoor</span></span>

## <span data-ttu-id="83b45-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83b45-102">SYNOPSIS</span></span>
<span data-ttu-id="83b45-103">A bejárati ajtó betöltője</span><span class="sxs-lookup"><span data-stu-id="83b45-103">Get Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83b45-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83b45-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83b45-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="83b45-105">DESCRIPTION</span></span>
<span data-ttu-id="83b45-106">A **Get-AzureRmFrontDoor** cmdletGet beilleszti az összes meglévő ajtót az aktuális előfizetésben, amely megfelel a megadott adatoknak.</span><span class="sxs-lookup"><span data-stu-id="83b45-106">The **Get-AzureRmFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="83b45-107">Példák</span><span class="sxs-lookup"><span data-stu-id="83b45-107">EXAMPLES</span></span>

### <span data-ttu-id="83b45-108">Példa 1: a jelenlegi előfizetés összes FrontDoors beszerzése.</span><span class="sxs-lookup"><span data-stu-id="83b45-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor

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

<span data-ttu-id="83b45-109">A jelenlegi előfizetés összes FrontDoors beszerzése.</span><span class="sxs-lookup"><span data-stu-id="83b45-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="83b45-110">2. példa: a jelenlegi előfizetésben a "rg1" erőforráscsoport minden FrontDoors beolvasása</span><span class="sxs-lookup"><span data-stu-id="83b45-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1"

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

<span data-ttu-id="83b45-111">A jelenlegi előfizetésben a "rg1" erőforráscsoport minden FrontDoors beolvasása</span><span class="sxs-lookup"><span data-stu-id="83b45-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="83b45-112">3. példa: a "rg1" nevű erőforráscsoport "frontDoor1" nevű FrontDoors beszerzése a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="83b45-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

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

<span data-ttu-id="83b45-113">A FrontDoors "rg1" nevű erőforráscsoport "frontDoor1" nevű csoportjának beszerzése a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="83b45-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="83b45-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83b45-114">PARAMETERS</span></span>

### <span data-ttu-id="83b45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b45-115">-DefaultProfile</span></span>
<span data-ttu-id="83b45-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83b45-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83b45-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83b45-117">-Name</span></span>
<span data-ttu-id="83b45-118">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="83b45-118">Front Door name.</span></span>

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

### <span data-ttu-id="83b45-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83b45-119">-ResourceGroupName</span></span>
<span data-ttu-id="83b45-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="83b45-120">The resource group name.</span></span>

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

### <span data-ttu-id="83b45-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b45-121">CommonParameters</span></span>
<span data-ttu-id="83b45-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83b45-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b45-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b45-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b45-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83b45-124">INPUTS</span></span>

### <span data-ttu-id="83b45-125">System. String</span><span class="sxs-lookup"><span data-stu-id="83b45-125">System.String</span></span>

## <span data-ttu-id="83b45-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83b45-126">OUTPUTS</span></span>

### <span data-ttu-id="83b45-127">Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="83b45-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="83b45-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83b45-128">NOTES</span></span>

## <span data-ttu-id="83b45-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83b45-129">RELATED LINKS</span></span>

<span data-ttu-id="83b45-130">[Új – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="83b45-130">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span></span>
