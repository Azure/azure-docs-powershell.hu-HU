---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: a934b1d96b260a6615acfbe02b15c80e6d3bfae5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400552"
---
# <span data-ttu-id="fdac2-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fdac2-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="fdac2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdac2-102">SYNOPSIS</span></span>
<span data-ttu-id="fdac2-103">Lekérte a kulcstár kulcsait.</span><span class="sxs-lookup"><span data-stu-id="fdac2-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="fdac2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fdac2-104">SYNTAX</span></span>

### <span data-ttu-id="fdac2-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fdac2-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdac2-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="fdac2-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdac2-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="fdac2-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdac2-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="fdac2-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdac2-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="fdac2-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdac2-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="fdac2-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdac2-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="fdac2-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdac2-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="fdac2-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdac2-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="fdac2-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdac2-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fdac2-114">DESCRIPTION</span></span>
<span data-ttu-id="fdac2-115">A **Get-AzKeyVaultKey** parancsmag azure-kulcstár-kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="fdac2-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="fdac2-116">Ez a parancsmag egy adott **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** parancsot vagy egy kulcstárban vagy verziók szerint az összes **KeyBundle-objektum** listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="fdac2-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="fdac2-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fdac2-117">EXAMPLES</span></span>

### <span data-ttu-id="fdac2-118">1. példa: Az összes kulcs lekérte a kulcstárban található összes kulcsot</span><span class="sxs-lookup"><span data-stu-id="fdac2-118">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso'

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="fdac2-119">Ez a parancs a Contoso nevű kulcstár összes kulcsát megkapja.</span><span class="sxs-lookup"><span data-stu-id="fdac2-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="fdac2-120">2. példa: Kulcs aktuális verziójának lekérte</span><span class="sxs-lookup"><span data-stu-id="fdac2-120">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="fdac2-121">Ez a parancs a Contoso nevű kulcstárban a Test1 nevű kulcs aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fdac2-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="fdac2-122">3. példa: Kulcs összes verziójának lekérte</span><span class="sxs-lookup"><span data-stu-id="fdac2-122">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="fdac2-123">Ez a parancs az ITPfx nevű összes verziót megkapja a Contoso nevű kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="fdac2-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="fdac2-124">4. példa: Kulcs adott verziójának lekérte</span><span class="sxs-lookup"><span data-stu-id="fdac2-124">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="fdac2-125">Ez a parancs a Contoso nevű kulcstárban a Test1 nevű kulcs adott verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fdac2-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="fdac2-126">A parancs futtatása után a kulcs különféle tulajdonságainak vizsgálatához navigálhat a $Key objektumban.</span><span class="sxs-lookup"><span data-stu-id="fdac2-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="fdac2-127">5. példa: Szerezze be az összes olyan kulcsot, amely törlődött, de nem lett véglegesen törölve ehhez a kulcstárhoz.</span><span class="sxs-lookup"><span data-stu-id="fdac2-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="fdac2-128">Ez a parancs a Korábban törölt, de nem véglegesen törölt összes kulcsot a Contoso nevű kulcstárba kapja.</span><span class="sxs-lookup"><span data-stu-id="fdac2-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="fdac2-129">6. példa: A kulcstár törölt, de nem véglegesen törölt ITPfx kulcsát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fdac2-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3/1af807cc331a49d0b52b7c75e1b2366e
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="fdac2-130">Ez a parancs a Korábban törölt, de nem véglegesen törölt kulcstesztet kapja meg a Contoso nevű kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="fdac2-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="fdac2-131">Ez a parancs metaadatokat, például törlési dátumot és a törölt kulcs ütemezett végleges törlési dátumát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="fdac2-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="fdac2-132">7. példa: Az összes kulcs behozása egy kulcstárba szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="fdac2-132">Example 7: Get all the keys in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName "test*"

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="fdac2-133">Ez a parancs a Contoso nevű kulcstár "teszt" kezdetű összes kulcsát megkapja.</span><span class="sxs-lookup"><span data-stu-id="fdac2-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

## <span data-ttu-id="fdac2-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdac2-134">PARAMETERS</span></span>

### <span data-ttu-id="fdac2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdac2-135">-DefaultProfile</span></span>
<span data-ttu-id="fdac2-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fdac2-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdac2-137">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="fdac2-137">-IncludeVersions</span></span>
<span data-ttu-id="fdac2-138">Azt jelzi, hogy ez a parancsmag a kulcs összes verzióját lekérte.</span><span class="sxs-lookup"><span data-stu-id="fdac2-138">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="fdac2-139">A kulcs aktuális verziója az első a listában.</span><span class="sxs-lookup"><span data-stu-id="fdac2-139">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="fdac2-140">Ha ezt a paramétert adja meg, a *Name* és *a VaultName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="fdac2-140">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="fdac2-141">Ha nem adja meg az *IncludeVersions* paramétert, ez a parancsmag a kulcs aktuális verzióját kapja meg a megadott *névvel.*</span><span class="sxs-lookup"><span data-stu-id="fdac2-141">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, ByInputObjectKeyVersions, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdac2-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdac2-142">-InputObject</span></span>
<span data-ttu-id="fdac2-143">KeyVault objektum.</span><span class="sxs-lookup"><span data-stu-id="fdac2-143">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdac2-144">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="fdac2-144">-InRemovedState</span></span>
<span data-ttu-id="fdac2-145">Megadja, hogy a korábban törölt billentyűket a kimenetben is meg kell-e mutatni.</span><span class="sxs-lookup"><span data-stu-id="fdac2-145">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdac2-146">-Name</span><span class="sxs-lookup"><span data-stu-id="fdac2-146">-Name</span></span>
<span data-ttu-id="fdac2-147">A lekért kulcscsomag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdac2-147">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="fdac2-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdac2-148">-ResourceId</span></span>
<span data-ttu-id="fdac2-149">KeyVault-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fdac2-149">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdac2-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fdac2-150">-VaultName</span></span>
<span data-ttu-id="fdac2-151">Annak a kulcstárnak a neve, amelyből a parancsmag kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="fdac2-151">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="fdac2-152">Ez a parancsmag egy kulcstár teljes tartománynevét (FQDN) építi fel a paraméter által megadott név és a kiválasztott környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="fdac2-152">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdac2-153">-Version</span><span class="sxs-lookup"><span data-stu-id="fdac2-153">-Version</span></span>
<span data-ttu-id="fdac2-154">A kulcsverziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdac2-154">Specifies the key version.</span></span>
<span data-ttu-id="fdac2-155">Ez a parancsmag egy kulcs FQDN-ét építi fel a kulcs tárolóneve, az aktuálisan kiválasztott környezet, a kulcs neve és a kulcsverzió alapján.</span><span class="sxs-lookup"><span data-stu-id="fdac2-155">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByInputObjectKeyName, ByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdac2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdac2-156">CommonParameters</span></span>
<span data-ttu-id="fdac2-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdac2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdac2-158">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdac2-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdac2-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fdac2-159">INPUTS</span></span>

### <span data-ttu-id="fdac2-160">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="fdac2-160">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="fdac2-161">System.String</span><span class="sxs-lookup"><span data-stu-id="fdac2-161">System.String</span></span>

## <span data-ttu-id="fdac2-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdac2-162">OUTPUTS</span></span>

### <span data-ttu-id="fdac2-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fdac2-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="fdac2-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fdac2-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="fdac2-165">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fdac2-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="fdac2-166">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultKey billentyű</span><span class="sxs-lookup"><span data-stu-id="fdac2-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="fdac2-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fdac2-167">NOTES</span></span>

## <span data-ttu-id="fdac2-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdac2-168">RELATED LINKS</span></span>

[<span data-ttu-id="fdac2-169">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fdac2-169">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="fdac2-170">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fdac2-170">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="fdac2-171">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="fdac2-171">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)


