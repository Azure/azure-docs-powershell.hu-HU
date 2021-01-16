---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: cc07dd366d5c82705a23e3b9276ee9d681c6ae2c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354353"
---
# <span data-ttu-id="1c5a4-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c5a4-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="1c5a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c5a4-102">SYNOPSIS</span></span>
<span data-ttu-id="1c5a4-103">Get a front door frontend endpoint.</span><span class="sxs-lookup"><span data-stu-id="1c5a4-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="1c5a4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1c5a4-104">SYNTAX</span></span>

### <span data-ttu-id="1c5a4-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c5a4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c5a4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c5a4-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c5a4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c5a4-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c5a4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1c5a4-108">DESCRIPTION</span></span>
<span data-ttu-id="1c5a4-109">A **Get-AzFrontDoorFrontendEndpoint** parancsmag az aktuális Front Door erőforrás összes olyan előtér-végpontját megkapja, amely megfelel a megadott információknak.</span><span class="sxs-lookup"><span data-stu-id="1c5a4-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="1c5a4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1c5a4-110">EXAMPLES</span></span>

### <span data-ttu-id="1c5a4-111">1. példa: Szerezze be az összes előtér-végpontot a Front Door "frontdoor1" alkalmazásában, amely az "rg1" erőforráscsoport része.</span><span class="sxs-lookup"><span data-stu-id="1c5a4-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
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

<span data-ttu-id="1c5a4-112">Szerezze be az összes előtér-végpontot a Front Door "frontdoor1" alkalmazásba, amely az "rg1" erőforráscsoport része.</span><span class="sxs-lookup"><span data-stu-id="1c5a4-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="1c5a4-113">2. példa: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span><span class="sxs-lookup"><span data-stu-id="1c5a4-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
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

<span data-ttu-id="1c5a4-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span><span class="sxs-lookup"><span data-stu-id="1c5a4-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="1c5a4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c5a4-115">PARAMETERS</span></span>

### <span data-ttu-id="1c5a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c5a4-116">-DefaultProfile</span></span>
<span data-ttu-id="1c5a4-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c5a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c5a4-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="1c5a4-118">-FrontDoorName</span></span>
<span data-ttu-id="1c5a4-119">Front Door name.</span><span class="sxs-lookup"><span data-stu-id="1c5a4-119">Front Door name.</span></span>

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

### <span data-ttu-id="1c5a4-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="1c5a4-120">-FrontDoorObject</span></span>
<span data-ttu-id="1c5a4-121">A FrontDoor objektum.</span><span class="sxs-lookup"><span data-stu-id="1c5a4-121">The FrontDoor object.</span></span>

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

### <span data-ttu-id="1c5a4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1c5a4-122">-Name</span></span>
<span data-ttu-id="1c5a4-123">Frontend endpoint name.</span><span class="sxs-lookup"><span data-stu-id="1c5a4-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="1c5a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c5a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="1c5a4-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1c5a4-125">The resource group name.</span></span>

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

### <span data-ttu-id="1c5a4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c5a4-126">-ResourceId</span></span>
<span data-ttu-id="1c5a4-127">A front door erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1c5a4-127">Resource Id of the Front Door</span></span>

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

### <span data-ttu-id="1c5a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c5a4-128">CommonParameters</span></span>
<span data-ttu-id="1c5a4-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c5a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c5a4-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c5a4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c5a4-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c5a4-131">INPUTS</span></span>

### <span data-ttu-id="1c5a4-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="1c5a4-132">None</span></span>

## <span data-ttu-id="1c5a4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c5a4-133">OUTPUTS</span></span>

### <span data-ttu-id="1c5a4-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c5a4-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="1c5a4-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1c5a4-135">NOTES</span></span>

## <span data-ttu-id="1c5a4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c5a4-136">RELATED LINKS</span></span>
