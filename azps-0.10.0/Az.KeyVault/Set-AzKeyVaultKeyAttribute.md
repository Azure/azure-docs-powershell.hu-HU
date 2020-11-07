---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultKeyAttribute.md
ms.openlocfilehash: df861a5efa87126b5eac1657a2b33b6fbae2110b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843850"
---
# <span data-ttu-id="818c2-101">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="818c2-101">Set-AzKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="818c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="818c2-102">SYNOPSIS</span></span>
<span data-ttu-id="818c2-103">Frissíti a kulcsok attribútumait egy kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="818c2-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="818c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="818c2-104">SYNTAX</span></span>

```
Set-AzKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="818c2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="818c2-105">DESCRIPTION</span></span>
<span data-ttu-id="818c2-106">A **set-AzKeyVaultKeyAttribute** parancsmag a kulcsok szerkeszthető attribútumait frissíti a kulcs boltozatakor.</span><span class="sxs-lookup"><span data-stu-id="818c2-106">The **Set-AzKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="818c2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="818c2-107">EXAMPLES</span></span>

### <span data-ttu-id="818c2-108">1. példa: kulcs módosítása az engedélyezéshez, és a lejárat dátuma és a címkék beállítása</span><span class="sxs-lookup"><span data-stu-id="818c2-108">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="818c2-109">Az első parancs egy **datetime** típusú objektumot hoz létre a **Get-Date** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="818c2-109">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="818c2-110">Ez az objektum két év múlva adja meg a jövőbeli időpontot.</span><span class="sxs-lookup"><span data-stu-id="818c2-110">That object specifies a time two years in the future.</span></span> <span data-ttu-id="818c2-111">A parancs a $Expires változóban tárolja a dátumot.</span><span class="sxs-lookup"><span data-stu-id="818c2-111">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="818c2-112">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="818c2-112">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="818c2-113">A második parancs létrehoz egy változót, amely a nagy súlyosságú és a számviteli adatok címkézését tárolja.</span><span class="sxs-lookup"><span data-stu-id="818c2-113">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="818c2-114">A végleges parancs módosítja a ITSoftware nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="818c2-114">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="818c2-115">A parancs engedélyezi a kulcsot, a lejárati időt az $Expires tárolt időpontra állítja be, és beállítja a $Tags tárolt címkéket.</span><span class="sxs-lookup"><span data-stu-id="818c2-115">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="818c2-116">2. példa: kulcs módosítása az összes címke törléséhez</span><span class="sxs-lookup"><span data-stu-id="818c2-116">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="818c2-117">Ez a parancs törli az összes címkét a ITSoftware nevű kulcs adott verziójához.</span><span class="sxs-lookup"><span data-stu-id="818c2-117">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="818c2-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="818c2-118">PARAMETERS</span></span>

### <span data-ttu-id="818c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="818c2-119">-DefaultProfile</span></span>
<span data-ttu-id="818c2-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="818c2-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="818c2-121">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="818c2-121">-Enable</span></span>
<span data-ttu-id="818c2-122">Itt adhatja meg, hogy engedélyezi vagy letiltja-e a billentyűt.</span><span class="sxs-lookup"><span data-stu-id="818c2-122">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="818c2-123">A $True értéke lehetővé teszi a kulcs használatát.</span><span class="sxs-lookup"><span data-stu-id="818c2-123">A value of $True enables the key.</span></span> <span data-ttu-id="818c2-124">A $False értéke letiltja a billentyűt.</span><span class="sxs-lookup"><span data-stu-id="818c2-124">A value of $False disables the key.</span></span> <span data-ttu-id="818c2-125">Ha nem adja meg ezt a paramétert, ez a parancsmag nem módosítja a kulcs állapotát.</span><span class="sxs-lookup"><span data-stu-id="818c2-125">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="818c2-126">-Lejár</span><span class="sxs-lookup"><span data-stu-id="818c2-126">-Expires</span></span>
<span data-ttu-id="818c2-127">A lejárati idő **datetime** objektumként való megadása a parancsmag által frissített kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="818c2-127">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="818c2-128">Ez a paraméter koordinált univerzális időpontot (UTC) használ.</span><span class="sxs-lookup"><span data-stu-id="818c2-128">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="818c2-129">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="818c2-129">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="818c2-130">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="818c2-130">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="818c2-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="818c2-131">-KeyOps</span></span>
<span data-ttu-id="818c2-132">Megadja azokat a műveleteket, amelyeket a parancsmag által hozzáadott kulccsal végezhet el.</span><span class="sxs-lookup"><span data-stu-id="818c2-132">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="818c2-133">Ha nem adja meg ezt a paramétert, akkor az összes művelet elvégezhető.</span><span class="sxs-lookup"><span data-stu-id="818c2-133">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="818c2-134">A paraméter elfogadható értékei a JSON webkulcs specifikációja által meghatározott főbb műveletek vesszővel elválasztott listája.</span><span class="sxs-lookup"><span data-stu-id="818c2-134">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="818c2-135">Ezek az értékek (kis-és nagybetűk):</span><span class="sxs-lookup"><span data-stu-id="818c2-135">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="818c2-136">beavatkozik</span><span class="sxs-lookup"><span data-stu-id="818c2-136">encrypt</span></span>
- <span data-ttu-id="818c2-137">visszafejtése</span><span class="sxs-lookup"><span data-stu-id="818c2-137">decrypt</span></span>
- <span data-ttu-id="818c2-138">wrap</span><span class="sxs-lookup"><span data-stu-id="818c2-138">wrap</span></span>
- <span data-ttu-id="818c2-139">tördelésének megszüntetéséhez</span><span class="sxs-lookup"><span data-stu-id="818c2-139">unwrap</span></span>
- <span data-ttu-id="818c2-140">jel</span><span class="sxs-lookup"><span data-stu-id="818c2-140">sign</span></span>
- <span data-ttu-id="818c2-141">Ellenőrizze</span><span class="sxs-lookup"><span data-stu-id="818c2-141">verify</span></span>
- <span data-ttu-id="818c2-142">hát</span><span class="sxs-lookup"><span data-stu-id="818c2-142">backup</span></span>
- <span data-ttu-id="818c2-143">visszaállítása</span><span class="sxs-lookup"><span data-stu-id="818c2-143">restore</span></span>

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

### <span data-ttu-id="818c2-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="818c2-144">-Name</span></span>
<span data-ttu-id="818c2-145">A frissítendő kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="818c2-145">Specifies the name of the key to update.</span></span> <span data-ttu-id="818c2-146">Ez a parancsmag a kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="818c2-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="818c2-147">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="818c2-147">-NotBefore</span></span>
<span data-ttu-id="818c2-148">Itt adhatja meg az időt **datetime** objektumként, amely előtt a kulcs nem használható.</span><span class="sxs-lookup"><span data-stu-id="818c2-148">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="818c2-149">Ez a paraméter az UTC-t használja.</span><span class="sxs-lookup"><span data-stu-id="818c2-149">This parameter uses UTC.</span></span>
<span data-ttu-id="818c2-150">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="818c2-150">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="818c2-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="818c2-151">-PassThru</span></span>
<span data-ttu-id="818c2-152">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="818c2-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="818c2-153">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="818c2-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="818c2-154">-Címke</span><span class="sxs-lookup"><span data-stu-id="818c2-154">-Tag</span></span>
<span data-ttu-id="818c2-155">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="818c2-155">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="818c2-156">Példa:</span><span class="sxs-lookup"><span data-stu-id="818c2-156">For example:</span></span>

<span data-ttu-id="818c2-157">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="818c2-157">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="818c2-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="818c2-158">-VaultName</span></span>
<span data-ttu-id="818c2-159">Annak a kulcsnak a nevét adja meg, amelyben ez a parancsmag módosítja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="818c2-159">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="818c2-160">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="818c2-160">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="818c2-161">-Verzió</span><span class="sxs-lookup"><span data-stu-id="818c2-161">-Version</span></span>
<span data-ttu-id="818c2-162">A kulcs verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="818c2-162">Specifies the key version.</span></span>
<span data-ttu-id="818c2-163">Ez a parancsmag a kulcs teljes tartománynevét, az aktuálisan kijelölt környezetet, a kulcs nevét és a kulcs verziószámát építi fel.</span><span class="sxs-lookup"><span data-stu-id="818c2-163">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="818c2-164">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="818c2-164">-Confirm</span></span>
<span data-ttu-id="818c2-165">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="818c2-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="818c2-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="818c2-166">-WhatIf</span></span>
<span data-ttu-id="818c2-167">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="818c2-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="818c2-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="818c2-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="818c2-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="818c2-169">CommonParameters</span></span>
<span data-ttu-id="818c2-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="818c2-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="818c2-171">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="818c2-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="818c2-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="818c2-172">INPUTS</span></span>

### <span data-ttu-id="818c2-173">Nincs</span><span class="sxs-lookup"><span data-stu-id="818c2-173">None</span></span>
<span data-ttu-id="818c2-174">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="818c2-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="818c2-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="818c2-175">OUTPUTS</span></span>

### <span data-ttu-id="818c2-176">Microsoft. Azure. Command. Vault. models. Bundle</span><span class="sxs-lookup"><span data-stu-id="818c2-176">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="818c2-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="818c2-177">NOTES</span></span>

## <span data-ttu-id="818c2-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="818c2-178">RELATED LINKS</span></span>

[<span data-ttu-id="818c2-179">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="818c2-179">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="818c2-180">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="818c2-180">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="818c2-181">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="818c2-181">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)
