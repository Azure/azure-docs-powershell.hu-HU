---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167538"
---
# <span data-ttu-id="a0386-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="a0386-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="a0386-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0386-102">SYNOPSIS</span></span>
<span data-ttu-id="a0386-103">PSFrontendEndpoint-objektum létrehozása a front door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="a0386-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="a0386-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a0386-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0386-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a0386-105">DESCRIPTION</span></span>
<span data-ttu-id="a0386-106">PSFrontendEndpoint-objektum létrehozása a front door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="a0386-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="a0386-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a0386-107">EXAMPLES</span></span>

### <span data-ttu-id="a0386-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a0386-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName "frontendendpoint1"


HostName                         : frontendendpoint1
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                :
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
ProtocolType                     : ServerNameIndication
```

<span data-ttu-id="a0386-109">PSFrontendEndpoint-objektum létrehozása a front door létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="a0386-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="a0386-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0386-110">PARAMETERS</span></span>

### <span data-ttu-id="a0386-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="a0386-111">-CertificateSource</span></span>
<span data-ttu-id="a0386-112">Az SSL-tanúsítvány forrása</span><span class="sxs-lookup"><span data-stu-id="a0386-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="a0386-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="a0386-113">-CertificateType</span></span>
<span data-ttu-id="a0386-114">a frontendEndpointtal létesített biztonságos kapcsolatokhoz használt tanúsítvány típusa</span><span class="sxs-lookup"><span data-stu-id="a0386-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="a0386-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0386-115">-DefaultProfile</span></span>
<span data-ttu-id="a0386-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0386-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0386-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="a0386-117">-HostName</span></span>
<span data-ttu-id="a0386-118">A frontendEndpoint állomásneve.</span><span class="sxs-lookup"><span data-stu-id="a0386-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="a0386-119">Tartománynévnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a0386-119">Must be a domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0386-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a0386-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="a0386-121">Az SSL-kézbeszélőnek a Front Door segítségével való létesítéséhez az ügyfelek által megkövetelt minimális TLS-verzió.</span><span class="sxs-lookup"><span data-stu-id="a0386-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="a0386-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a0386-122">-Name</span></span>
<span data-ttu-id="a0386-123">Frontend endpoint name.</span><span class="sxs-lookup"><span data-stu-id="a0386-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0386-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="a0386-124">-ProtocolType</span></span>
<span data-ttu-id="a0386-125">A biztonságos kézbesítéshez használt TLS-bővítmény protokoll</span><span class="sxs-lookup"><span data-stu-id="a0386-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="a0386-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="a0386-126">-SecretName</span></span>
<span data-ttu-id="a0386-127">A pfX teljes tanúsítványt képviselő kulcstároló-titkos kulcs neve</span><span class="sxs-lookup"><span data-stu-id="a0386-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="a0386-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="a0386-128">-SecretVersion</span></span>
<span data-ttu-id="a0386-129">A kulcstároló titkos verziója, amely a teljes PFX tanúsítványt képviseli</span><span class="sxs-lookup"><span data-stu-id="a0386-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="a0386-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="a0386-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="a0386-131">Engedélyezi-e a munkamenet-affinitást ezen az állomáson.</span><span class="sxs-lookup"><span data-stu-id="a0386-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="a0386-132">Az alapértelmezett érték le van tiltva</span><span class="sxs-lookup"><span data-stu-id="a0386-132">Default value is Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0386-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="a0386-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="a0386-134">A munkamenet affinitása esetén másodpercben használható TTL.</span><span class="sxs-lookup"><span data-stu-id="a0386-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="a0386-135">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="a0386-135">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0386-136">-Vault</span><span class="sxs-lookup"><span data-stu-id="a0386-136">-Vault</span></span>
<span data-ttu-id="a0386-137">Az SSL-tanúsítványt tartalmazó kulcstároló</span><span class="sxs-lookup"><span data-stu-id="a0386-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="a0386-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="a0386-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="a0386-139">A webalkalmazás tűzfal házirendje erőforrás-azonosítója az egyes gazdakiszolgálókhoz (ha van ilyen)</span><span class="sxs-lookup"><span data-stu-id="a0386-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="a0386-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0386-140">CommonParameters</span></span>
<span data-ttu-id="a0386-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0386-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0386-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0386-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0386-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0386-143">INPUTS</span></span>

### <span data-ttu-id="a0386-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="a0386-144">None</span></span>
## <span data-ttu-id="a0386-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0386-145">OUTPUTS</span></span>

### <span data-ttu-id="a0386-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0386-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="a0386-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a0386-147">NOTES</span></span>

## <span data-ttu-id="a0386-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0386-148">RELATED LINKS</span></span>

<span data-ttu-id="a0386-149">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="a0386-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
