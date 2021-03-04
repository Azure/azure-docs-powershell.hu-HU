---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: 631cb05e15231bb4e695ad3047a7736177a785e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931098"
---
# <span data-ttu-id="9a7bd-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9a7bd-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="9a7bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a7bd-102">SYNOPSIS</span></span>
<span data-ttu-id="9a7bd-103">Frissíti egy kulcskulcs attribútumát egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="9a7bd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9a7bd-104">SYNTAX</span></span>

### <span data-ttu-id="9a7bd-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a7bd-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a7bd-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="9a7bd-106">HsmInteractive</span></span>
```
Update-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a7bd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9a7bd-107">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a7bd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9a7bd-108">DESCRIPTION</span></span>
<span data-ttu-id="9a7bd-109">Az **Update-AzKeyVaultKey** parancsmag frissíti egy kulcs kulcs szerkeszthető attribútumát egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-109">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="9a7bd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9a7bd-110">EXAMPLES</span></span>

### <span data-ttu-id="9a7bd-111">1. példa: Kulcs módosítása annak engedélyezéséhez, valamint a lejárati dátum és a címkék beállítása</span><span class="sxs-lookup"><span data-stu-id="9a7bd-111">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
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

<span data-ttu-id="9a7bd-112">Az első parancs a **Get-Date** parancsmag használatával hoz létre **DateTime-objektumot.**</span><span class="sxs-lookup"><span data-stu-id="9a7bd-112">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="9a7bd-113">Ez az objektum a jövőben két évet ad meg.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-113">That object specifies a time two years in the future.</span></span> <span data-ttu-id="9a7bd-114">A parancs ezt a dátumot a $Expires tárolja.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-114">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="9a7bd-115">További információért írja be a `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9a7bd-115">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="9a7bd-116">A második parancs létrehoz egy változót, amely a nagy súlyosságú és a Könyvelési címkeértékeket tárolja.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-116">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="9a7bd-117">Az utolsó parancs módosítja az ITSoftware nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-117">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="9a7bd-118">A parancs engedélyezi a kulcsot, beállítja a lejárati idejét a $Expires, és beállítja a $Tags.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-118">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="9a7bd-119">2. példa: Kulcs módosítása az összes címke törléséhez</span><span class="sxs-lookup"><span data-stu-id="9a7bd-119">Example 2: Modify a key to delete all tags</span></span>
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

<span data-ttu-id="9a7bd-120">Ez a parancs törli az ITSoftware nevű kulcs adott verziójának összes címkéét.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-120">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="9a7bd-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a7bd-121">PARAMETERS</span></span>

### <span data-ttu-id="9a7bd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a7bd-122">-DefaultProfile</span></span>
<span data-ttu-id="9a7bd-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a7bd-124">-Enable</span><span class="sxs-lookup"><span data-stu-id="9a7bd-124">-Enable</span></span>
<span data-ttu-id="9a7bd-125">Az igaz érték engedélyezi a kulcsot és a hamis értéket, letiltja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-125">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="9a7bd-126">Ha nincs megadva, a meglévő engedélyezett/letiltott állapot változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-126">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="9a7bd-127">-Lejár</span><span class="sxs-lookup"><span data-stu-id="9a7bd-127">-Expires</span></span>
<span data-ttu-id="9a7bd-128">A kulcs lejárati ideje az UTC-ben.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-128">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="9a7bd-129">Ha nincs megadva, a kulcs meglévő lejárati ideje változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-129">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="9a7bd-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="9a7bd-130">-HsmName</span></span>
<span data-ttu-id="9a7bd-131">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-131">HSM name.</span></span> <span data-ttu-id="9a7bd-132">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9a7bd-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a7bd-133">-InputObject</span></span>
<span data-ttu-id="9a7bd-134">Kulcsobjektum</span><span class="sxs-lookup"><span data-stu-id="9a7bd-134">Key object</span></span>

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

### <span data-ttu-id="9a7bd-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="9a7bd-135">-KeyOps</span></span>
<span data-ttu-id="9a7bd-136">A kulccsal elvégezhető műveletek.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-136">The operations that can be performed with the key.</span></span>
<span data-ttu-id="9a7bd-137">Ha nincs megadva, a kulcs meglévő kulcsműveletei változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-137">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="9a7bd-138">-Name</span><span class="sxs-lookup"><span data-stu-id="9a7bd-138">-Name</span></span>
<span data-ttu-id="9a7bd-139">Kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-139">Key name.</span></span>
<span data-ttu-id="9a7bd-140">A parancsmag a tárolónévből (jelenleg kijelölt környezetből és kulcsnévből) egy kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-140">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="9a7bd-141">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="9a7bd-141">-NotBefore</span></span>
<span data-ttu-id="9a7bd-142">Az a UTC-idő, amely előtt a kulcs nem használható.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-142">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="9a7bd-143">Ha nincs megadva, a kulcs meglévő NotBefore attribútuma változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-143">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="9a7bd-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a7bd-144">-PassThru</span></span>
<span data-ttu-id="9a7bd-145">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-145">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9a7bd-146">Ha ez a kapcsoló meg van adva, akkor a frissített kulcskötegobjektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-146">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="9a7bd-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="9a7bd-147">-Tag</span></span>
<span data-ttu-id="9a7bd-148">A hashtable a kulcscímkéket jelöli.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-148">A hashtable represents key tags.</span></span>
<span data-ttu-id="9a7bd-149">Ha nincs megadva, a kulcs meglévő címkéi változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-149">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="9a7bd-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9a7bd-150">-VaultName</span></span>
<span data-ttu-id="9a7bd-151">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-151">Vault name.</span></span>
<span data-ttu-id="9a7bd-152">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-152">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9a7bd-153">-Version</span><span class="sxs-lookup"><span data-stu-id="9a7bd-153">-Version</span></span>
<span data-ttu-id="9a7bd-154">Főverzió.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-154">Key version.</span></span>
<span data-ttu-id="9a7bd-155">A parancsmag a tárolónévből (jelenleg kijelölt környezetből, kulcsnévből és kulcsverzióból) egy kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-155">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="9a7bd-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a7bd-156">-Confirm</span></span>
<span data-ttu-id="9a7bd-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a7bd-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a7bd-158">-WhatIf</span></span>
<span data-ttu-id="9a7bd-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a7bd-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a7bd-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a7bd-161">CommonParameters</span></span>
<span data-ttu-id="9a7bd-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a7bd-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a7bd-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a7bd-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a7bd-164">INPUTS</span></span>

### <span data-ttu-id="9a7bd-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9a7bd-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="9a7bd-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a7bd-166">OUTPUTS</span></span>

### <span data-ttu-id="9a7bd-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9a7bd-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="9a7bd-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9a7bd-168">NOTES</span></span>

## <span data-ttu-id="9a7bd-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a7bd-169">RELATED LINKS</span></span>
