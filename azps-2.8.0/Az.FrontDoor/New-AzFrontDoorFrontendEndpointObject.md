---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 3684c7d0cf28c0814178ea234f9368d138fc78d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666424"
---
# <span data-ttu-id="05c2c-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="05c2c-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="05c2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="05c2c-103">PSFrontendEndpoint objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="05c2c-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="05c2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05c2c-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-ProtocolType <String>]
 [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>] [-CertificateType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05c2c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="05c2c-105">DESCRIPTION</span></span>
<span data-ttu-id="05c2c-106">PSFrontendEndpoint objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="05c2c-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="05c2c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="05c2c-107">EXAMPLES</span></span>

### <span data-ttu-id="05c2c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="05c2c-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


HostName                         : frontdoor5.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  : Shared
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
```

<span data-ttu-id="05c2c-109">PSFrontendEndpoint objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="05c2c-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="05c2c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05c2c-110">PARAMETERS</span></span>

### <span data-ttu-id="05c2c-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="05c2c-111">-CertificateSource</span></span>
<span data-ttu-id="05c2c-112">Az SSL-tanúsítvány forrása</span><span class="sxs-lookup"><span data-stu-id="05c2c-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="05c2c-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="05c2c-113">-CertificateType</span></span>
<span data-ttu-id="05c2c-114">a frontendEndpoint való biztonságos csatlakozáshoz használt tanúsítvány típusa</span><span class="sxs-lookup"><span data-stu-id="05c2c-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="05c2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c2c-115">-DefaultProfile</span></span>
<span data-ttu-id="05c2c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05c2c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05c2c-117">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="05c2c-117">-HostName</span></span>
<span data-ttu-id="05c2c-118">A frontendEndpoint gazdagép neve.</span><span class="sxs-lookup"><span data-stu-id="05c2c-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="05c2c-119">Tartománynévnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="05c2c-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="05c2c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05c2c-120">-Name</span></span>
<span data-ttu-id="05c2c-121">A frontend végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="05c2c-121">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="05c2c-122">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="05c2c-122">-ProtocolType</span></span>
<span data-ttu-id="05c2c-123">A biztonságos kézbesítéshez használt TLS-kiterjesztési protokoll</span><span class="sxs-lookup"><span data-stu-id="05c2c-123">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="05c2c-124">-SecretName</span><span class="sxs-lookup"><span data-stu-id="05c2c-124">-SecretName</span></span>
<span data-ttu-id="05c2c-125">A teljes tanúsítvány (PFX) teljes tanúsítványát képviselő kulcs-Vault-titok neve</span><span class="sxs-lookup"><span data-stu-id="05c2c-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="05c2c-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="05c2c-126">-SecretVersion</span></span>
<span data-ttu-id="05c2c-127">A teljes tanúsítvány (PFX) teljes tanúsítványát jelképező kulcsfájl-titok verziója.</span><span class="sxs-lookup"><span data-stu-id="05c2c-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="05c2c-128">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="05c2c-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="05c2c-129">Engedélyezi-e a munkamenet-affinitás használatát az állomáson.</span><span class="sxs-lookup"><span data-stu-id="05c2c-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="05c2c-130">Az alapértelmezett érték le van tiltva</span><span class="sxs-lookup"><span data-stu-id="05c2c-130">Default value is Disabled</span></span>

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

### <span data-ttu-id="05c2c-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="05c2c-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="05c2c-132">A munkamenet-affinitáshoz másodpercben használható TTL, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="05c2c-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="05c2c-133">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="05c2c-133">Default value is 0</span></span>

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

### <span data-ttu-id="05c2c-134">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="05c2c-134">-Vault</span></span>
<span data-ttu-id="05c2c-135">Az SSL-tanúsítványt tartalmazó fő pince</span><span class="sxs-lookup"><span data-stu-id="05c2c-135">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="05c2c-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="05c2c-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="05c2c-137">A webalkalmazás tűzfal-házirendjének minden állomáshoz tartozó erőforrás-azonosítója (ha szükséges)</span><span class="sxs-lookup"><span data-stu-id="05c2c-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="05c2c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c2c-138">CommonParameters</span></span>
<span data-ttu-id="05c2c-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05c2c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c2c-140">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="05c2c-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c2c-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05c2c-141">INPUTS</span></span>

### <span data-ttu-id="05c2c-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="05c2c-142">None</span></span>

## <span data-ttu-id="05c2c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05c2c-143">OUTPUTS</span></span>

### <span data-ttu-id="05c2c-144">Microsoft. Azure. Command. FrontDoor. models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="05c2c-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="05c2c-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05c2c-145">NOTES</span></span>

## <span data-ttu-id="05c2c-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05c2c-146">RELATED LINKS</span></span>

<span data-ttu-id="05c2c-147">[Új – AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="05c2c-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
