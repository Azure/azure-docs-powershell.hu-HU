---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: a0d79aa0d1699f6e6645f86475732c235447342f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842138"
---
# <span data-ttu-id="d2e8a-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d2e8a-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="d2e8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e8a-103">Beolvassa a kulcsok kulcsát.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="d2e8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2e8a-104">SYNTAX</span></span>

### <span data-ttu-id="d2e8a-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2e8a-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2e8a-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="d2e8a-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2e8a-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="d2e8a-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2e8a-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="d2e8a-108">ByDeletedKey</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2e8a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2e8a-109">DESCRIPTION</span></span>
<span data-ttu-id="d2e8a-110">A **Get-AzKeyVaultKey** parancsmag Azure Key Vault-kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-110">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="d2e8a-111">Ez a parancsmag a **Microsoft. Azure. commands. kulcskezelő. models.** vagy a kulcsfájl vagy **az összes kulcskezelő** objektum listáját adja meg egy kulcs-boltozatban vagy egy verzióban.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="d2e8a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d2e8a-112">EXAMPLES</span></span>

### <span data-ttu-id="d2e8a-113">1. példa: a billentyűk lekérése a fő boltozaton</span><span class="sxs-lookup"><span data-stu-id="d2e8a-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="d2e8a-114">Ez a parancs a contoso nevű fő boltozat összes kulcsát kinyeri.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="d2e8a-115">2. példa: a kulcs aktuális verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d2e8a-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="d2e8a-116">Ez a parancs beolvassa a ITPfx nevű kulcs aktuális verzióját a contoso nevű kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="d2e8a-117">3. példa: a kulcsok minden verziójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="d2e8a-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="d2e8a-118">Ez a parancs a ITPfx nevű kulcsot a contoso vaultnamed kulcsában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="d2e8a-119">Példa 4: a kulcs meghatározott verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d2e8a-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="d2e8a-120">Ez a parancs beolvassa a ITPfx nevű kulcs egy bizonyos verzióját a contoso nevű kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="d2e8a-121">Miután futtatta ezt a parancsot, a $Key objektumban való navigálással ellenőrizheti a billentyűk különböző tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="d2e8a-122">5. példa: a kulcsfájl által törölt, de nem törölt billentyűk beolvasása.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="d2e8a-123">Ez a parancs az összes korábban törölt, de nem törölt billentyűt beilleszti a contoso nevű billentyűvel.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="d2e8a-124">6. példa: a kulcsfájl a ITPfx, amelyet töröltek, de nem tisztítják meg.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="d2e8a-125">Ez a parancs a contoso nevű kulcsfájl által korábban törölt, de el nem távolított kulcs ITPfx kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="d2e8a-126">Ez a parancs metaadatokat ad vissza, például a törlési dátumot, valamint a törölt kulcs ütemezett leöblítési dátumát.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="d2e8a-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2e8a-127">PARAMETERS</span></span>

### <span data-ttu-id="d2e8a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e8a-128">-DefaultProfile</span></span>
<span data-ttu-id="d2e8a-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d2e8a-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e8a-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="d2e8a-130">-IncludeVersions</span></span>
<span data-ttu-id="d2e8a-131">Azt jelzi, hogy ez a parancsmag a kulcsok minden verzióját bekapja.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-131">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="d2e8a-132">A kulcsok jelenlegi verziója az első a listán.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-132">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="d2e8a-133">Ha ezt a paramétert adja meg, a *nevet* és a *VaultName* paramétereket is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-133">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="d2e8a-134">Ha nem adja meg a *IncludeVersions* paramétert, ez a parancsmag a megadott *nevű* kulcs aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-134">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e8a-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d2e8a-135">-InRemovedState</span></span>
<span data-ttu-id="d2e8a-136">Annak megadása, hogy a kimenetben a korábban törölt billentyűk jelenjenek-e meg</span><span class="sxs-lookup"><span data-stu-id="d2e8a-136">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e8a-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d2e8a-137">-Name</span></span>
<span data-ttu-id="d2e8a-138">A beolvasott kulcs kötegének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-138">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e8a-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d2e8a-139">-VaultName</span></span>
<span data-ttu-id="d2e8a-140">Annak a kulcsnak a nevét adja meg, amelyből a parancsmag kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-140">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="d2e8a-141">Ez a parancsmag a kulcsfájl teljesen minősített tartománynevét (FQDN) építi fel a paraméter által megadott név és a kijelölt környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-141">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e8a-142">-Verzió</span><span class="sxs-lookup"><span data-stu-id="d2e8a-142">-Version</span></span>
<span data-ttu-id="d2e8a-143">A kulcs verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-143">Specifies the key version.</span></span>
<span data-ttu-id="d2e8a-144">Ez a parancsmag a kulcs teljes tartománynevét, az aktuálisan kijelölt környezetet, a kulcs nevét és a kulcs verziószámát építi fel.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-144">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e8a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e8a-145">CommonParameters</span></span>
<span data-ttu-id="d2e8a-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2e8a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e8a-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e8a-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e8a-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2e8a-148">INPUTS</span></span>

### <span data-ttu-id="d2e8a-149">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="d2e8a-149">String</span></span>

## <span data-ttu-id="d2e8a-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2e8a-150">OUTPUTS</span></span>

### <span data-ttu-id="d2e8a-151">Lista<Microsoft. Azure. commands. KeyIdentityItem. models.>, Microsoft. Azure. commands.-Vault. models. debundle, List<Microsoft. Azure. Command. DeletedKeyBundle. DeletedKeyIdentityItem>, Microsoft. Azure. Command.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="d2e8a-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2e8a-152">NOTES</span></span>

## <span data-ttu-id="d2e8a-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2e8a-153">RELATED LINKS</span></span>

[<span data-ttu-id="d2e8a-154">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d2e8a-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="d2e8a-155">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d2e8a-155">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="d2e8a-156">Visszavonás – AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="d2e8a-156">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="d2e8a-157">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="d2e8a-157">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

