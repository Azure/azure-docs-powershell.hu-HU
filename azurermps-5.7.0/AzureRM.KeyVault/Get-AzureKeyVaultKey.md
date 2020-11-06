---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: eaddfaa6be725d588c8856031a34e1bdefcc3892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500583"
---
# <span data-ttu-id="f8b54-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f8b54-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="f8b54-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8b54-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b54-103">Beolvassa a kulcsok kulcsát.</span><span class="sxs-lookup"><span data-stu-id="f8b54-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8b54-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8b54-104">SYNTAX</span></span>

### <span data-ttu-id="f8b54-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8b54-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8b54-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="f8b54-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8b54-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="f8b54-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8b54-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="f8b54-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8b54-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="f8b54-109">ByInputObjectKeyName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8b54-110">ByKInputObjecteyVersions</span><span class="sxs-lookup"><span data-stu-id="f8b54-110">ByKInputObjecteyVersions</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8b54-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8b54-111">DESCRIPTION</span></span>
<span data-ttu-id="f8b54-112">A **Get-AzureKeyVaultKey** parancsmag Azure Key Vault-kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="f8b54-112">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="f8b54-113">Ez a parancsmag a **Microsoft. Azure. commands. kulcskezelő. models.** vagy a kulcsfájl vagy **az összes kulcskezelő** objektum listáját adja meg egy kulcs-boltozatban vagy egy verzióban.</span><span class="sxs-lookup"><span data-stu-id="f8b54-113">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="f8b54-114">Példák</span><span class="sxs-lookup"><span data-stu-id="f8b54-114">EXAMPLES</span></span>

### <span data-ttu-id="f8b54-115">1. példa: a billentyűk lekérése a fő boltozaton</span><span class="sxs-lookup"><span data-stu-id="f8b54-115">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="f8b54-116">Ez a parancs a contoso nevű fő boltozat összes kulcsát kinyeri.</span><span class="sxs-lookup"><span data-stu-id="f8b54-116">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="f8b54-117">2. példa: a kulcs aktuális verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f8b54-117">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="f8b54-118">Ez a parancs beolvassa a ITPfx nevű kulcs aktuális verzióját a contoso nevű kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="f8b54-118">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="f8b54-119">3. példa: a kulcsok minden verziójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="f8b54-119">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="f8b54-120">Ez a parancs a ITPfx nevű kulcsot a contoso vaultnamed kulcsában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f8b54-120">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="f8b54-121">Példa 4: a kulcs meghatározott verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f8b54-121">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="f8b54-122">Ez a parancs beolvassa a ITPfx nevű kulcs egy bizonyos verzióját a contoso nevű kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="f8b54-122">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="f8b54-123">Miután futtatta ezt a parancsot, a $Key objektumban való navigálással ellenőrizheti a billentyűk különböző tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="f8b54-123">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="f8b54-124">5. példa: a kulcsfájl által törölt, de nem törölt billentyűk beolvasása.</span><span class="sxs-lookup"><span data-stu-id="f8b54-124">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="f8b54-125">Ez a parancs az összes korábban törölt, de nem törölt billentyűt beilleszti a contoso nevű billentyűvel.</span><span class="sxs-lookup"><span data-stu-id="f8b54-125">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="f8b54-126">6. példa: a kulcsfájl a ITPfx, amelyet töröltek, de nem tisztítják meg.</span><span class="sxs-lookup"><span data-stu-id="f8b54-126">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="f8b54-127">Ez a parancs a contoso nevű kulcsfájl által korábban törölt, de el nem távolított kulcs ITPfx kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f8b54-127">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="f8b54-128">Ez a parancs metaadatokat ad vissza, például a törlési dátumot, valamint a törölt kulcs ütemezett leöblítési dátumát.</span><span class="sxs-lookup"><span data-stu-id="f8b54-128">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="f8b54-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8b54-129">PARAMETERS</span></span>

### <span data-ttu-id="f8b54-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b54-130">-DefaultProfile</span></span>
<span data-ttu-id="f8b54-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f8b54-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b54-132">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="f8b54-132">-IncludeVersions</span></span>
<span data-ttu-id="f8b54-133">Azt jelzi, hogy ez a parancsmag a kulcsok minden verzióját bekapja.</span><span class="sxs-lookup"><span data-stu-id="f8b54-133">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="f8b54-134">A kulcsok jelenlegi verziója az első a listán.</span><span class="sxs-lookup"><span data-stu-id="f8b54-134">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="f8b54-135">Ha ezt a paramétert adja meg, a *nevet* és a *VaultName* paramétereket is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="f8b54-135">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="f8b54-136">Ha nem adja meg a *IncludeVersions* paramétert, ez a parancsmag a megadott *nevű* kulcs aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f8b54-136">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions, ByKInputObjecteyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b54-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8b54-137">-InputObject</span></span>
<span data-ttu-id="f8b54-138">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="f8b54-138">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8b54-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f8b54-139">-InRemovedState</span></span>
<span data-ttu-id="f8b54-140">Annak megadása, hogy a kimenetben a korábban törölt billentyűk jelenjenek-e meg</span><span class="sxs-lookup"><span data-stu-id="f8b54-140">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b54-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f8b54-141">-Name</span></span>
<span data-ttu-id="f8b54-142">A beolvasott kulcs kötegének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8b54-142">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8b54-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f8b54-143">-VaultName</span></span>
<span data-ttu-id="f8b54-144">Annak a kulcsnak a nevét adja meg, amelyből a parancsmag kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="f8b54-144">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="f8b54-145">Ez a parancsmag a kulcsfájl teljesen minősített tartománynevét (FQDN) építi fel a paraméter által megadott név és a kijelölt környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="f8b54-145">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8b54-146">-Verzió</span><span class="sxs-lookup"><span data-stu-id="f8b54-146">-Version</span></span>
<span data-ttu-id="f8b54-147">A kulcs verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8b54-147">Specifies the key version.</span></span>
<span data-ttu-id="f8b54-148">Ez a parancsmag a kulcs teljes tartománynevét, az aktuálisan kijelölt környezetet, a kulcs nevét és a kulcs verziószámát építi fel.</span><span class="sxs-lookup"><span data-stu-id="f8b54-148">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByInputObjectKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8b54-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b54-149">CommonParameters</span></span>
<span data-ttu-id="f8b54-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8b54-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b54-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8b54-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b54-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8b54-152">INPUTS</span></span>

### <span data-ttu-id="f8b54-153">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="f8b54-153">String</span></span>

## <span data-ttu-id="f8b54-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8b54-154">OUTPUTS</span></span>

### <span data-ttu-id="f8b54-155">Lista<Microsoft. Azure. commands. PSKeyVaultKeyIdentityItem. models.>, Microsoft. Azure. commands. PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem> Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f8b54-155">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="f8b54-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8b54-156">NOTES</span></span>

## <span data-ttu-id="f8b54-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8b54-157">RELATED LINKS</span></span>

[<span data-ttu-id="f8b54-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f8b54-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="f8b54-159">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f8b54-159">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="f8b54-160">Visszavonás – AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="f8b54-160">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="f8b54-161">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="f8b54-161">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

