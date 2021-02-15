---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: de8e542079cdeebdb6513c8e0febf8cfe0952889
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152634"
---
# <span data-ttu-id="0bb64-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0bb64-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="0bb64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bb64-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb64-103">Frissíti egy kulcskulcs attribútumát egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="0bb64-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="0bb64-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0bb64-104">SYNTAX</span></span>

### <span data-ttu-id="0bb64-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0bb64-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bb64-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="0bb64-106">HsmInteractive</span></span>
```
Update-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bb64-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="0bb64-107">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bb64-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0bb64-108">DESCRIPTION</span></span>
<span data-ttu-id="0bb64-109">Az **Update-AzKeyVaultKey** parancsmag frissíti egy kulcs szerkeszthető attribútumát egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="0bb64-109">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="0bb64-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0bb64-110">EXAMPLES</span></span>

### <span data-ttu-id="0bb64-111">1. példa: Kulcs módosítása annak engedélyezéséhez, valamint a lejárati dátum és a címkék beállítása</span><span class="sxs-lookup"><span data-stu-id="0bb64-111">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
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

<span data-ttu-id="0bb64-112">Az első parancs a **Get-Date** parancsmag használatával hoz létre **DateTime-objektumot.**</span><span class="sxs-lookup"><span data-stu-id="0bb64-112">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0bb64-113">Ez az objektum a jövőben két évet ad meg.</span><span class="sxs-lookup"><span data-stu-id="0bb64-113">That object specifies a time two years in the future.</span></span> <span data-ttu-id="0bb64-114">A parancs ezt a dátumot a $Expires tárolja.</span><span class="sxs-lookup"><span data-stu-id="0bb64-114">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="0bb64-115">További információért írja be a `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0bb64-115">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="0bb64-116">A második parancs létrehoz egy változót a nagy súlyosságú és könyvelési címkeértékek tárolására.</span><span class="sxs-lookup"><span data-stu-id="0bb64-116">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="0bb64-117">Az utolsó parancs módosítja az ITSoftware nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="0bb64-117">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="0bb64-118">A parancs engedélyezi a kulcsot, beállítja a lejárati idejét a $Expires, és beállítja a $Tags.</span><span class="sxs-lookup"><span data-stu-id="0bb64-118">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="0bb64-119">2. példa: Kulcs módosítása az összes címke törléséhez</span><span class="sxs-lookup"><span data-stu-id="0bb64-119">Example 2: Modify a key to delete all tags</span></span>
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

<span data-ttu-id="0bb64-120">Ez a parancs törli az ITSoftware nevű kulcs adott verziójának összes címkéét.</span><span class="sxs-lookup"><span data-stu-id="0bb64-120">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="0bb64-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bb64-121">PARAMETERS</span></span>

### <span data-ttu-id="0bb64-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb64-122">-DefaultProfile</span></span>
<span data-ttu-id="0bb64-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0bb64-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bb64-124">-Enable</span><span class="sxs-lookup"><span data-stu-id="0bb64-124">-Enable</span></span>
<span data-ttu-id="0bb64-125">Az igaz érték engedélyezi a kulcsot és a hamis értéket, letiltja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="0bb64-125">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="0bb64-126">Ha nincs megadva, a meglévő engedélyezett/letiltott állapot változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="0bb64-126">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="0bb64-127">-Lejár</span><span class="sxs-lookup"><span data-stu-id="0bb64-127">-Expires</span></span>
<span data-ttu-id="0bb64-128">A kulcs lejárati ideje az UTC-ben.</span><span class="sxs-lookup"><span data-stu-id="0bb64-128">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="0bb64-129">Ha nincs megadva, a kulcs meglévő lejárati ideje változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="0bb64-129">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="0bb64-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="0bb64-130">-HsmName</span></span>
<span data-ttu-id="0bb64-131">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="0bb64-131">HSM name.</span></span> <span data-ttu-id="0bb64-132">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="0bb64-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb64-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bb64-133">-InputObject</span></span>
<span data-ttu-id="0bb64-134">Kulcsobjektum</span><span class="sxs-lookup"><span data-stu-id="0bb64-134">Key object</span></span>

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

### <span data-ttu-id="0bb64-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="0bb64-135">-KeyOps</span></span>
<span data-ttu-id="0bb64-136">A billentyűvel elvégezhető műveletek.</span><span class="sxs-lookup"><span data-stu-id="0bb64-136">The operations that can be performed with the key.</span></span>
<span data-ttu-id="0bb64-137">Ha nincs megadva, a kulcs meglévő főbb műveletei változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="0bb64-137">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="0bb64-138">-Name</span><span class="sxs-lookup"><span data-stu-id="0bb64-138">-Name</span></span>
<span data-ttu-id="0bb64-139">Kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="0bb64-139">Key name.</span></span>
<span data-ttu-id="0bb64-140">A parancsmag a tárolónévből (jelenleg kijelölt környezetből és kulcsnévből) egy kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="0bb64-140">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb64-141">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="0bb64-141">-NotBefore</span></span>
<span data-ttu-id="0bb64-142">Az a UTC-idő, amely előtt a kulcs nem használható.</span><span class="sxs-lookup"><span data-stu-id="0bb64-142">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="0bb64-143">Ha nincs megadva, a kulcs meglévő NotBefore attribútuma változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="0bb64-143">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="0bb64-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bb64-144">-PassThru</span></span>
<span data-ttu-id="0bb64-145">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="0bb64-145">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0bb64-146">Ha ez a kapcsoló meg van adva, a frissített kulcskötegobjektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="0bb64-146">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="0bb64-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="0bb64-147">-Tag</span></span>
<span data-ttu-id="0bb64-148">A hashtable a kulcscímkéket jelöli.</span><span class="sxs-lookup"><span data-stu-id="0bb64-148">A hashtable represents key tags.</span></span>
<span data-ttu-id="0bb64-149">Ha nincs megadva, a kulcs meglévő címkéi változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="0bb64-149">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="0bb64-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0bb64-150">-VaultName</span></span>
<span data-ttu-id="0bb64-151">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="0bb64-151">Vault name.</span></span>
<span data-ttu-id="0bb64-152">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="0bb64-152">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="0bb64-153">-Verzió</span><span class="sxs-lookup"><span data-stu-id="0bb64-153">-Version</span></span>
<span data-ttu-id="0bb64-154">Főverzió.</span><span class="sxs-lookup"><span data-stu-id="0bb64-154">Key version.</span></span>
<span data-ttu-id="0bb64-155">A parancsmag a tárolónévből (jelenleg kijelölt környezetből, kulcsnévből és kulcsverzióból) egy kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="0bb64-155">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="0bb64-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0bb64-156">-Confirm</span></span>
<span data-ttu-id="0bb64-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0bb64-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bb64-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bb64-158">-WhatIf</span></span>
<span data-ttu-id="0bb64-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0bb64-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bb64-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0bb64-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bb64-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb64-161">CommonParameters</span></span>
<span data-ttu-id="0bb64-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bb64-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb64-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bb64-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb64-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0bb64-164">INPUTS</span></span>

### <span data-ttu-id="0bb64-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0bb64-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="0bb64-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bb64-166">OUTPUTS</span></span>

### <span data-ttu-id="0bb64-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0bb64-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="0bb64-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0bb64-168">NOTES</span></span>

## <span data-ttu-id="0bb64-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0bb64-169">RELATED LINKS</span></span>
