---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://go.microsoft.com/fwlink/?LinkId=690297
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: 48d050623ea75bed1aee1b78a26bf81bf3305e06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493498"
---
# <span data-ttu-id="91ba2-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="91ba2-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="91ba2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91ba2-102">SYNOPSIS</span></span>
<span data-ttu-id="91ba2-103">Beolvassa a kulcsok kulcsát.</span><span class="sxs-lookup"><span data-stu-id="91ba2-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91ba2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91ba2-104">SYNTAX</span></span>

### <span data-ttu-id="91ba2-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91ba2-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91ba2-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="91ba2-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91ba2-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="91ba2-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91ba2-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="91ba2-108">ByDeletedKey</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91ba2-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="91ba2-109">DESCRIPTION</span></span>
<span data-ttu-id="91ba2-110">A **Get-AzureKeyVaultKey** parancsmag Azure Key Vault-kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="91ba2-110">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="91ba2-111">Ez a parancsmag a **Microsoft. Azure. commands. kulcskezelő. models.** vagy a kulcsfájl vagy **az összes kulcskezelő** objektum listáját adja meg egy kulcs-boltozatban vagy egy verzióban.</span><span class="sxs-lookup"><span data-stu-id="91ba2-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="91ba2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="91ba2-112">EXAMPLES</span></span>

### <span data-ttu-id="91ba2-113">1. példa: a billentyűk lekérése a fő boltozaton</span><span class="sxs-lookup"><span data-stu-id="91ba2-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="91ba2-114">Ez a parancs a contoso nevű fő boltozat összes kulcsát kinyeri.</span><span class="sxs-lookup"><span data-stu-id="91ba2-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="91ba2-115">2. példa: a kulcs aktuális verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="91ba2-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="91ba2-116">Ez a parancs beolvassa a ITPfx nevű kulcs aktuális verzióját a contoso nevű kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="91ba2-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="91ba2-117">3. példa: a kulcsok minden verziójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="91ba2-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="91ba2-118">Ez a parancs a ITPfx nevű kulcsot a contoso vaultnamed kulcsában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="91ba2-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="91ba2-119">Példa 4: a kulcs meghatározott verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="91ba2-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="91ba2-120">Ez a parancs beolvassa a ITPfx nevű kulcs egy bizonyos verzióját a contoso nevű kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="91ba2-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="91ba2-121">Miután futtatta ezt a parancsot, a $Key objektumban való navigálással ellenőrizheti a billentyűk különböző tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="91ba2-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="91ba2-122">5. példa: a kulcsfájl által törölt, de nem törölt billentyűk beolvasása.</span><span class="sxs-lookup"><span data-stu-id="91ba2-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="91ba2-123">Ez a parancs az összes korábban törölt, de nem törölt billentyűt beilleszti a contoso nevű billentyűvel.</span><span class="sxs-lookup"><span data-stu-id="91ba2-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="91ba2-124">6. példa: a kulcsfájl a ITPfx, amelyet töröltek, de nem tisztítják meg.</span><span class="sxs-lookup"><span data-stu-id="91ba2-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="91ba2-125">Ez a parancs a contoso nevű kulcsfájl által korábban törölt, de el nem távolított kulcs ITPfx kapja meg.</span><span class="sxs-lookup"><span data-stu-id="91ba2-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="91ba2-126">Ez a parancs metaadatokat ad vissza, például a törlési dátumot, valamint a törölt kulcs ütemezett leöblítési dátumát.</span><span class="sxs-lookup"><span data-stu-id="91ba2-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="91ba2-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91ba2-127">PARAMETERS</span></span>

### <span data-ttu-id="91ba2-128">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="91ba2-128">-IncludeVersions</span></span>
<span data-ttu-id="91ba2-129">Azt jelzi, hogy ez a parancsmag a kulcsok minden verzióját bekapja.</span><span class="sxs-lookup"><span data-stu-id="91ba2-129">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="91ba2-130">A kulcsok jelenlegi verziója az első a listán.</span><span class="sxs-lookup"><span data-stu-id="91ba2-130">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="91ba2-131">Ha ezt a paramétert adja meg, a *nevet* és a *VaultName* paramétereket is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="91ba2-131">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="91ba2-132">Ha nem adja meg a *IncludeVersions* paramétert, ez a parancsmag a megadott *nevű* kulcs aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="91ba2-132">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ba2-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="91ba2-133">-InRemovedState</span></span>
<span data-ttu-id="91ba2-134">Itt adhatja meg, hogy megjelenjen-e a korábban törölt kulcsok a kimenetben.</span><span class="sxs-lookup"><span data-stu-id="91ba2-134">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ba2-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91ba2-135">-Name</span></span>
<span data-ttu-id="91ba2-136">A beolvasott kulcs kötegének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91ba2-136">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91ba2-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="91ba2-137">-VaultName</span></span>
<span data-ttu-id="91ba2-138">Annak a kulcsnak a nevét adja meg, amelyből a parancsmag kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="91ba2-138">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="91ba2-139">Ez a parancsmag a kulcsfájl teljesen minősített tartománynevét (FQDN) építi fel a paraméter által megadott név és a kijelölt környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="91ba2-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91ba2-140">-Verzió</span><span class="sxs-lookup"><span data-stu-id="91ba2-140">-Version</span></span>
<span data-ttu-id="91ba2-141">A kulcs verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91ba2-141">Specifies the key version.</span></span>
<span data-ttu-id="91ba2-142">Ez a parancsmag a kulcs teljes tartománynevét, az aktuálisan kijelölt környezetet, a kulcs nevét és a kulcs verziószámát építi fel.</span><span class="sxs-lookup"><span data-stu-id="91ba2-142">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91ba2-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ba2-143">-DefaultProfile</span></span>
<span data-ttu-id="91ba2-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91ba2-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ba2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ba2-145">CommonParameters</span></span>
<span data-ttu-id="91ba2-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91ba2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ba2-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91ba2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ba2-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91ba2-148">INPUTS</span></span>

### <span data-ttu-id="91ba2-149">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="91ba2-149">String</span></span>

## <span data-ttu-id="91ba2-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91ba2-150">OUTPUTS</span></span>

### <span data-ttu-id="91ba2-151">Lista<Microsoft. Azure. commands. KeyIdentityItem. models.>, Microsoft. Azure. commands.-Vault. models. debundle, List<Microsoft. Azure. Command. DeletedKeyBundle. DeletedKeyIdentityItem>, Microsoft. Azure. Command.</span><span class="sxs-lookup"><span data-stu-id="91ba2-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="91ba2-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91ba2-152">NOTES</span></span>

## <span data-ttu-id="91ba2-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91ba2-153">RELATED LINKS</span></span>

[<span data-ttu-id="91ba2-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="91ba2-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="91ba2-155">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="91ba2-155">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="91ba2-156">Visszavonás – AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="91ba2-156">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="91ba2-157">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="91ba2-157">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

