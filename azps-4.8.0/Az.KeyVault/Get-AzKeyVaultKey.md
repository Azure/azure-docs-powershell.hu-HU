---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 0de3582d9a5cbdaba8555cf53bd9038d3eaf15b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181739"
---
# <span data-ttu-id="bcbae-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bcbae-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="bcbae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bcbae-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbae-103">Beolvassa a kulcsok kulcsát.</span><span class="sxs-lookup"><span data-stu-id="bcbae-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="bcbae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bcbae-104">SYNTAX</span></span>

### <span data-ttu-id="bcbae-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bcbae-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcbae-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="bcbae-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcbae-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bcbae-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcbae-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="bcbae-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcbae-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="bcbae-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcbae-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bcbae-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcbae-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="bcbae-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcbae-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="bcbae-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcbae-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bcbae-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcbae-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="bcbae-114">DESCRIPTION</span></span>
<span data-ttu-id="bcbae-115">A **Get-AzKeyVaultKey** parancsmag Azure Key Vault-kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="bcbae-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="bcbae-116">Ez a parancsmag a **Microsoft. Azure. commands. kulcskezelő. models.** vagy a kulcsfájl vagy **az összes kulcskezelő** objektum listáját adja meg egy kulcs-boltozatban vagy egy verzióban.</span><span class="sxs-lookup"><span data-stu-id="bcbae-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="bcbae-117">Példák</span><span class="sxs-lookup"><span data-stu-id="bcbae-117">EXAMPLES</span></span>

### <span data-ttu-id="bcbae-118">1. példa: a billentyűk lekérése a fő boltozaton</span><span class="sxs-lookup"><span data-stu-id="bcbae-118">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="bcbae-119">Ez a parancs a contoso nevű fő boltozat összes kulcsát kinyeri.</span><span class="sxs-lookup"><span data-stu-id="bcbae-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="bcbae-120">2. példa: a kulcs aktuális verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="bcbae-120">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="bcbae-121">Ez a parancs beolvassa a test1 nevű kulcs aktuális verzióját a contoso nevű kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="bcbae-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="bcbae-122">3. példa: a kulcsok minden verziójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="bcbae-122">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="bcbae-123">Ez a parancs a ITPfx nevű kulcsot a contoso vaultnamed kulcsában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bcbae-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="bcbae-124">Példa 4: a kulcs meghatározott verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="bcbae-124">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="bcbae-125">Ez a parancs beolvassa a test1 nevű kulcs egy bizonyos verzióját a contoso nevű kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="bcbae-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="bcbae-126">Miután futtatta ezt a parancsot, a $Key objektumban való navigálással ellenőrizheti a billentyűk különböző tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="bcbae-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="bcbae-127">5. példa: a kulcsfájl által törölt, de nem törölt billentyűk beolvasása.</span><span class="sxs-lookup"><span data-stu-id="bcbae-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="bcbae-128">Ez a parancs az összes korábban törölt, de nem törölt billentyűt beilleszti a contoso nevű billentyűvel.</span><span class="sxs-lookup"><span data-stu-id="bcbae-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="bcbae-129">6. példa: a kulcsfájl a ITPfx, amelyet töröltek, de nem tisztítják meg.</span><span class="sxs-lookup"><span data-stu-id="bcbae-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="bcbae-130">Ez a parancs a contoso nevű kulcsfájl által korábban törölt, de el nem távolított kulcs test3 kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bcbae-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="bcbae-131">Ez a parancs metaadatokat ad vissza, például a törlési dátumot, valamint a törölt kulcs ütemezett leöblítési dátumát.</span><span class="sxs-lookup"><span data-stu-id="bcbae-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="bcbae-132">7. példa: a billentyűk lekérése szűréssel</span><span class="sxs-lookup"><span data-stu-id="bcbae-132">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="bcbae-133">Ez a parancs az összes olyan billentyűt megkapja a contoso nevű kulcsban, amely a "teszt" kifejezéssel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="bcbae-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="bcbae-134">8. példa: nyilvános kulcs letöltése. PEM fájlként</span><span class="sxs-lookup"><span data-stu-id="bcbae-134">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="bcbae-135">Az RSA-kulcsok nyilvános kulcsát a paraméter megadásával töltheti le `-OutFile` .</span><span class="sxs-lookup"><span data-stu-id="bcbae-135">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="bcbae-136">Ez egy lépés a HSM-védelemmel ellátott kulcsok az Azure Key Vault-ba történő importálásához.</span><span class="sxs-lookup"><span data-stu-id="bcbae-136">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="bcbae-137">Olvassa el https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="bcbae-137">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="bcbae-138">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bcbae-138">PARAMETERS</span></span>

### <span data-ttu-id="bcbae-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbae-139">-DefaultProfile</span></span>
<span data-ttu-id="bcbae-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bcbae-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcbae-141">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="bcbae-141">-IncludeVersions</span></span>
<span data-ttu-id="bcbae-142">Azt jelzi, hogy ez a parancsmag a kulcsok minden verzióját bekapja.</span><span class="sxs-lookup"><span data-stu-id="bcbae-142">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="bcbae-143">A kulcsok jelenlegi verziója az első a listán.</span><span class="sxs-lookup"><span data-stu-id="bcbae-143">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="bcbae-144">Ha ezt a paramétert adja meg, a *nevet* és a *VaultName* paramétereket is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="bcbae-144">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="bcbae-145">Ha nem adja meg a *IncludeVersions* paramétert, ez a parancsmag a megadott *nevű* kulcs aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bcbae-145">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

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

### <span data-ttu-id="bcbae-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcbae-146">-InputObject</span></span>
<span data-ttu-id="bcbae-147">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="bcbae-147">KeyVault object.</span></span>

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

### <span data-ttu-id="bcbae-148">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="bcbae-148">-InRemovedState</span></span>
<span data-ttu-id="bcbae-149">Annak megadása, hogy a kimenetben a korábban törölt billentyűk jelenjenek-e meg</span><span class="sxs-lookup"><span data-stu-id="bcbae-149">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="bcbae-150">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bcbae-150">-Name</span></span>
<span data-ttu-id="bcbae-151">A beolvasott kulcs kötegének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcbae-151">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcbae-152">-Fájl kilépése</span><span class="sxs-lookup"><span data-stu-id="bcbae-152">-OutFile</span></span>
<span data-ttu-id="bcbae-153">Azt a kimeneti fájlt adja meg, amelyre a parancsmag menti a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="bcbae-153">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="bcbae-154">A nyilvános kulcs alapértelmezés szerint PEM formátumban lett mentve.</span><span class="sxs-lookup"><span data-stu-id="bcbae-154">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="bcbae-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcbae-155">-ResourceId</span></span>
<span data-ttu-id="bcbae-156">A főkészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bcbae-156">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="bcbae-157">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bcbae-157">-VaultName</span></span>
<span data-ttu-id="bcbae-158">Annak a kulcsnak a nevét adja meg, amelyből a parancsmag kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="bcbae-158">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="bcbae-159">Ez a parancsmag a kulcsfájl teljesen minősített tartománynevét (FQDN) építi fel a paraméter által megadott név és a kijelölt környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="bcbae-159">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="bcbae-160">-Verzió</span><span class="sxs-lookup"><span data-stu-id="bcbae-160">-Version</span></span>
<span data-ttu-id="bcbae-161">A kulcs verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcbae-161">Specifies the key version.</span></span>
<span data-ttu-id="bcbae-162">Ez a parancsmag a kulcs teljes tartománynevét, az aktuálisan kijelölt környezetet, a kulcs nevét és a kulcs verziószámát építi fel.</span><span class="sxs-lookup"><span data-stu-id="bcbae-162">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="bcbae-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbae-163">CommonParameters</span></span>
<span data-ttu-id="bcbae-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bcbae-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbae-165">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bcbae-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbae-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcbae-166">INPUTS</span></span>

### <span data-ttu-id="bcbae-167">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="bcbae-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="bcbae-168">System. String</span><span class="sxs-lookup"><span data-stu-id="bcbae-168">System.String</span></span>

## <span data-ttu-id="bcbae-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcbae-169">OUTPUTS</span></span>

### <span data-ttu-id="bcbae-170">Microsoft. Azure. Command. PSKeyVaultKeyIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="bcbae-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="bcbae-171">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="bcbae-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="bcbae-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bcbae-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="bcbae-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bcbae-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="bcbae-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bcbae-174">NOTES</span></span>

## <span data-ttu-id="bcbae-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcbae-175">RELATED LINKS</span></span>

[<span data-ttu-id="bcbae-176">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bcbae-176">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="bcbae-177">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bcbae-177">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="bcbae-178">Visszavonás – AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="bcbae-178">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="bcbae-179">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="bcbae-179">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

