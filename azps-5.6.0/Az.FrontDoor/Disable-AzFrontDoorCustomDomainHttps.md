---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: e76d4f0da95e8cc315cbbf4218a68f340b2a5e7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938682"
---
# <span data-ttu-id="b5798-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="b5798-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="b5798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5798-102">SYNOPSIS</span></span>
<span data-ttu-id="b5798-103">Egyéni tartomány HTTPS-címének letiltása</span><span class="sxs-lookup"><span data-stu-id="b5798-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="b5798-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5798-104">SYNTAX</span></span>

### <span data-ttu-id="b5798-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5798-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5798-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5798-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5798-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5798-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5798-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5798-108">DESCRIPTION</span></span>
<span data-ttu-id="b5798-109">A **Disable-AzFrontDoorCustomDomainHttps letiltja a HTTPS-t** egy egyéni tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="b5798-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="b5798-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5798-110">EXAMPLES</span></span>

### <span data-ttu-id="b5798-111">1. példa: A HTTPS letiltása a FrontDoorName és a ResourceGroupName egyéni tartomány esetén.</span><span class="sxs-lookup"><span data-stu-id="b5798-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
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

<span data-ttu-id="b5798-112">Tiltsa le a HTTPS-t a "frontendpointname1-custom-xyz" egyéni tartományhoz úgy, hogy a FrontDoorName "frontdoor1" és az ResourceGroupName "resourcegroup1" (erőforráscsoport1) nevet használja.</span><span class="sxs-lookup"><span data-stu-id="b5798-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="b5798-113">2. példa: A HTTPS letiltása egy PSFrontendEndpoint-objektummal létrehozott egyéni tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="b5798-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
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

<span data-ttu-id="b5798-114">A PSFrontendEndpoint-objektum egyéni tartomány esetén tiltsa le a HTTPS-t.</span><span class="sxs-lookup"><span data-stu-id="b5798-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="b5798-115">3. példa: A HTTPS letiltása egyéni tartomány esetén az ResourceId beállítással.</span><span class="sxs-lookup"><span data-stu-id="b5798-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
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

<span data-ttu-id="b5798-116">Tiltsa le a HTTPS-t egy egyéni tartomány "frontendpointname1-custom-xyz" tartományában, amely a ResourceId mint $resourceId.</span><span class="sxs-lookup"><span data-stu-id="b5798-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="b5798-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5798-117">PARAMETERS</span></span>

### <span data-ttu-id="b5798-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5798-118">-DefaultProfile</span></span>
<span data-ttu-id="b5798-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5798-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5798-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="b5798-120">-FrontDoorName</span></span>
<span data-ttu-id="b5798-121">A front door neve.</span><span class="sxs-lookup"><span data-stu-id="b5798-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="b5798-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="b5798-122">-FrontendEndpointName</span></span>
<span data-ttu-id="b5798-123">Frontend endpoint name.</span><span class="sxs-lookup"><span data-stu-id="b5798-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="b5798-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5798-124">-InputObject</span></span>
<span data-ttu-id="b5798-125">A frissítend frontend végpontobjektum.</span><span class="sxs-lookup"><span data-stu-id="b5798-125">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="b5798-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5798-126">-ResourceGroupName</span></span>
<span data-ttu-id="b5798-127">Az az erőforráscsoport, amelyhez a Front Door tartozik.</span><span class="sxs-lookup"><span data-stu-id="b5798-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="b5798-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5798-128">-ResourceId</span></span>
<span data-ttu-id="b5798-129">A https letiltására a Front Door végpont erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b5798-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="b5798-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5798-130">-Confirm</span></span>
<span data-ttu-id="b5798-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b5798-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5798-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5798-132">-WhatIf</span></span>
<span data-ttu-id="b5798-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b5798-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5798-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5798-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5798-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5798-135">CommonParameters</span></span>
<span data-ttu-id="b5798-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5798-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5798-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5798-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5798-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5798-138">INPUTS</span></span>

### <span data-ttu-id="b5798-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b5798-139">System.String</span></span>

## <span data-ttu-id="b5798-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5798-140">OUTPUTS</span></span>

### <span data-ttu-id="b5798-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5798-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="b5798-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5798-142">NOTES</span></span>

## <span data-ttu-id="b5798-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5798-143">RELATED LINKS</span></span>
