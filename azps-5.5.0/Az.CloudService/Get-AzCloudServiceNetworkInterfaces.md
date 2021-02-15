---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServiceNetworkInterfaces
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
ms.openlocfilehash: 7f8a51c518bd034e51d8c25d5029bb57b3e38caf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164219"
---
# <span data-ttu-id="40e29-101">Get-AzCloudServiceNetworkInterfaces</span><span class="sxs-lookup"><span data-stu-id="40e29-101">Get-AzCloudServiceNetworkInterfaces</span></span>

## <span data-ttu-id="40e29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40e29-102">SYNOPSIS</span></span>
<span data-ttu-id="40e29-103">Szerezze be egy felhőszolgáltatás hálózati felületét.</span><span class="sxs-lookup"><span data-stu-id="40e29-103">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="40e29-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="40e29-104">SYNTAX</span></span>

### <span data-ttu-id="40e29-105">CloudServiceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40e29-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-RoleInstanceName <String>] [<CommonParameters>]
```

### <span data-ttu-id="40e29-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="40e29-106">CloudService</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudService <CloudService> [-SubscriptionId <String>]
 [-RoleInstanceName <String>] [<CommonParameters>]
```

## <span data-ttu-id="40e29-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="40e29-107">DESCRIPTION</span></span>
<span data-ttu-id="40e29-108">Szerezze be egy felhőszolgáltatás hálózati felületét.</span><span class="sxs-lookup"><span data-stu-id="40e29-108">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="40e29-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="40e29-109">EXAMPLES</span></span>

### <span data-ttu-id="40e29-110">1. példa: Hálózati felületek lekérte a felhőszolgáltatás nevét</span><span class="sxs-lookup"><span data-stu-id="40e29-110">Example 1: Get network interfaces by a cloud service name</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="40e29-111">Egy adott felhőbeli szolgáltatásnév összes hálózati felületét beveszi.</span><span class="sxs-lookup"><span data-stu-id="40e29-111">Gets all the network interfaces for a given cloud service name.</span></span>

### <span data-ttu-id="40e29-112">2. példa: Hálózati felületek lekérte a felhőszolgáltatás-objektumokat</span><span class="sxs-lookup"><span data-stu-id="40e29-112">Example 2: Get network interfaces by a cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs

```

<span data-ttu-id="40e29-113">Egy adott felhőszolgáltatás-objektum összes hálózati felületét beveszi.</span><span class="sxs-lookup"><span data-stu-id="40e29-113">Gets all the network interfaces for a given cloud service object.</span></span>

### <span data-ttu-id="40e29-114">3. példa: Hálózati felületek lekérte egy felhőalapú szolgáltatásobjektum és szerepkörpéldány neve alapján.</span><span class="sxs-lookup"><span data-stu-id="40e29-114">Example 3: Get network interfaces by a cloud service object and role instance name.</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs -RoleInstanceName WebRole1_IN_0

```

<span data-ttu-id="40e29-115">Egy adott felhőszolgáltatás-objektum és szerepkörpéldány nevének összes hálózati felületét beszeri.</span><span class="sxs-lookup"><span data-stu-id="40e29-115">Gets all the network interfaces for a given cloud service object and role instance name.</span></span>

## <span data-ttu-id="40e29-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40e29-116">PARAMETERS</span></span>

### <span data-ttu-id="40e29-117">-CloudService</span><span class="sxs-lookup"><span data-stu-id="40e29-117">-CloudService</span></span>
<span data-ttu-id="40e29-118">CloudService-példány.</span><span class="sxs-lookup"><span data-stu-id="40e29-118">CloudService instance.</span></span>
<span data-ttu-id="40e29-119">A felhőszolgáltatás tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK című szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="40e29-119">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="40e29-120">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="40e29-120">-CloudServiceName</span></span>
<span data-ttu-id="40e29-121">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="40e29-121">CloudServiceName.</span></span>

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

### <span data-ttu-id="40e29-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e29-122">-ResourceGroupName</span></span>
<span data-ttu-id="40e29-123">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="40e29-123">ResourceGroupName.</span></span>

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

### <span data-ttu-id="40e29-124">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="40e29-124">-RoleInstanceName</span></span>
<span data-ttu-id="40e29-125">RoleInstanceName.</span><span class="sxs-lookup"><span data-stu-id="40e29-125">RoleInstanceName.</span></span>

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

### <span data-ttu-id="40e29-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40e29-126">-SubscriptionId</span></span>
<span data-ttu-id="40e29-127">Előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40e29-127">Subscription.</span></span>

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

### <span data-ttu-id="40e29-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e29-128">CommonParameters</span></span>
<span data-ttu-id="40e29-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e29-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e29-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40e29-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e29-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40e29-131">INPUTS</span></span>

## <span data-ttu-id="40e29-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40e29-132">OUTPUTS</span></span>

## <span data-ttu-id="40e29-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="40e29-133">NOTES</span></span>

<span data-ttu-id="40e29-134">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="40e29-134">ALIASES</span></span>

<span data-ttu-id="40e29-135">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="40e29-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40e29-136">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="40e29-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40e29-137">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="40e29-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40e29-138"><CloudService>CLOUDSERVICE: CloudService példány.</span><span class="sxs-lookup"><span data-stu-id="40e29-138">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="40e29-139">`Location <String>`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="40e29-139">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="40e29-140">`[Configuration <String>]`: A felhőszolgáltatás XML-szolgáltatáskonfigurációját (.cscfg) adja meg.</span><span class="sxs-lookup"><span data-stu-id="40e29-140">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="40e29-141">`[ConfigurationUrl <String>]`: Egy URL-címet ad meg, amely a blobszolgáltatás szolgáltatás-konfigurációjának helyére hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="40e29-141">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="40e29-142">A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet SAS-URI.</span><span class="sxs-lookup"><span data-stu-id="40e29-142">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="40e29-143">Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="40e29-143">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="40e29-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Egy felhőbeli szolgáltatásbővítmény-profilt ismertet.</span><span class="sxs-lookup"><span data-stu-id="40e29-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="40e29-145">`[Extension <IExtension[]>]`: A felhőszolgáltatás bővítményei.</span><span class="sxs-lookup"><span data-stu-id="40e29-145">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="40e29-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicit módon megadhatja, hogy a platform képes-e automatikusan frissíteni a TypeHandlerVersiont a nagyobb alverziókra, amikor elérhetővé válnak.</span><span class="sxs-lookup"><span data-stu-id="40e29-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="40e29-147">`[ForceUpdateTag <String>]`: Címkével kényszerítheti a megadott nyilvános és védett beállítások alkalmazását.</span><span class="sxs-lookup"><span data-stu-id="40e29-147">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="40e29-148">A címkeérték módosítása lehetővé teszi a bővítmény újrafuttatését a nyilvános vagy védett beállítások módosítása nélkül.</span><span class="sxs-lookup"><span data-stu-id="40e29-148">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="40e29-149">Ha a forceUpdateTag nem változik, a nyilvános vagy védett beállítások frissítéseit a kezelő továbbra is alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="40e29-149">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="40e29-150">Ha sem a forceUpdateTag, sem a nyilvános vagy védett beállítások egyike sem változik, a bővítmény a szerepkörpéldányba áramolna ugyanazokkal a sorszámmal, és a kezelő implementációja függ attól, hogy újra futtatja-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="40e29-150">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="40e29-151">`[Name <String>]`: A bővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="40e29-151">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="40e29-152">`[ProtectedSetting <String>]`: A bővítmény védett beállításai, amelyek titkosítottak, mielőtt elkülde volna a szerepkörpéldánynak.</span><span class="sxs-lookup"><span data-stu-id="40e29-152">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="40e29-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="40e29-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="40e29-154">`[Publisher <String>]`: A bővítménykezelő közzétevője neve.</span><span class="sxs-lookup"><span data-stu-id="40e29-154">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="40e29-155">`[RolesAppliedTo <String[]>]`: A bővítmény alkalmazásához választható szerepkörök listája.</span><span class="sxs-lookup"><span data-stu-id="40e29-155">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="40e29-156">Ha a tulajdonság nincs megadva, vagy a "\*" érték meg van adva, a bővítmény a felhőszolgáltatás összes szerepkörében érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="40e29-156">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="40e29-157">`[Setting <String>]`: A bővítmény nyilvános beállításai.</span><span class="sxs-lookup"><span data-stu-id="40e29-157">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="40e29-158">JSON-bővítményekben ez a bővítmény JSON-beállításai.</span><span class="sxs-lookup"><span data-stu-id="40e29-158">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="40e29-159">XML-bővítmény (például RDP) esetén ez a bővítmény XML-beállítása.</span><span class="sxs-lookup"><span data-stu-id="40e29-159">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="40e29-160">`[SourceVaultId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="40e29-160">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="40e29-161">`[Type <String>]`: A bővítmény típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="40e29-161">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="40e29-162">`[TypeHandlerVersion <String>]`: A bővítmény verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="40e29-162">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="40e29-163">A bővítmény verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="40e29-163">Specifies the version of the extension.</span></span> <span data-ttu-id="40e29-164">Ha ez az elem nincs megadva, vagy csillag (\*) használja értékként, akkor a bővítmény legújabb verzióját használja a program.</span><span class="sxs-lookup"><span data-stu-id="40e29-164">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="40e29-165">Ha az értéket egy főverzió számával, a csillagot pedig alverziószámmal (X.) adja meg, akkor a megadott főverzió legújabb alverziója van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="40e29-165">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="40e29-166">Ha főverziószámot és alverziószámot ad meg (X.Y), az adott bővítményverzió van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="40e29-166">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="40e29-167">Ha egy verzió meg van adva, a szerepkörpéldányon automatikus frissítés történik.</span><span class="sxs-lookup"><span data-stu-id="40e29-167">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="40e29-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: A felhőszolgáltatás hálózati profilja.</span><span class="sxs-lookup"><span data-stu-id="40e29-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="40e29-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: A felhőszolgáltatás terheléselosztási konfigurációjának listája.</span><span class="sxs-lookup"><span data-stu-id="40e29-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="40e29-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: AZ IP-címek listája</span><span class="sxs-lookup"><span data-stu-id="40e29-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="40e29-171">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="40e29-171">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="40e29-172">`[PrivateIPAddress <String>]`: A felhőszolgáltatás által hivatkozott privát IP-cím.</span><span class="sxs-lookup"><span data-stu-id="40e29-172">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="40e29-173">`[PublicIPAddressId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="40e29-173">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="40e29-174">`[SubnetId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="40e29-174">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="40e29-175">`[Name <String>]`: Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="40e29-175">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="40e29-176">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="40e29-176">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="40e29-177">`[Id <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="40e29-177">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="40e29-178">`[OSProfile <ICloudServiceOSProfile>]`: A felhőszolgáltatás operációs rendszerprofilját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="40e29-178">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="40e29-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: A szerepkörpéldányokra telepíthető tanúsítványok halmazát adja meg.</span><span class="sxs-lookup"><span data-stu-id="40e29-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="40e29-180">`[SourceVaultId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="40e29-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="40e29-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: A SourceVault kulcstár-hivatkozásai, amelyek tanúsítványokat tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="40e29-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="40e29-182">`[CertificateUrl <String>]`: Ez annak a tanúsítványnak az URL-címe, amely titkosként lett feltöltve a kulcstárolóba.</span><span class="sxs-lookup"><span data-stu-id="40e29-182">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="40e29-183">`[PackageUrl <String>]`: Egy URL-címet ad meg, amely a szolgáltatáscsomag blobszolgáltatásban való helyére hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="40e29-183">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="40e29-184">A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet sas-uri.</span><span class="sxs-lookup"><span data-stu-id="40e29-184">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="40e29-185">Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="40e29-185">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="40e29-186">`[RoleProfile <ICloudServiceRoleProfile>]`: A felhőszolgáltatás szerepkörprofilját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="40e29-186">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="40e29-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: A felhőszolgáltatás szerepkörei.</span><span class="sxs-lookup"><span data-stu-id="40e29-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="40e29-188">`[Name <String>]`: Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="40e29-188">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="40e29-189">`[SkuCapacity <Int64?>]`: A felhőszolgáltatás szerepkörpéldányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="40e29-189">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="40e29-190">`[SkuName <String>]`: A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="40e29-190">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="40e29-191">MEGJEGYZÉS: Ha az új termékváltozat nem támogatott a felhőszolgáltatás által jelenleg használt hardveren, törölnie és újra létre kell hoznia a felhőszolgáltatást, vagy vissza kell lépnie a régi termékváltozatra.</span><span class="sxs-lookup"><span data-stu-id="40e29-191">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="40e29-192">`[SkuTier <String>]`: A felhőszolgáltatás rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40e29-192">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="40e29-193">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="40e29-193">Possible Values are</span></span> <br /><br /> <span data-ttu-id="40e29-194">**Normál**</span><span class="sxs-lookup"><span data-stu-id="40e29-194">**Standard**</span></span> <br /><br /> <span data-ttu-id="40e29-195">**Alapszintű**</span><span class="sxs-lookup"><span data-stu-id="40e29-195">**Basic**</span></span>
  - <span data-ttu-id="40e29-196">`[StartCloudService <Boolean?>]`: (Nem kötelező) Azt jelzi, hogy a felhőszolgáltatást a létrehozása után azonnal el kell-e kezdeni.</span><span class="sxs-lookup"><span data-stu-id="40e29-196">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="40e29-197">Az alapértelmezett érték `true` a .</span><span class="sxs-lookup"><span data-stu-id="40e29-197">The default value is `true`.</span></span>         <span data-ttu-id="40e29-198">Ha hamis, a szolgáltatásmodell továbbra is telepítve van, de a kód nem fut azonnal.</span><span class="sxs-lookup"><span data-stu-id="40e29-198">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="40e29-199">Ehelyett a szolgáltatás PoweredOff lesz, amíg fel nem hívja a Start menüt, és a szolgáltatás elindul.</span><span class="sxs-lookup"><span data-stu-id="40e29-199">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="40e29-200">Az üzembe helyezett szolgáltatások akkor is költségeket fizetninek, ha a szolgáltatás nem működik.</span><span class="sxs-lookup"><span data-stu-id="40e29-200">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="40e29-201">`[Tag <ICloudServiceTags>]`: Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="40e29-201">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="40e29-202">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="40e29-202">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="40e29-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: A felhőszolgáltatás frissítési módja.</span><span class="sxs-lookup"><span data-stu-id="40e29-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="40e29-204">A szerepkörpéldányok ki vannak osztva a tartományok frissítéséhez a szolgáltatás telepítésekor.</span><span class="sxs-lookup"><span data-stu-id="40e29-204">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="40e29-205">A frissítéseket manuálisan kezdeményezheti az egyes frissítési tartományokban, illetve automatikusan az összes frissítési tartományban.</span><span class="sxs-lookup"><span data-stu-id="40e29-205">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="40e29-206">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="40e29-206">Possible Values are</span></span> <br /><br /><span data-ttu-id="40e29-207">**Automatikus**</span><span class="sxs-lookup"><span data-stu-id="40e29-207">**Auto**</span></span><br /><br /><span data-ttu-id="40e29-208">**Kézi**</span><span class="sxs-lookup"><span data-stu-id="40e29-208">**Manual**</span></span> <br /><br /><span data-ttu-id="40e29-209">**Egyidejű**</span><span class="sxs-lookup"><span data-stu-id="40e29-209">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="40e29-210">Ha nincs megadva, az alapértelmezett érték az Automatikus. Ha a Kézi beállítás van beállítva, akkor a PUT UpdateDomain tartományt meg kell hívva alkalmazni a frissítést.</span><span class="sxs-lookup"><span data-stu-id="40e29-210">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="40e29-211">Ha az Automatikus beállítás van beállítva, a rendszer automatikusan alkalmazza a frissítést az egyes frissítési tartományokra.</span><span class="sxs-lookup"><span data-stu-id="40e29-211">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="40e29-212">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40e29-212">RELATED LINKS</span></span>

