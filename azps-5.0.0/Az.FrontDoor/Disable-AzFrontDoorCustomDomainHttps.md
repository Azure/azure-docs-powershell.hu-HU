---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 65c9bca6eb678ff3f3cb0a61d815f8415c715e43
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194775"
---
# <span data-ttu-id="cb4ac-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="cb4ac-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="cb4ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb4ac-102">SYNOPSIS</span></span>
<span data-ttu-id="cb4ac-103">HTTPS letiltása egyéni tartományhoz</span><span class="sxs-lookup"><span data-stu-id="cb4ac-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="cb4ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb4ac-104">SYNTAX</span></span>

### <span data-ttu-id="cb4ac-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb4ac-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb4ac-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb4ac-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb4ac-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb4ac-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb4ac-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb4ac-108">DESCRIPTION</span></span>
<span data-ttu-id="cb4ac-109">A **disable-AzFrontDoorCustomDomainHttps** letiltja a HTTPS-t egy egyéni tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="cb4ac-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cb4ac-110">EXAMPLES</span></span>

### <span data-ttu-id="cb4ac-111">1. példa: a HTTPS letiltása egyéni tartományhoz a FrontDoorName és a ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="cb4ac-112">Tiltsa le a HTTPS protokollt az "frontendpointname1-Custom-XYZ" ("frontdoor1") és a ResourceGroupName ("resourcegroup1") FrontDoorName.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="cb4ac-113">2. példa: a HTTPS letiltása egyéni tartományhoz a PSFrontendEndpoint objektummal.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Disable-AzFrontDoorCustomDomainHttps -InputObject $frontendEndpointObj 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="cb4ac-114">Tiltsa le a HTTPS protokollt egy egyéni tartományhoz a PSFrontendEndpoint objektummal.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="cb4ac-115">3. példa: a HTTPS letiltása egyéni tartományhoz a ResourceId-ban.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="cb4ac-116">Tiltsa le a HTTPS protokollt egy "frontendpointname1-Custom-XYZ" egyéni tartományhoz a ResourceId-ban $resourceId.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="cb4ac-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb4ac-117">PARAMETERS</span></span>

### <span data-ttu-id="cb4ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb4ac-118">-DefaultProfile</span></span>
<span data-ttu-id="cb4ac-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb4ac-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="cb4ac-120">-FrontDoorName</span></span>
<span data-ttu-id="cb4ac-121">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="cb4ac-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="cb4ac-122">-FrontendEndpointName</span></span>
<span data-ttu-id="cb4ac-123">A frontend végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="cb4ac-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb4ac-124">-InputObject</span></span>
<span data-ttu-id="cb4ac-125">A frontend végpont objektum a frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-125">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb4ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb4ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="cb4ac-127">Az az erőforráscsoport, amelyhez az első ajtó tartozik.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="cb4ac-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb4ac-128">-ResourceId</span></span>
<span data-ttu-id="cb4ac-129">A https letiltása a bejárati ajtó végpontjának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="cb4ac-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="cb4ac-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cb4ac-130">-Confirm</span></span>
<span data-ttu-id="cb4ac-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb4ac-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb4ac-132">-WhatIf</span></span>
<span data-ttu-id="cb4ac-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb4ac-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb4ac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb4ac-135">CommonParameters</span></span>
<span data-ttu-id="cb4ac-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb4ac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb4ac-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cb4ac-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb4ac-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb4ac-138">INPUTS</span></span>

### <span data-ttu-id="cb4ac-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cb4ac-139">System.String</span></span>

## <span data-ttu-id="cb4ac-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb4ac-140">OUTPUTS</span></span>

### <span data-ttu-id="cb4ac-141">Microsoft. Azure. Command. FrontDoor. models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb4ac-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="cb4ac-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb4ac-142">NOTES</span></span>

## <span data-ttu-id="cb4ac-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb4ac-143">RELATED LINKS</span></span>
