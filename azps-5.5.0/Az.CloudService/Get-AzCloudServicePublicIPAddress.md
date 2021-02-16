---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServicePublicIPAddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
ms.openlocfilehash: 2a3b643a9ad9d9c588589003e5edb24ceddc4ae1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149035"
---
# <span data-ttu-id="28ca5-101">Get-AzCloudServicePublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="28ca5-101">Get-AzCloudServicePublicIPAddress</span></span>

## <span data-ttu-id="28ca5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="28ca5-103">Szerezze be egy felhőszolgáltatás nyilvános IP-címét.</span><span class="sxs-lookup"><span data-stu-id="28ca5-103">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="28ca5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="28ca5-104">SYNTAX</span></span>

### <span data-ttu-id="28ca5-105">CloudServiceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28ca5-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [<CommonParameters>]
```

### <span data-ttu-id="28ca5-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="28ca5-106">CloudService</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudService <CloudService> [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="28ca5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="28ca5-107">DESCRIPTION</span></span>
<span data-ttu-id="28ca5-108">Szerezze be egy felhőszolgáltatás nyilvános IP-címét.</span><span class="sxs-lookup"><span data-stu-id="28ca5-108">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="28ca5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="28ca5-109">EXAMPLES</span></span>

### <span data-ttu-id="28ca5-110">1. példa: Példányszintű nyilvános IP-címek lekérte egy adott felhőbeli szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="28ca5-110">Example 1: Get instance level public IP addresses for a given cloud service name.</span></span>
```powershell
PS C:\> Get-AzCloudServicePublicIPAddress -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="28ca5-111">Egy adott felhőszolgáltatás nevének példányszintű nyilvános IP-címét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="28ca5-111">Gets the instance level public IP addresses for a given cloud service name.</span></span>

### <span data-ttu-id="28ca5-112">2. példa: Példányszintű nyilvános IP-címek lekérte egy adott felhőszolgáltatás-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="28ca5-112">Example 2: Get instance level public IP addresses for a given cloud service object.</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServicePublicIPAddress -CloudService $cs

```

<span data-ttu-id="28ca5-113">Egy adott felhőszolgáltatás-objektum példányszintű nyilvános IP-címeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="28ca5-113">Gets the instance level public IP addresses for a given cloud service object.</span></span>

## <span data-ttu-id="28ca5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28ca5-114">PARAMETERS</span></span>

### <span data-ttu-id="28ca5-115">-CloudService</span><span class="sxs-lookup"><span data-stu-id="28ca5-115">-CloudService</span></span>
<span data-ttu-id="28ca5-116">CloudService-példány.</span><span class="sxs-lookup"><span data-stu-id="28ca5-116">CloudService instance.</span></span>
<span data-ttu-id="28ca5-117">A felhőszolgáltatás tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK című szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="28ca5-117">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ca5-118">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="28ca5-118">-CloudServiceName</span></span>
<span data-ttu-id="28ca5-119">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="28ca5-119">CloudServiceName.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ca5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28ca5-120">-ResourceGroupName</span></span>
<span data-ttu-id="28ca5-121">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="28ca5-121">ResourceGroupName.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ca5-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28ca5-122">-SubscriptionId</span></span>
<span data-ttu-id="28ca5-123">Előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28ca5-123">Subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ca5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ca5-124">CommonParameters</span></span>
<span data-ttu-id="28ca5-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28ca5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ca5-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28ca5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ca5-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28ca5-127">INPUTS</span></span>

## <span data-ttu-id="28ca5-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28ca5-128">OUTPUTS</span></span>

## <span data-ttu-id="28ca5-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="28ca5-129">NOTES</span></span>

<span data-ttu-id="28ca5-130">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="28ca5-130">ALIASES</span></span>

<span data-ttu-id="28ca5-131">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="28ca5-131">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="28ca5-132">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="28ca5-132">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="28ca5-133">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="28ca5-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="28ca5-134"><CloudService>CLOUDSERVICE: CloudService instance.</span><span class="sxs-lookup"><span data-stu-id="28ca5-134">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="28ca5-135">`Location <String>`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="28ca5-135">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="28ca5-136">`[Configuration <String>]`: A felhőszolgáltatás XML-szolgáltatáskonfigurációját (.cscfg) adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ca5-136">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="28ca5-137">`[ConfigurationUrl <String>]`: Egy URL-címet ad meg, amely a blobszolgáltatás szolgáltatás-konfigurációjának helyére hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="28ca5-137">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="28ca5-138">A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet SAS-URI.</span><span class="sxs-lookup"><span data-stu-id="28ca5-138">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="28ca5-139">Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="28ca5-139">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="28ca5-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Egy felhőbeli szolgáltatásbővítmény-profilt ismertet.</span><span class="sxs-lookup"><span data-stu-id="28ca5-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="28ca5-141">`[Extension <IExtension[]>]`: A felhőszolgáltatás bővítményei.</span><span class="sxs-lookup"><span data-stu-id="28ca5-141">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="28ca5-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicit módon megadhatja, hogy a platform képes-e automatikusan frissíteni a TypeHandlerVersiont a nagyobb alverziókra, amikor elérhetővé válnak.</span><span class="sxs-lookup"><span data-stu-id="28ca5-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="28ca5-143">`[ForceUpdateTag <String>]`: Címkével kényszerítheti a megadott nyilvános és védett beállítások alkalmazását.</span><span class="sxs-lookup"><span data-stu-id="28ca5-143">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="28ca5-144">A címkeérték módosítása lehetővé teszi a bővítmény újrafuttatését a nyilvános vagy védett beállítások módosítása nélkül.</span><span class="sxs-lookup"><span data-stu-id="28ca5-144">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="28ca5-145">Ha a forceUpdateTag nem változik, a nyilvános vagy védett beállítások frissítéseit a kezelő továbbra is alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="28ca5-145">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="28ca5-146">Ha sem a forceUpdateTag, sem a nyilvános vagy védett beállítások egyike sem változik, a bővítmény a szerepkörpéldányba áramolna ugyanazokkal a sorszámmal, és a kezelő implementációja függ attól, hogy újra futtatja-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="28ca5-146">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="28ca5-147">`[Name <String>]`: A bővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="28ca5-147">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="28ca5-148">`[ProtectedSetting <String>]`: A bővítmény védett beállításai, amelyek titkosítottak, mielőtt elkülde volna a szerepkörpéldánynak.</span><span class="sxs-lookup"><span data-stu-id="28ca5-148">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="28ca5-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="28ca5-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="28ca5-150">`[Publisher <String>]`: A bővítménykezelő közzétevője neve.</span><span class="sxs-lookup"><span data-stu-id="28ca5-150">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="28ca5-151">`[RolesAppliedTo <String[]>]`: A bővítmény alkalmazásához választható szerepkörök listája.</span><span class="sxs-lookup"><span data-stu-id="28ca5-151">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="28ca5-152">Ha a tulajdonság nincs megadva, vagy a "\*" érték meg van adva, a bővítmény a felhőszolgáltatás összes szerepkörében érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="28ca5-152">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="28ca5-153">`[Setting <String>]`: A bővítmény nyilvános beállításai.</span><span class="sxs-lookup"><span data-stu-id="28ca5-153">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="28ca5-154">JSON-bővítményekben ez a bővítmény JSON-beállításai.</span><span class="sxs-lookup"><span data-stu-id="28ca5-154">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="28ca5-155">XML-bővítmény (például RDP) esetén ez a bővítmény XML-beállítása.</span><span class="sxs-lookup"><span data-stu-id="28ca5-155">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="28ca5-156">`[SourceVaultId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="28ca5-156">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="28ca5-157">`[Type <String>]`: A bővítmény típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="28ca5-157">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="28ca5-158">`[TypeHandlerVersion <String>]`: A bővítmény verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ca5-158">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="28ca5-159">A bővítmény verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="28ca5-159">Specifies the version of the extension.</span></span> <span data-ttu-id="28ca5-160">Ha ez az elem nincs megadva, vagy csillag (\*) használja értékként, akkor a bővítmény legújabb verzióját használja a program.</span><span class="sxs-lookup"><span data-stu-id="28ca5-160">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="28ca5-161">Ha az értéket egy főverzió számával, a csillagot pedig alverziószámmal (X.) adja meg, akkor a megadott főverzió legújabb alverziója van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="28ca5-161">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="28ca5-162">Ha a főverzió és az alverzió száma meg van adva (X.Y), akkor az adott bővítményverzió van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="28ca5-162">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="28ca5-163">Ha egy verzió meg van adva, a szerepkörpéldányon automatikus frissítés történik.</span><span class="sxs-lookup"><span data-stu-id="28ca5-163">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="28ca5-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: A felhőszolgáltatás hálózati profilja.</span><span class="sxs-lookup"><span data-stu-id="28ca5-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="28ca5-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: A felhőszolgáltatás terheléselosztási konfigurációjának listája.</span><span class="sxs-lookup"><span data-stu-id="28ca5-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="28ca5-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: AZ IP-címek listája</span><span class="sxs-lookup"><span data-stu-id="28ca5-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="28ca5-167">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="28ca5-167">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="28ca5-168">`[PrivateIPAddress <String>]`: A felhőszolgáltatás által hivatkozott privát IP-cím.</span><span class="sxs-lookup"><span data-stu-id="28ca5-168">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="28ca5-169">`[PublicIPAddressId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="28ca5-169">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="28ca5-170">`[SubnetId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="28ca5-170">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="28ca5-171">`[Name <String>]`: Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="28ca5-171">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="28ca5-172">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="28ca5-172">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="28ca5-173">`[Id <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="28ca5-173">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="28ca5-174">`[OSProfile <ICloudServiceOSProfile>]`: A felhőszolgáltatás operációs rendszerprofilját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="28ca5-174">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="28ca5-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Megadja a szerepkörpéldányokra telepíthető tanúsítványok készletét.</span><span class="sxs-lookup"><span data-stu-id="28ca5-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="28ca5-176">`[SourceVaultId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="28ca5-176">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="28ca5-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: A SourceVault kulcstár-hivatkozásai, amelyek tanúsítványokat tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="28ca5-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="28ca5-178">`[CertificateUrl <String>]`: Ez annak a tanúsítványnak az URL-címe, amely titkosként lett feltöltve a kulcstárolóba.</span><span class="sxs-lookup"><span data-stu-id="28ca5-178">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="28ca5-179">`[PackageUrl <String>]`: Egy URL-címet ad meg, amely a szolgáltatáscsomag blobszolgáltatásban való helyére hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="28ca5-179">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="28ca5-180">A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet SAS-URI.</span><span class="sxs-lookup"><span data-stu-id="28ca5-180">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="28ca5-181">Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="28ca5-181">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="28ca5-182">`[RoleProfile <ICloudServiceRoleProfile>]`: A felhőszolgáltatás szerepkörprofilját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="28ca5-182">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="28ca5-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: A felhőszolgáltatás szerepkörei.</span><span class="sxs-lookup"><span data-stu-id="28ca5-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="28ca5-184">`[Name <String>]`: Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="28ca5-184">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="28ca5-185">`[SkuCapacity <Int64?>]`: A felhőszolgáltatás szerepkör-példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ca5-185">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="28ca5-186">`[SkuName <String>]`: A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="28ca5-186">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="28ca5-187">MEGJEGYZÉS: Ha az új termékváltozat nem támogatott a felhőszolgáltatás által jelenleg használt hardveren, törölnie és újra létre kell hoznia a felhőszolgáltatást, vagy vissza kell lépnie a régi termékváltozatra.</span><span class="sxs-lookup"><span data-stu-id="28ca5-187">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="28ca5-188">`[SkuTier <String>]`: A felhőszolgáltatás rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ca5-188">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="28ca5-189">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="28ca5-189">Possible Values are</span></span> <br /><br /> <span data-ttu-id="28ca5-190">**Normál**</span><span class="sxs-lookup"><span data-stu-id="28ca5-190">**Standard**</span></span> <br /><br /> <span data-ttu-id="28ca5-191">**Alapszintű**</span><span class="sxs-lookup"><span data-stu-id="28ca5-191">**Basic**</span></span>
  - <span data-ttu-id="28ca5-192">`[StartCloudService <Boolean?>]`: (Nem kötelező) Azt jelzi, hogy a felhőszolgáltatást közvetlenül a létrehozása után indítja-e el.</span><span class="sxs-lookup"><span data-stu-id="28ca5-192">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="28ca5-193">Az alapértelmezett érték `true` a .</span><span class="sxs-lookup"><span data-stu-id="28ca5-193">The default value is `true`.</span></span>         <span data-ttu-id="28ca5-194">Ha hamis, a szolgáltatásmodell továbbra is telepítve van, de a kód nem fut azonnal.</span><span class="sxs-lookup"><span data-stu-id="28ca5-194">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="28ca5-195">Ehelyett a szolgáltatás PoweredOff lesz, amíg fel nem hívja a Start menüt, és a szolgáltatás elindul.</span><span class="sxs-lookup"><span data-stu-id="28ca5-195">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="28ca5-196">A telepített szolgáltatások még akkor is költségeket is fizetninek, ha a szolgáltatás nem működik.</span><span class="sxs-lookup"><span data-stu-id="28ca5-196">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="28ca5-197">`[Tag <ICloudServiceTags>]`: Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="28ca5-197">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="28ca5-198">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="28ca5-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="28ca5-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: A felhőszolgáltatás frissítési módja.</span><span class="sxs-lookup"><span data-stu-id="28ca5-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="28ca5-200">A szerepkörpéldányok ki vannak osztva a tartományok frissítéséhez a szolgáltatás telepítésekor.</span><span class="sxs-lookup"><span data-stu-id="28ca5-200">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="28ca5-201">A frissítéseket manuálisan kezdeményezheti az egyes frissítési tartományokban, illetve automatikusan az összes frissítési tartományban.</span><span class="sxs-lookup"><span data-stu-id="28ca5-201">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="28ca5-202">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="28ca5-202">Possible Values are</span></span> <br /><br /><span data-ttu-id="28ca5-203">**Automatikus**</span><span class="sxs-lookup"><span data-stu-id="28ca5-203">**Auto**</span></span><br /><br /><span data-ttu-id="28ca5-204">**Kézi**</span><span class="sxs-lookup"><span data-stu-id="28ca5-204">**Manual**</span></span> <br /><br /><span data-ttu-id="28ca5-205">**Egyidejű**</span><span class="sxs-lookup"><span data-stu-id="28ca5-205">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="28ca5-206">Ha nincs megadva, az alapértelmezett érték az Automatikus. Ha a Kézi beállítás van beállítva, akkor a PUT UpdateDomain tartományt meg kell hívva alkalmazni a frissítést.</span><span class="sxs-lookup"><span data-stu-id="28ca5-206">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="28ca5-207">Ha az Automatikus beállítás van beállítva, a rendszer automatikusan alkalmazza a frissítést az egyes frissítési tartományokra.</span><span class="sxs-lookup"><span data-stu-id="28ca5-207">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="28ca5-208">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28ca5-208">RELATED LINKS</span></span>

