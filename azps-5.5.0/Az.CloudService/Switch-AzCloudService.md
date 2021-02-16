---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: f10d11dbbe98c098286a072d5882bf5d3a464d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162346"
---
# <span data-ttu-id="50cff-101">Switch-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="50cff-101">Switch-AzCloudService</span></span>

## <span data-ttu-id="50cff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50cff-102">SYNOPSIS</span></span>
<span data-ttu-id="50cff-103">Az IP-pontokat felcseréli két felhőszolgáltatás (kiterjesztett támogatás) terhelésegyenleg-elosztása között.</span><span class="sxs-lookup"><span data-stu-id="50cff-103">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="50cff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="50cff-104">SYNTAX</span></span>

### <span data-ttu-id="50cff-105">CloudServiceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="50cff-105">CloudServiceName (Default)</span></span>
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="50cff-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="50cff-106">CloudService</span></span>
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="50cff-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="50cff-107">DESCRIPTION</span></span>
<span data-ttu-id="50cff-108">Az IP-pontokat felcseréli két felhőszolgáltatás (kiterjesztett támogatás) terhelésegyenleg-elosztása között.</span><span class="sxs-lookup"><span data-stu-id="50cff-108">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="50cff-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="50cff-109">EXAMPLES</span></span>

### <span data-ttu-id="50cff-110">1. példa: Felhőszolgáltatás váltása név használatával</span><span class="sxs-lookup"><span data-stu-id="50cff-110">Example 1: Switch cloud service using name</span></span>
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="50cff-111">A fenti parancs meghívja a "BService" nevű, a felhőbeli szolgáltatáson a helyi műveletet, és végrehajtja a műveletet, amint a felhasználó megerősíti a műveletet a megerősítést kérő üzenetben.</span><span class="sxs-lookup"><span data-stu-id="50cff-111">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="50cff-112">A "BService" felcserélhető a felcserélhető felhőszolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="50cff-112">'BService' with be swapped with its swappable cloud service.</span></span>

### <span data-ttu-id="50cff-113">2. példa: Felhőszolgáltatás váltása felhőalapú szolgáltatásobjektum használatával</span><span class="sxs-lookup"><span data-stu-id="50cff-113">Example 2: Switch cloud service using cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

<span data-ttu-id="50cff-114">A fenti parancs meghívja a "BService" nevű, a felhőbeli szolgáltatáson a helyi műveletet, és végrehajtja a műveletet, amint a felhasználó megerősíti a műveletet a megerősítést kérő üzenetben.</span><span class="sxs-lookup"><span data-stu-id="50cff-114">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="50cff-115">A "BService" felcserélhető a felcserélhető felhőszolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="50cff-115">'BService' with be swapped with its swappable cloud service.</span></span>

## <span data-ttu-id="50cff-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50cff-116">PARAMETERS</span></span>

### <span data-ttu-id="50cff-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50cff-117">-AsJob</span></span>
<span data-ttu-id="50cff-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="50cff-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50cff-119">-Async</span><span class="sxs-lookup"><span data-stu-id="50cff-119">-Async</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50cff-120">-CloudService</span><span class="sxs-lookup"><span data-stu-id="50cff-120">-CloudService</span></span>
<span data-ttu-id="50cff-121">A felhőszolgáltatás tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="50cff-121">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="50cff-122">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="50cff-122">-CloudServiceName</span></span>


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

### <span data-ttu-id="50cff-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50cff-123">-DefaultProfile</span></span>
<span data-ttu-id="50cff-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50cff-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50cff-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50cff-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="50cff-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50cff-126">-SubscriptionId</span></span>
<span data-ttu-id="50cff-127">Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="50cff-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="50cff-128">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="50cff-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="50cff-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50cff-129">-Confirm</span></span>
<span data-ttu-id="50cff-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="50cff-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50cff-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50cff-131">-WhatIf</span></span>
<span data-ttu-id="50cff-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="50cff-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50cff-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50cff-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50cff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50cff-134">CommonParameters</span></span>
<span data-ttu-id="50cff-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50cff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50cff-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50cff-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50cff-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50cff-137">INPUTS</span></span>

## <span data-ttu-id="50cff-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50cff-138">OUTPUTS</span></span>

### <span data-ttu-id="50cff-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="50cff-139">System.Boolean</span></span>

## <span data-ttu-id="50cff-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="50cff-140">NOTES</span></span>

<span data-ttu-id="50cff-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="50cff-141">ALIASES</span></span>

<span data-ttu-id="50cff-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="50cff-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="50cff-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="50cff-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="50cff-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="50cff-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="50cff-145"><CloudService>CLOUDSERVICE:</span><span class="sxs-lookup"><span data-stu-id="50cff-145">CLOUDSERVICE <CloudService>:</span></span> 
  - <span data-ttu-id="50cff-146">`Location <String>`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="50cff-146">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="50cff-147">`[Configuration <String>]`: A felhőszolgáltatás XML-szolgáltatáskonfigurációját (.cscfg) adja meg.</span><span class="sxs-lookup"><span data-stu-id="50cff-147">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="50cff-148">`[ConfigurationUrl <String>]`: Olyan URL-címet ad meg, amely a blobszolgáltatás szolgáltatás-konfigurációjának helyére hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="50cff-148">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="50cff-149">A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet SAS-URI.</span><span class="sxs-lookup"><span data-stu-id="50cff-149">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="50cff-150">Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="50cff-150">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="50cff-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Egy felhőbeli szolgáltatásbővítmény-profilt ismertet.</span><span class="sxs-lookup"><span data-stu-id="50cff-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="50cff-152">`[Extension <IExtension[]>]`: A felhőszolgáltatás bővítményei.</span><span class="sxs-lookup"><span data-stu-id="50cff-152">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="50cff-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicit módon megadhatja, hogy a platform képes-e automatikusan frissíteni a TypeHandlerVersiont a nagyobb alverziókra, amikor elérhetővé válnak.</span><span class="sxs-lookup"><span data-stu-id="50cff-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="50cff-154">`[ForceUpdateTag <String>]`: Címkével kényszerítheti a megadott nyilvános és védett beállítások alkalmazását.</span><span class="sxs-lookup"><span data-stu-id="50cff-154">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="50cff-155">A címkeérték módosítása lehetővé teszi a bővítmény újrafuttatését a nyilvános vagy védett beállítások módosítása nélkül.</span><span class="sxs-lookup"><span data-stu-id="50cff-155">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="50cff-156">Ha a forceUpdateTag nem változik, a nyilvános vagy védett beállítások frissítéseit a kezelő továbbra is alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="50cff-156">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="50cff-157">Ha sem a forceUpdateTag, sem a nyilvános vagy védett beállítások egyike sem változik, a bővítmény a szerepkörpéldányba áramolna ugyanazokkal a sorszámmal, és a kezelő implementációja függ attól, hogy újra futtatja-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="50cff-157">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="50cff-158">`[Name <String>]`: A bővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="50cff-158">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="50cff-159">`[ProtectedSetting <String>]`: A bővítmény védett beállításai, amelyek titkosítottak, mielőtt elkülde volna a szerepkörpéldánynak.</span><span class="sxs-lookup"><span data-stu-id="50cff-159">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="50cff-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="50cff-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="50cff-161">`[Publisher <String>]`: A bővítménykezelő közzétevője neve.</span><span class="sxs-lookup"><span data-stu-id="50cff-161">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="50cff-162">`[RolesAppliedTo <String[]>]`: A bővítmény alkalmazásához választható szerepkörök listája.</span><span class="sxs-lookup"><span data-stu-id="50cff-162">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="50cff-163">Ha a tulajdonság nincs megadva, vagy a "\*" érték meg van adva, a bővítmény a felhőszolgáltatás összes szerepkörében érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="50cff-163">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="50cff-164">`[Setting <String>]`: A bővítmény nyilvános beállításai.</span><span class="sxs-lookup"><span data-stu-id="50cff-164">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="50cff-165">JSON-bővítményekben ez a bővítmény JSON-beállításai.</span><span class="sxs-lookup"><span data-stu-id="50cff-165">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="50cff-166">XML-bővítmény (például RDP) esetén ez a bővítmény XML-beállítása.</span><span class="sxs-lookup"><span data-stu-id="50cff-166">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="50cff-167">`[SourceVaultId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="50cff-167">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="50cff-168">`[Type <String>]`: A bővítmény típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="50cff-168">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="50cff-169">`[TypeHandlerVersion <String>]`: A bővítmény verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="50cff-169">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="50cff-170">A bővítmény verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="50cff-170">Specifies the version of the extension.</span></span> <span data-ttu-id="50cff-171">Ha ez az elem nincs megadva, vagy csillag (\*) használja értékként, akkor a bővítmény legújabb verzióját használja a program.</span><span class="sxs-lookup"><span data-stu-id="50cff-171">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="50cff-172">Ha az értéket egy főverzió számával, a csillagot pedig alverziószámmal (X.) adja meg, akkor a megadott főverzió legújabb alverziója van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="50cff-172">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="50cff-173">Ha a főverzió és az alverzió száma meg van adva (X.Y), akkor az adott bővítményverzió van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="50cff-173">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="50cff-174">Ha egy verzió meg van adva, a szerepkörpéldányon automatikus frissítés történik.</span><span class="sxs-lookup"><span data-stu-id="50cff-174">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="50cff-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: A felhőszolgáltatás hálózati profilja.</span><span class="sxs-lookup"><span data-stu-id="50cff-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="50cff-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: A felhőszolgáltatás terheléselosztási konfigurációjának listája.</span><span class="sxs-lookup"><span data-stu-id="50cff-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="50cff-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: AZ IP-címek listája</span><span class="sxs-lookup"><span data-stu-id="50cff-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="50cff-178">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="50cff-178">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="50cff-179">`[PrivateIPAddress <String>]`: A felhőszolgáltatás által hivatkozott privát IP-cím.</span><span class="sxs-lookup"><span data-stu-id="50cff-179">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="50cff-180">`[PublicIPAddressId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="50cff-180">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="50cff-181">`[SubnetId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="50cff-181">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="50cff-182">`[Name <String>]`: Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="50cff-182">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="50cff-183">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="50cff-183">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="50cff-184">`[Id <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="50cff-184">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="50cff-185">`[OSProfile <ICloudServiceOSProfile>]`: A felhőszolgáltatás operációs rendszerprofilját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="50cff-185">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="50cff-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: A szerepkörpéldányokra telepíthető tanúsítványok halmazát adja meg.</span><span class="sxs-lookup"><span data-stu-id="50cff-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="50cff-187">`[SourceVaultId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="50cff-187">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="50cff-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: A SourceVault kulcstár-hivatkozásai, amelyek tanúsítványokat tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="50cff-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="50cff-189">`[CertificateUrl <String>]`: Ez annak a tanúsítványnak az URL-címe, amely titkosként lett feltöltve a kulcstárolóba.</span><span class="sxs-lookup"><span data-stu-id="50cff-189">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="50cff-190">`[PackageUrl <String>]`: Egy URL-címet ad meg, amely a szolgáltatáscsomag helyére hivatkozik a Blob szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="50cff-190">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="50cff-191">A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet sas-uri.</span><span class="sxs-lookup"><span data-stu-id="50cff-191">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="50cff-192">Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="50cff-192">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="50cff-193">`[RoleProfile <ICloudServiceRoleProfile>]`: A felhőszolgáltatás szerepkörprofilját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="50cff-193">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="50cff-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: A felhőszolgáltatás szerepkörei.</span><span class="sxs-lookup"><span data-stu-id="50cff-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="50cff-195">`[Name <String>]`: Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="50cff-195">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="50cff-196">`[SkuCapacity <Int64?>]`: A felhőszolgáltatás szerepkörpéldányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="50cff-196">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="50cff-197">`[SkuName <String>]`: A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="50cff-197">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="50cff-198">MEGJEGYZÉS: Ha az új termékváltozat nem támogatott a felhőszolgáltatás által jelenleg használt hardveren, törölnie és újra létre kell hoznia a felhőszolgáltatást, vagy vissza kell lépnie a régi termékváltozatra.</span><span class="sxs-lookup"><span data-stu-id="50cff-198">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="50cff-199">`[SkuTier <String>]`: A felhőszolgáltatás rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50cff-199">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="50cff-200">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="50cff-200">Possible Values are</span></span> <br /><br /> <span data-ttu-id="50cff-201">**Normál**</span><span class="sxs-lookup"><span data-stu-id="50cff-201">**Standard**</span></span> <br /><br /> <span data-ttu-id="50cff-202">**Alapszintű**</span><span class="sxs-lookup"><span data-stu-id="50cff-202">**Basic**</span></span>
  - <span data-ttu-id="50cff-203">`[StartCloudService <Boolean?>]`: (Nem kötelező) Azt jelzi, hogy a felhőszolgáltatást a létrehozása után azonnal el kell-e kezdeni.</span><span class="sxs-lookup"><span data-stu-id="50cff-203">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="50cff-204">Az alapértelmezett érték `true` a .</span><span class="sxs-lookup"><span data-stu-id="50cff-204">The default value is `true`.</span></span>         <span data-ttu-id="50cff-205">Ha hamis, a szolgáltatásmodell továbbra is telepítve van, de a kód nem fut azonnal.</span><span class="sxs-lookup"><span data-stu-id="50cff-205">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="50cff-206">Ehelyett a szolgáltatás PoweredOff lesz, amíg fel nem hívja a Start menüt, és a szolgáltatás elindul.</span><span class="sxs-lookup"><span data-stu-id="50cff-206">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="50cff-207">Az üzembe helyezett szolgáltatások akkor is költségeket fizetninek, ha a szolgáltatás nem működik.</span><span class="sxs-lookup"><span data-stu-id="50cff-207">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="50cff-208">`[Tag <ICloudServiceTags>]`: Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="50cff-208">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="50cff-209">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="50cff-209">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="50cff-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: A felhőszolgáltatás frissítési módja.</span><span class="sxs-lookup"><span data-stu-id="50cff-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="50cff-211">A szerepkörpéldányok ki vannak osztva a tartományok frissítéséhez a szolgáltatás telepítésekor.</span><span class="sxs-lookup"><span data-stu-id="50cff-211">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="50cff-212">A frissítéseket manuálisan kezdeményezheti az egyes frissítési tartományokban, illetve automatikusan az összes frissítési tartományban.</span><span class="sxs-lookup"><span data-stu-id="50cff-212">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="50cff-213">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="50cff-213">Possible Values are</span></span> <br /><br /><span data-ttu-id="50cff-214">**Automatikus**</span><span class="sxs-lookup"><span data-stu-id="50cff-214">**Auto**</span></span><br /><br /><span data-ttu-id="50cff-215">**Kézi**</span><span class="sxs-lookup"><span data-stu-id="50cff-215">**Manual**</span></span> <br /><br /><span data-ttu-id="50cff-216">**Egyidejű**</span><span class="sxs-lookup"><span data-stu-id="50cff-216">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="50cff-217">Ha nincs megadva, az alapértelmezett érték az Automatikus. Ha a Kézi beállítás van beállítva, akkor a PUT UpdateDomain tartományt meg kell hívva alkalmazni a frissítést.</span><span class="sxs-lookup"><span data-stu-id="50cff-217">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="50cff-218">Ha az Automatikus beállítás van beállítva, a rendszer automatikusan alkalmazza a frissítést az egyes frissítési tartományokra.</span><span class="sxs-lookup"><span data-stu-id="50cff-218">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="50cff-219">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50cff-219">RELATED LINKS</span></span>

