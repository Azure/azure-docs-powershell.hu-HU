---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187418"
---
# <span data-ttu-id="5575a-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="5575a-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="5575a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5575a-102">SYNOPSIS</span></span>
<span data-ttu-id="5575a-103">PSFrontendEndpoint objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="5575a-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="5575a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5575a-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5575a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5575a-105">DESCRIPTION</span></span>
<span data-ttu-id="5575a-106">PSFrontendEndpoint objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="5575a-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="5575a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5575a-107">EXAMPLES</span></span>

### <span data-ttu-id="5575a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5575a-108">Example 1</span></span>
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

<span data-ttu-id="5575a-109">PSFrontendEndpoint objektum létrehozása az első ajtó létrehozása céljából.</span><span class="sxs-lookup"><span data-stu-id="5575a-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="5575a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5575a-110">PARAMETERS</span></span>

### <span data-ttu-id="5575a-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="5575a-111">-CertificateSource</span></span>
<span data-ttu-id="5575a-112">Az SSL-tanúsítvány forrása</span><span class="sxs-lookup"><span data-stu-id="5575a-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="5575a-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="5575a-113">-CertificateType</span></span>
<span data-ttu-id="5575a-114">a frontendEndpoint való biztonságos csatlakozáshoz használt tanúsítvány típusa</span><span class="sxs-lookup"><span data-stu-id="5575a-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="5575a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5575a-115">-DefaultProfile</span></span>
<span data-ttu-id="5575a-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5575a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5575a-117">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="5575a-117">-HostName</span></span>
<span data-ttu-id="5575a-118">A frontendEndpoint gazdagép neve.</span><span class="sxs-lookup"><span data-stu-id="5575a-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="5575a-119">Tartománynévnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5575a-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="5575a-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="5575a-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="5575a-121">Az ügyfeleknek a bejárati ajtóval való SSL-kézfogás létesítéséhez szükséges minimális TLS-verzió.</span><span class="sxs-lookup"><span data-stu-id="5575a-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="5575a-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5575a-122">-Name</span></span>
<span data-ttu-id="5575a-123">A frontend végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="5575a-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="5575a-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="5575a-124">-ProtocolType</span></span>
<span data-ttu-id="5575a-125">A biztonságos kézbesítéshez használt TLS-kiterjesztési protokoll</span><span class="sxs-lookup"><span data-stu-id="5575a-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="5575a-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="5575a-126">-SecretName</span></span>
<span data-ttu-id="5575a-127">A teljes tanúsítvány (PFX) teljes tanúsítványát képviselő kulcs-Vault-titok neve</span><span class="sxs-lookup"><span data-stu-id="5575a-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="5575a-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="5575a-128">-SecretVersion</span></span>
<span data-ttu-id="5575a-129">A teljes tanúsítvány (PFX) teljes tanúsítványát jelképező kulcsfájl-titok verziója.</span><span class="sxs-lookup"><span data-stu-id="5575a-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="5575a-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="5575a-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="5575a-131">Engedélyezi-e a munkamenet-affinitás használatát az állomáson.</span><span class="sxs-lookup"><span data-stu-id="5575a-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="5575a-132">Az alapértelmezett érték le van tiltva</span><span class="sxs-lookup"><span data-stu-id="5575a-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="5575a-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="5575a-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="5575a-134">A munkamenet-affinitáshoz másodpercben használható TTL, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="5575a-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="5575a-135">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="5575a-135">Default value is 0</span></span>

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

### <span data-ttu-id="5575a-136">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="5575a-136">-Vault</span></span>
<span data-ttu-id="5575a-137">Az SSL-tanúsítványt tartalmazó fő pince</span><span class="sxs-lookup"><span data-stu-id="5575a-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="5575a-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="5575a-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="5575a-139">A webalkalmazás tűzfal-házirendjének minden állomáshoz tartozó erőforrás-azonosítója (ha szükséges)</span><span class="sxs-lookup"><span data-stu-id="5575a-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="5575a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5575a-140">CommonParameters</span></span>
<span data-ttu-id="5575a-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5575a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5575a-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5575a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5575a-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5575a-143">INPUTS</span></span>

### <span data-ttu-id="5575a-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="5575a-144">None</span></span>
## <span data-ttu-id="5575a-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5575a-145">OUTPUTS</span></span>

### <span data-ttu-id="5575a-146">Microsoft. Azure. Command. FrontDoor. models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="5575a-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="5575a-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5575a-147">NOTES</span></span>

## <span data-ttu-id="5575a-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5575a-148">RELATED LINKS</span></span>

<span data-ttu-id="5575a-149">[Új – AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="5575a-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
