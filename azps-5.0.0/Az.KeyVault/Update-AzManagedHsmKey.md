---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
ms.openlocfilehash: 79d01f96fe776432f650d827b16ba83f48b84ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194748"
---
# <span data-ttu-id="f0ad3-101">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f0ad3-101">Update-AzManagedHsmKey</span></span>

## <span data-ttu-id="f0ad3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ad3-103">Frissíti a felügyelt HSM-kulcsok attribútumait.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-103">Updates the attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="f0ad3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0ad3-104">SYNTAX</span></span>

### <span data-ttu-id="f0ad3-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f0ad3-105">Default (Default)</span></span>
```
Update-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0ad3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f0ad3-106">InputObject</span></span>
```
Update-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0ad3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0ad3-107">DESCRIPTION</span></span>
<span data-ttu-id="f0ad3-108">Az **Update-AzManagedHsmKey** parancsmag frissíti a felügyelt HSM-kulcsok szerkeszthető attribútumait.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-108">The **Update-AzManagedHsmKey** cmdlet updates the editable attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="f0ad3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f0ad3-109">EXAMPLES</span></span>

### <span data-ttu-id="f0ad3-110">1. példa: kulcs módosítása az engedélyezéshez, és a lejárat dátuma és a címkék beállítása</span><span class="sxs-lookup"><span data-stu-id="f0ad3-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzManagedHsmKey -HsmName testmhsm -Name testkey001 -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 49b74a39dab605bd336628dc094dc31b
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/49b74a39dab605bd336628dc094dc31b
Enabled        : True
Expires        : 10/14/2022 9:46:55 AM
Not Before     :
Created        : 10/14/2020 3:39:16 AM
Updated        : 10/14/2020 9:47:06 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="f0ad3-111">Az első parancs egy **datetime** típusú objektumot hoz létre a **Get-Date** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="f0ad3-112">Ez az objektum két év múlva adja meg a jövőbeli időpontot.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="f0ad3-113">A parancs a $Expires változóban tárolja a dátumot.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="f0ad3-114">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f0ad3-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="f0ad3-115">A második parancs létrehoz egy változót, amely a nagy súlyosságú és a számviteli adatok címkézését tárolja.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="f0ad3-116">A végleges parancs módosítja a testkey001 nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-116">The final command modifies a key named testkey001.</span></span> <span data-ttu-id="f0ad3-117">A parancs engedélyezi a kulcsot, a lejárati időt az $Expires tárolt időpontra állítja be, és beállítja a $Tags tárolt címkéket.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

## <span data-ttu-id="f0ad3-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0ad3-118">PARAMETERS</span></span>

### <span data-ttu-id="f0ad3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ad3-119">-DefaultProfile</span></span>
<span data-ttu-id="f0ad3-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0ad3-121">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="f0ad3-121">-Enable</span></span>
<span data-ttu-id="f0ad3-122">Az igaz érték lehetővé teszi a kulcs és a hamis érték kiírását.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-122">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="f0ad3-123">Ha nincs megadva, a meglévő engedélyezett/letiltott állapot továbbra sem változik.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-123">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ad3-124">-Lejár</span><span class="sxs-lookup"><span data-stu-id="f0ad3-124">-Expires</span></span>
<span data-ttu-id="f0ad3-125">Egy kulcs lejárati ideje az UTC időpontjában.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-125">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="f0ad3-126">Ha nincs megadva, a kulcs meglévő lejárati ideje változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-126">If not specified, the existing expiration time of the key remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ad3-127">-HsmName</span><span class="sxs-lookup"><span data-stu-id="f0ad3-127">-HsmName</span></span>
<span data-ttu-id="f0ad3-128">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-128">HSM name.</span></span> <span data-ttu-id="f0ad3-129">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-129">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ad3-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0ad3-130">-InputObject</span></span>
<span data-ttu-id="f0ad3-131">Fő objektum</span><span class="sxs-lookup"><span data-stu-id="f0ad3-131">Key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ad3-132">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="f0ad3-132">-KeyOps</span></span>
<span data-ttu-id="f0ad3-133">A kulccsal elvégezhető műveletek.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-133">The operations that can be performed with the key.</span></span>
<span data-ttu-id="f0ad3-134">Ha nem adja meg, a kulcs meglévő fő műveletei változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-134">If not specified, the existing key operations of the key remain unchanged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ad3-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f0ad3-135">-Name</span></span>
<span data-ttu-id="f0ad3-136">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-136">Key name.</span></span>
<span data-ttu-id="f0ad3-137">Parancsmag: a felügyelt HSM-név, az aktuálisan kijelölt környezet és a kulcsnév alapján egy kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-137">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ad3-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="f0ad3-138">-NotBefore</span></span>
<span data-ttu-id="f0ad3-139">A nem használható billentyűt tartalmazó UTC-idő.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-139">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="f0ad3-140">Ha nincs megadva, a kulcs meglévő NotBefore attribútuma változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-140">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ad3-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0ad3-141">-PassThru</span></span>
<span data-ttu-id="f0ad3-142">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f0ad3-143">Ha ez a kapcsoló van megadva, a frissített kulcs köteg objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-143">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="f0ad3-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="f0ad3-144">-Tag</span></span>
<span data-ttu-id="f0ad3-145">A Hashtable A kulcsok címkéit képviselik.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-145">A hashtable represents key tags.</span></span>
<span data-ttu-id="f0ad3-146">Ha nem adja meg, akkor a billentyű meglévő címkéi változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-146">If not specified, the existings tags of the key remain unchanged.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ad3-147">-Verzió</span><span class="sxs-lookup"><span data-stu-id="f0ad3-147">-Version</span></span>
<span data-ttu-id="f0ad3-148">Fő verzió.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-148">Key version.</span></span>
<span data-ttu-id="f0ad3-149">Parancsmag: a felügyelt HSM-név, az aktuálisan kijelölt környezet, a kulcs neve és a kulcs verziója alapján egy kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-149">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ad3-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f0ad3-150">-Confirm</span></span>
<span data-ttu-id="f0ad3-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0ad3-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ad3-152">-WhatIf</span></span>
<span data-ttu-id="f0ad3-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0ad3-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0ad3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ad3-155">CommonParameters</span></span>
<span data-ttu-id="f0ad3-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0ad3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ad3-157">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ad3-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0ad3-158">INPUTS</span></span>

### <span data-ttu-id="f0ad3-159">Microsoft. Azure. Command. PSKeyVaultKeyIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="f0ad3-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0ad3-160">OUTPUTS</span></span>

### <span data-ttu-id="f0ad3-161">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="f0ad3-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0ad3-162">NOTES</span></span>

## <span data-ttu-id="f0ad3-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0ad3-163">RELATED LINKS</span></span>

[<span data-ttu-id="f0ad3-164">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f0ad3-164">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="f0ad3-165">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f0ad3-165">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="f0ad3-166">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f0ad3-166">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="f0ad3-167">Visszavonás – AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="f0ad3-167">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="f0ad3-168">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f0ad3-168">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="f0ad3-169">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f0ad3-169">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)