---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 81276c0896d6cb6685d3ce3ee71bb72cb39b690a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920529"
---
# <span data-ttu-id="5533e-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5533e-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="5533e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5533e-102">SYNOPSIS</span></span>
<span data-ttu-id="5533e-103">Lekérte a kulcstár kulcsait.</span><span class="sxs-lookup"><span data-stu-id="5533e-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="5533e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5533e-104">SYNTAX</span></span>

### <span data-ttu-id="5533e-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5533e-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="5533e-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="5533e-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-108">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="5533e-108">HsmByKeyName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-109">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="5533e-109">HsmByVaultName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-110">HsmByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="5533e-110">HsmByKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-111">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="5533e-111">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-112">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="5533e-112">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-113">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="5533e-113">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-114">HsmByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="5533e-114">HsmByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-115">HsmByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="5533e-115">HsmByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-116">HsmByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="5533e-116">HsmByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-117">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="5533e-117">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-118">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="5533e-118">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-119">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="5533e-119">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-120">HsmByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="5533e-120">HsmByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-121">HsmByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="5533e-121">HsmByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5533e-122">HsmByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="5533e-122">HsmByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5533e-123">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5533e-123">DESCRIPTION</span></span>
<span data-ttu-id="5533e-124">A **Get-AzKeyVaultKey** parancsmag azure-kulcstár-kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="5533e-124">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="5533e-125">Ez a parancsmag egy adott **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** parancsot vagy egy kulcstárban vagy verziók szerint az összes **KeyBundle-objektum** listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="5533e-125">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="5533e-126">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5533e-126">EXAMPLES</span></span>

### <span data-ttu-id="5533e-127">1. példa: Az összes kulcs lekérte a kulcstárban található összes kulcsot</span><span class="sxs-lookup"><span data-stu-id="5533e-127">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="5533e-128">Ez a parancs a Contoso nevű kulcstár összes kulcsát megkapja.</span><span class="sxs-lookup"><span data-stu-id="5533e-128">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="5533e-129">2. példa: Kulcs aktuális verziójának lekérte</span><span class="sxs-lookup"><span data-stu-id="5533e-129">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="5533e-130">Ez a parancs a Contoso nevű kulcstárban a Test1 nevű kulcs aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5533e-130">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="5533e-131">3. példa: Kulcs összes verziójának lekérte</span><span class="sxs-lookup"><span data-stu-id="5533e-131">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="5533e-132">Ez a parancs az ITPfx nevű összes verziót megkapja a Contoso nevű kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="5533e-132">This command gets all versions the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="5533e-133">4. példa: Kulcs adott verziójának lekérte</span><span class="sxs-lookup"><span data-stu-id="5533e-133">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="5533e-134">Ez a parancs a Contoso nevű kulcstárban lekérte a test1 nevű kulcs egy adott verzióját.</span><span class="sxs-lookup"><span data-stu-id="5533e-134">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="5533e-135">A parancs futtatása után a kulcs különféle tulajdonságainak vizsgálatához navigálhat a $Key objektumban.</span><span class="sxs-lookup"><span data-stu-id="5533e-135">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="5533e-136">5. példa: A kulcstár összes törölt, de véglegesen nem véglegesen törölt kulcsának be szereznie</span><span class="sxs-lookup"><span data-stu-id="5533e-136">Example 5: Get all the keys that have been deleted but not purged for this key vault</span></span>
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

<span data-ttu-id="5533e-137">Ez a parancs a Korábban törölt, de nem véglegesen törölt összes kulcsot a Contoso nevű kulcstárba kapja.</span><span class="sxs-lookup"><span data-stu-id="5533e-137">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="5533e-138">6. példa: A kulcstár törölt, de nem véglegesen törölt ITPfx kulcsát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5533e-138">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="5533e-139">Ez a parancs a Korábban törölt, de nem véglegesen törölt kulcstesztet kapja meg a Contoso nevű kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="5533e-139">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="5533e-140">Ez a parancs metaadatokat, például törlési dátumot és a törölt kulcs ütemezett végleges törlési dátumát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="5533e-140">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="5533e-141">7. példa: Az összes kulcs behozása egy kulcstárba szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="5533e-141">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="5533e-142">Ez a parancs a Contoso nevű kulcstárban a "teszt" kezdetű összes kulcsot megkapja.</span><span class="sxs-lookup"><span data-stu-id="5533e-142">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="5533e-143">8. példa: Nyilvános kulcs letöltése .pem fájlként</span><span class="sxs-lookup"><span data-stu-id="5533e-143">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="5533e-144">Az RSA-kulcs nyilvános kulcsát a paraméter megadásával töltheti `-OutFile` le.</span><span class="sxs-lookup"><span data-stu-id="5533e-144">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="5533e-145">Ez a lépés a HSM által védett kulcsok importálása az Azure-kulcstárba.</span><span class="sxs-lookup"><span data-stu-id="5533e-145">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="5533e-146">Lásd: https://docs.microsoft.com/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="5533e-146">See https://docs.microsoft.com/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="5533e-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5533e-147">PARAMETERS</span></span>

### <span data-ttu-id="5533e-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5533e-148">-DefaultProfile</span></span>
<span data-ttu-id="5533e-149">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5533e-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5533e-150">-HsmName</span><span class="sxs-lookup"><span data-stu-id="5533e-150">-HsmName</span></span>
<span data-ttu-id="5533e-151">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="5533e-151">HSM name.</span></span> <span data-ttu-id="5533e-152">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="5533e-152">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName, HsmByVaultName, HsmByKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5533e-153">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="5533e-153">-HsmObject</span></span>
<span data-ttu-id="5533e-154">HSM-objektum.</span><span class="sxs-lookup"><span data-stu-id="5533e-154">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObjectVaultName, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5533e-155">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="5533e-155">-HsmResourceId</span></span>
<span data-ttu-id="5533e-156">HSM Resource Id.</span><span class="sxs-lookup"><span data-stu-id="5533e-156">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceIdVaultName, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5533e-157">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="5533e-157">-IncludeVersions</span></span>
<span data-ttu-id="5533e-158">Azt jelzi, hogy ez a parancsmag a kulcs összes verzióját lekérte.</span><span class="sxs-lookup"><span data-stu-id="5533e-158">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="5533e-159">A kulcs aktuális verziója az első a listában.</span><span class="sxs-lookup"><span data-stu-id="5533e-159">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="5533e-160">Ha ezt a paramétert adja meg, a *Name* és *a VaultName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="5533e-160">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="5533e-161">Ha nem adja meg az *IncludeVersions* paramétert, ez a parancsmag a kulcs aktuális verzióját kapja meg a megadott *névvel.*</span><span class="sxs-lookup"><span data-stu-id="5533e-161">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, HsmByKeyVersions, ByInputObjectKeyVersions, HsmByInputObjectKeyVersions, ByResourceIdKeyVersions, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5533e-162">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5533e-162">-InputObject</span></span>
<span data-ttu-id="5533e-163">KeyVault objektum.</span><span class="sxs-lookup"><span data-stu-id="5533e-163">KeyVault object.</span></span>

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

### <span data-ttu-id="5533e-164">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="5533e-164">-InRemovedState</span></span>
<span data-ttu-id="5533e-165">Megadja, hogy a korábban törölt billentyűket a kimenetben is meg kell-e mutatni.</span><span class="sxs-lookup"><span data-stu-id="5533e-165">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5533e-166">-Name</span><span class="sxs-lookup"><span data-stu-id="5533e-166">-Name</span></span>
<span data-ttu-id="5533e-167">A lekért kulcscsomag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5533e-167">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, HsmByKeyName, HsmByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="5533e-168">-OutFile</span><span class="sxs-lookup"><span data-stu-id="5533e-168">-OutFile</span></span>
<span data-ttu-id="5533e-169">Azt a kimeneti fájlt adja meg, amelybe ez a parancsmag menti a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="5533e-169">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="5533e-170">A nyilvános kulcsot a rendszer alapértelmezés szerint PEM formátumban menti.</span><span class="sxs-lookup"><span data-stu-id="5533e-170">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="5533e-171">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5533e-171">-ResourceId</span></span>
<span data-ttu-id="5533e-172">KeyVault-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5533e-172">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5533e-173">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5533e-173">-VaultName</span></span>
<span data-ttu-id="5533e-174">Annak a kulcstárnak a neve, amelyből a parancsmag kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="5533e-174">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="5533e-175">Ez a parancsmag egy kulcstár teljes tartománynevét (FQDN) építi fel a paraméter által megadott név és a kiválasztott környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="5533e-175">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="5533e-176">-Version</span><span class="sxs-lookup"><span data-stu-id="5533e-176">-Version</span></span>
<span data-ttu-id="5533e-177">A kulcsverziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="5533e-177">Specifies the key version.</span></span>
<span data-ttu-id="5533e-178">Ez a parancsmag egy kulcs FQDN-ét építi fel a kulcs tárolóneve, az aktuálisan kiválasztott környezet, a kulcs neve és a kulcsverzió alapján.</span><span class="sxs-lookup"><span data-stu-id="5533e-178">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName, ByInputObjectKeyName, HsmByInputObjectKeyName, ByResourceIdKeyName, HsmByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5533e-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5533e-179">CommonParameters</span></span>
<span data-ttu-id="5533e-180">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5533e-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5533e-181">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5533e-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5533e-182">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5533e-182">INPUTS</span></span>

### <span data-ttu-id="5533e-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5533e-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="5533e-184">System.String</span><span class="sxs-lookup"><span data-stu-id="5533e-184">System.String</span></span>

## <span data-ttu-id="5533e-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5533e-185">OUTPUTS</span></span>

### <span data-ttu-id="5533e-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5533e-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="5533e-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5533e-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="5533e-188">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5533e-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="5533e-189">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultKey billentyű</span><span class="sxs-lookup"><span data-stu-id="5533e-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="5533e-190">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5533e-190">NOTES</span></span>

## <span data-ttu-id="5533e-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5533e-191">RELATED LINKS</span></span>

[<span data-ttu-id="5533e-192">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5533e-192">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="5533e-193">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5533e-193">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="5533e-194">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="5533e-194">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="5533e-195">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="5533e-195">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

