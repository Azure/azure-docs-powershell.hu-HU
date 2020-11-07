---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: fb27aead0c45270a04c7a9f7f0c97eaa9d83cc08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666127"
---
# <span data-ttu-id="0d95c-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0d95c-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="0d95c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d95c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d95c-103">Frissíti a kulcsok attribútumait egy kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="0d95c-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="0d95c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d95c-104">SYNTAX</span></span>

### <span data-ttu-id="0d95c-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d95c-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d95c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0d95c-106">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d95c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d95c-107">DESCRIPTION</span></span>
<span data-ttu-id="0d95c-108">Az **Update-AzKeyVaultKey** parancsmag a kulcsok szerkeszthető attribútumait frissíti a kulcs boltozatakor.</span><span class="sxs-lookup"><span data-stu-id="0d95c-108">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="0d95c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0d95c-109">EXAMPLES</span></span>

### <span data-ttu-id="0d95c-110">1. példa: kulcs módosítása az engedélyezéshez, és a lejárat dátuma és a címkék beállítása</span><span class="sxs-lookup"><span data-stu-id="0d95c-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 7:59:02 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="0d95c-111">Az első parancs egy **datetime** típusú objektumot hoz létre a **Get-Date** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="0d95c-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0d95c-112">Ez az objektum két év múlva adja meg a jövőbeli időpontot.</span><span class="sxs-lookup"><span data-stu-id="0d95c-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="0d95c-113">A parancs a $Expires változóban tárolja a dátumot.</span><span class="sxs-lookup"><span data-stu-id="0d95c-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="0d95c-114">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0d95c-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="0d95c-115">A második parancs létrehoz egy változót, amely a nagy súlyosságú és a számviteli adatok címkézését tárolja.</span><span class="sxs-lookup"><span data-stu-id="0d95c-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="0d95c-116">A végleges parancs módosítja a ITSoftware nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="0d95c-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="0d95c-117">A parancs engedélyezi a kulcsot, a lejárati időt az $Expires tárolt időpontra állítja be, és beállítja a $Tags tárolt címkéket.</span><span class="sxs-lookup"><span data-stu-id="0d95c-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="0d95c-118">2. példa: kulcs módosítása az összes címke törléséhez</span><span class="sxs-lookup"><span data-stu-id="0d95c-118">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 8:00:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="0d95c-119">Ez a parancs törli az összes címkét a ITSoftware nevű kulcs adott verziójához.</span><span class="sxs-lookup"><span data-stu-id="0d95c-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="0d95c-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d95c-120">PARAMETERS</span></span>

### <span data-ttu-id="0d95c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d95c-121">-DefaultProfile</span></span>
<span data-ttu-id="0d95c-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d95c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d95c-123">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="0d95c-123">-Enable</span></span>
<span data-ttu-id="0d95c-124">Az igaz érték lehetővé teszi a kulcs és a hamis érték kiírását.</span><span class="sxs-lookup"><span data-stu-id="0d95c-124">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="0d95c-125">Ha nincs megadva, a meglévő engedélyezett/letiltott állapot továbbra sem változik.</span><span class="sxs-lookup"><span data-stu-id="0d95c-125">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="0d95c-126">-Lejár</span><span class="sxs-lookup"><span data-stu-id="0d95c-126">-Expires</span></span>
<span data-ttu-id="0d95c-127">Egy kulcs lejárati ideje az UTC időpontjában.</span><span class="sxs-lookup"><span data-stu-id="0d95c-127">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="0d95c-128">Ha nincs megadva, a kulcs meglévő lejárati ideje változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="0d95c-128">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="0d95c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d95c-129">-InputObject</span></span>
<span data-ttu-id="0d95c-130">Fő objektum</span><span class="sxs-lookup"><span data-stu-id="0d95c-130">Key object</span></span>

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

### <span data-ttu-id="0d95c-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="0d95c-131">-KeyOps</span></span>
<span data-ttu-id="0d95c-132">A kulccsal elvégezhető műveletek.</span><span class="sxs-lookup"><span data-stu-id="0d95c-132">The operations that can be performed with the key.</span></span>
<span data-ttu-id="0d95c-133">Ha nem adja meg, a kulcs meglévő fő műveletei változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="0d95c-133">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="0d95c-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0d95c-134">-Name</span></span>
<span data-ttu-id="0d95c-135">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="0d95c-135">Key name.</span></span>
<span data-ttu-id="0d95c-136">Parancsmag: a kulcs FQDN-je a boltozat neve, az aktuálisan kijelölt környezet és a kulcs neve alapján.</span><span class="sxs-lookup"><span data-stu-id="0d95c-136">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="0d95c-137">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="0d95c-137">-NotBefore</span></span>
<span data-ttu-id="0d95c-138">A nem használható billentyűt tartalmazó UTC-idő.</span><span class="sxs-lookup"><span data-stu-id="0d95c-138">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="0d95c-139">Ha nincs megadva, a kulcs meglévő NotBefore attribútuma változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="0d95c-139">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="0d95c-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d95c-140">-PassThru</span></span>
<span data-ttu-id="0d95c-141">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="0d95c-141">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0d95c-142">Ha ez a kapcsoló van megadva, a frissített kulcs köteg objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0d95c-142">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="0d95c-143">-Címke</span><span class="sxs-lookup"><span data-stu-id="0d95c-143">-Tag</span></span>
<span data-ttu-id="0d95c-144">A Hashtable A kulcsok címkéit képviselik.</span><span class="sxs-lookup"><span data-stu-id="0d95c-144">A hashtable represents key tags.</span></span>
<span data-ttu-id="0d95c-145">Ha nem adja meg, akkor a billentyű meglévő címkéi változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="0d95c-145">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="0d95c-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0d95c-146">-VaultName</span></span>
<span data-ttu-id="0d95c-147">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="0d95c-147">Vault name.</span></span>
<span data-ttu-id="0d95c-148">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="0d95c-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="0d95c-149">-Verzió</span><span class="sxs-lookup"><span data-stu-id="0d95c-149">-Version</span></span>
<span data-ttu-id="0d95c-150">Fő verzió.</span><span class="sxs-lookup"><span data-stu-id="0d95c-150">Key version.</span></span>
<span data-ttu-id="0d95c-151">Parancsmag: a kulcs FQDN-je a boltozat neve, az aktuálisan kijelölt környezet, a kulcs neve és a kulcs verziója alapján.</span><span class="sxs-lookup"><span data-stu-id="0d95c-151">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="0d95c-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0d95c-152">-Confirm</span></span>
<span data-ttu-id="0d95c-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0d95c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d95c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d95c-154">-WhatIf</span></span>
<span data-ttu-id="0d95c-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0d95c-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d95c-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0d95c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d95c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d95c-157">CommonParameters</span></span>
<span data-ttu-id="0d95c-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d95c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d95c-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d95c-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d95c-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d95c-160">INPUTS</span></span>

### <span data-ttu-id="0d95c-161">Microsoft. Azure. Command. PSKeyVaultKeyIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="0d95c-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="0d95c-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d95c-162">OUTPUTS</span></span>

### <span data-ttu-id="0d95c-163">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="0d95c-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="0d95c-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d95c-164">NOTES</span></span>

## <span data-ttu-id="0d95c-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d95c-165">RELATED LINKS</span></span>
