---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: f685bb7bdad663e84a67397c89568d2263d0ed9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836177"
---
# <span data-ttu-id="8eb29-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="8eb29-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="8eb29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8eb29-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb29-103">Első ajtós felület végpontjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="8eb29-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="8eb29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8eb29-104">SYNTAX</span></span>

### <span data-ttu-id="8eb29-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8eb29-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8eb29-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8eb29-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8eb29-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8eb29-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8eb29-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8eb29-108">DESCRIPTION</span></span>
<span data-ttu-id="8eb29-109">A **Get-AzFrontDoorFrontendEndpoint** parancsmag minden olyan meglévő felületi végpontot beilleszt az aktuális bejárati ajtó erőforrásában, amely megfelel a megadott adatoknak.</span><span class="sxs-lookup"><span data-stu-id="8eb29-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="8eb29-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8eb29-110">EXAMPLES</span></span>

### <span data-ttu-id="8eb29-111">1. példa: az "frontdoor1", amely a "rg1" erőforráscsoport részét képező "az első ajtó" végpontjának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="8eb29-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="8eb29-112">A bejárati végpontok beszerzése "frontdoor1", amely a "rg1" erőforráscsoport részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8eb29-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="8eb29-113">2. példa: a frontend végpontjának beszerzése "frontdoor1-azurefd-net" néven "frontdoor1", amely a "rg1" erőforráscsoport részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8eb29-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1" -Name "frontdoor1-azurefd-net"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="8eb29-114">A "frontdoor1-azurefd-net" "frontdoor1" nevű "" nevű "rg1" erőforráscsoport része</span><span class="sxs-lookup"><span data-stu-id="8eb29-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="8eb29-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8eb29-115">PARAMETERS</span></span>

### <span data-ttu-id="8eb29-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb29-116">-DefaultProfile</span></span>
<span data-ttu-id="8eb29-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8eb29-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eb29-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8eb29-118">-FrontDoorName</span></span>
<span data-ttu-id="8eb29-119">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="8eb29-119">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb29-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="8eb29-120">-FrontDoorObject</span></span>
<span data-ttu-id="8eb29-121">A FrontDoor objektum.</span><span class="sxs-lookup"><span data-stu-id="8eb29-121">The FrontDoor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb29-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8eb29-122">-Name</span></span>
<span data-ttu-id="8eb29-123">A frontend végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="8eb29-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb29-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eb29-124">-ResourceGroupName</span></span>
<span data-ttu-id="8eb29-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8eb29-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb29-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8eb29-126">-ResourceId</span></span>
<span data-ttu-id="8eb29-127">A bejárati ajtó erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8eb29-127">Resource Id of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb29-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb29-128">CommonParameters</span></span>
<span data-ttu-id="8eb29-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8eb29-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb29-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8eb29-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb29-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8eb29-131">INPUTS</span></span>

### <span data-ttu-id="8eb29-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="8eb29-132">None</span></span>

## <span data-ttu-id="8eb29-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8eb29-133">OUTPUTS</span></span>

### <span data-ttu-id="8eb29-134">Microsoft. Azure. Command. FrontDoor. models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="8eb29-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="8eb29-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8eb29-135">NOTES</span></span>

## <span data-ttu-id="8eb29-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8eb29-136">RELATED LINKS</span></span>
