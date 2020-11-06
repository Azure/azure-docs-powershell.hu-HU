---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: 4b9799a0d2433b513b801a95ffd5c408bf8bdbf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496515"
---
# <span data-ttu-id="fac40-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="fac40-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="fac40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fac40-102">SYNOPSIS</span></span>
<span data-ttu-id="fac40-103">Frissíti a kulcsok attribútumait egy kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="fac40-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fac40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fac40-104">SYNTAX</span></span>

### <span data-ttu-id="fac40-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fac40-105">Default (Default)</span></span>
```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac40-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fac40-106">InputObject</span></span>
```
Set-AzureKeyVaultKeyAttribute [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fac40-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fac40-107">DESCRIPTION</span></span>
<span data-ttu-id="fac40-108">A **set-AzureKeyVaultKeyAttribute** parancsmag a kulcsok szerkeszthető attribútumait frissíti a kulcs boltozatakor.</span><span class="sxs-lookup"><span data-stu-id="fac40-108">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="fac40-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fac40-109">EXAMPLES</span></span>

### <span data-ttu-id="fac40-110">1. példa: kulcs módosítása az engedélyezéshez, és a lejárat dátuma és a címkék beállítása</span><span class="sxs-lookup"><span data-stu-id="fac40-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="fac40-111">Az első parancs egy **datetime** típusú objektumot hoz létre a **Get-Date** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="fac40-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="fac40-112">Ez az objektum két év múlva adja meg a jövőbeli időpontot.</span><span class="sxs-lookup"><span data-stu-id="fac40-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="fac40-113">A parancs a $Expires változóban tárolja a dátumot.</span><span class="sxs-lookup"><span data-stu-id="fac40-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="fac40-114">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="fac40-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="fac40-115">A második parancs létrehoz egy változót, amely a nagy súlyosságú és a számviteli adatok címkézését tárolja.</span><span class="sxs-lookup"><span data-stu-id="fac40-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="fac40-116">A végleges parancs módosítja a ITSoftware nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="fac40-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="fac40-117">A parancs engedélyezi a kulcsot, a lejárati időt az $Expires tárolt időpontra állítja be, és beállítja a $Tags tárolt címkéket.</span><span class="sxs-lookup"><span data-stu-id="fac40-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="fac40-118">2. példa: kulcs módosítása az összes címke törléséhez</span><span class="sxs-lookup"><span data-stu-id="fac40-118">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="fac40-119">Ez a parancs törli az összes címkét a ITSoftware nevű kulcs adott verziójához.</span><span class="sxs-lookup"><span data-stu-id="fac40-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="fac40-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fac40-120">PARAMETERS</span></span>

### <span data-ttu-id="fac40-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fac40-121">-DefaultProfile</span></span>
<span data-ttu-id="fac40-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fac40-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fac40-123">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="fac40-123">-Enable</span></span>
<span data-ttu-id="fac40-124">Itt adhatja meg, hogy engedélyezi vagy letiltja-e a billentyűt.</span><span class="sxs-lookup"><span data-stu-id="fac40-124">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="fac40-125">A $True értéke lehetővé teszi a kulcs használatát.</span><span class="sxs-lookup"><span data-stu-id="fac40-125">A value of $True enables the key.</span></span> <span data-ttu-id="fac40-126">A $False értéke letiltja a billentyűt.</span><span class="sxs-lookup"><span data-stu-id="fac40-126">A value of $False disables the key.</span></span> <span data-ttu-id="fac40-127">Ha nem adja meg ezt a paramétert, ez a parancsmag nem módosítja a kulcs állapotát.</span><span class="sxs-lookup"><span data-stu-id="fac40-127">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-128">-Lejár</span><span class="sxs-lookup"><span data-stu-id="fac40-128">-Expires</span></span>
<span data-ttu-id="fac40-129">A lejárati idő **datetime** objektumként való megadása a parancsmag által frissített kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="fac40-129">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="fac40-130">Ez a paraméter koordinált univerzális időpontot (UTC) használ.</span><span class="sxs-lookup"><span data-stu-id="fac40-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="fac40-131">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fac40-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="fac40-132">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="fac40-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fac40-133">-InputObject</span></span>
<span data-ttu-id="fac40-134">Fő objektum</span><span class="sxs-lookup"><span data-stu-id="fac40-134">Key object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="fac40-135">-KeyOps</span></span>
<span data-ttu-id="fac40-136">Megadja azokat a műveleteket, amelyeket a parancsmag által hozzáadott kulccsal végezhet el.</span><span class="sxs-lookup"><span data-stu-id="fac40-136">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="fac40-137">Ha nem adja meg ezt a paramétert, akkor az összes művelet elvégezhető.</span><span class="sxs-lookup"><span data-stu-id="fac40-137">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="fac40-138">A paraméter elfogadható értékei a JSON webkulcs specifikációja által meghatározott főbb műveletek vesszővel elválasztott listája.</span><span class="sxs-lookup"><span data-stu-id="fac40-138">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="fac40-139">Ezek az értékek (kis-és nagybetűk):</span><span class="sxs-lookup"><span data-stu-id="fac40-139">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="fac40-140">beavatkozik</span><span class="sxs-lookup"><span data-stu-id="fac40-140">encrypt</span></span>
- <span data-ttu-id="fac40-141">visszafejtése</span><span class="sxs-lookup"><span data-stu-id="fac40-141">decrypt</span></span>
- <span data-ttu-id="fac40-142">wrap</span><span class="sxs-lookup"><span data-stu-id="fac40-142">wrap</span></span>
- <span data-ttu-id="fac40-143">tördelésének megszüntetéséhez</span><span class="sxs-lookup"><span data-stu-id="fac40-143">unwrap</span></span>
- <span data-ttu-id="fac40-144">jel</span><span class="sxs-lookup"><span data-stu-id="fac40-144">sign</span></span>
- <span data-ttu-id="fac40-145">Ellenőrizze</span><span class="sxs-lookup"><span data-stu-id="fac40-145">verify</span></span>
- <span data-ttu-id="fac40-146">hát</span><span class="sxs-lookup"><span data-stu-id="fac40-146">backup</span></span>
- <span data-ttu-id="fac40-147">visszaállítása</span><span class="sxs-lookup"><span data-stu-id="fac40-147">restore</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fac40-148">-Name</span></span>
<span data-ttu-id="fac40-149">A frissítendő kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fac40-149">Specifies the name of the key to update.</span></span> <span data-ttu-id="fac40-150">Ez a parancsmag a kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="fac40-150">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-151">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="fac40-151">-NotBefore</span></span>
<span data-ttu-id="fac40-152">Itt adhatja meg az időt **datetime** objektumként, amely előtt a kulcs nem használható.</span><span class="sxs-lookup"><span data-stu-id="fac40-152">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="fac40-153">Ez a paraméter az UTC-t használja.</span><span class="sxs-lookup"><span data-stu-id="fac40-153">This parameter uses UTC.</span></span>
<span data-ttu-id="fac40-154">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fac40-154">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fac40-155">-PassThru</span></span>
<span data-ttu-id="fac40-156">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="fac40-156">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fac40-157">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fac40-157">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-158">-Címke</span><span class="sxs-lookup"><span data-stu-id="fac40-158">-Tag</span></span>
<span data-ttu-id="fac40-159">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="fac40-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fac40-160">Példa:</span><span class="sxs-lookup"><span data-stu-id="fac40-160">For example:</span></span>

<span data-ttu-id="fac40-161">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="fac40-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-162">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fac40-162">-VaultName</span></span>
<span data-ttu-id="fac40-163">Annak a kulcsnak a nevét adja meg, amelyben ez a parancsmag módosítja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="fac40-163">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="fac40-164">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="fac40-164">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-165">-Verzió</span><span class="sxs-lookup"><span data-stu-id="fac40-165">-Version</span></span>
<span data-ttu-id="fac40-166">A kulcs verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fac40-166">Specifies the key version.</span></span>
<span data-ttu-id="fac40-167">Ez a parancsmag a kulcs teljes tartománynevét, az aktuálisan kijelölt környezetet, a kulcs nevét és a kulcs verziószámát építi fel.</span><span class="sxs-lookup"><span data-stu-id="fac40-167">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fac40-168">-Confirm</span></span>
<span data-ttu-id="fac40-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fac40-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fac40-170">-WhatIf</span></span>
<span data-ttu-id="fac40-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fac40-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fac40-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fac40-172">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac40-173">CommonParameters</span></span>
<span data-ttu-id="fac40-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fac40-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fac40-175">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fac40-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac40-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fac40-176">INPUTS</span></span>

### <span data-ttu-id="fac40-177">Nincs</span><span class="sxs-lookup"><span data-stu-id="fac40-177">None</span></span>
<span data-ttu-id="fac40-178">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fac40-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fac40-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fac40-179">OUTPUTS</span></span>

### <span data-ttu-id="fac40-180">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="fac40-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="fac40-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fac40-181">NOTES</span></span>

## <span data-ttu-id="fac40-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fac40-182">RELATED LINKS</span></span>

[<span data-ttu-id="fac40-183">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fac40-183">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="fac40-184">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fac40-184">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="fac40-185">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fac40-185">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
