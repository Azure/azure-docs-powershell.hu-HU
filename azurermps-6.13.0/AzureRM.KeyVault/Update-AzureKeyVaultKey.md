---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultKey.md
ms.openlocfilehash: e9e2401ab96da63c3fe6b5978916b96f98db9f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496027"
---
# <span data-ttu-id="8be37-101">Update-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8be37-101">Update-AzureKeyVaultKey</span></span>

## <span data-ttu-id="8be37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8be37-102">SYNOPSIS</span></span>
<span data-ttu-id="8be37-103">Frissíti a kulcsok attribútumait egy kulcs boltozatában.</span><span class="sxs-lookup"><span data-stu-id="8be37-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8be37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8be37-104">SYNTAX</span></span>

### <span data-ttu-id="8be37-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8be37-105">Default (Default)</span></span>
```
Update-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8be37-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8be37-106">InputObject</span></span>
```
Update-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8be37-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8be37-107">DESCRIPTION</span></span>
<span data-ttu-id="8be37-108">Az **Update-AzureKeyVaultKey** parancsmag a kulcsok szerkeszthető attribútumait frissíti a kulcs boltozatakor.</span><span class="sxs-lookup"><span data-stu-id="8be37-108">The **Update-AzureKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="8be37-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8be37-109">EXAMPLES</span></span>

### <span data-ttu-id="8be37-110">1. példa: kulcs módosítása az engedélyezéshez, és a lejárat dátuma és a címkék beállítása</span><span class="sxs-lookup"><span data-stu-id="8be37-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

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

<span data-ttu-id="8be37-111">Az első parancs egy **datetime** típusú objektumot hoz létre a **Get-Date** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="8be37-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="8be37-112">Ez az objektum két év múlva adja meg a jövőbeli időpontot.</span><span class="sxs-lookup"><span data-stu-id="8be37-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="8be37-113">A parancs a $Expires változóban tárolja a dátumot.</span><span class="sxs-lookup"><span data-stu-id="8be37-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="8be37-114">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8be37-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="8be37-115">A második parancs létrehoz egy változót, amely a nagy súlyosságú és a számviteli adatok címkézését tárolja.</span><span class="sxs-lookup"><span data-stu-id="8be37-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="8be37-116">A végleges parancs módosítja a ITSoftware nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="8be37-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="8be37-117">A parancs engedélyezi a kulcsot, a lejárati időt az $Expires tárolt időpontra állítja be, és beállítja a $Tags tárolt címkéket.</span><span class="sxs-lookup"><span data-stu-id="8be37-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="8be37-118">2. példa: kulcs módosítása az összes címke törléséhez</span><span class="sxs-lookup"><span data-stu-id="8be37-118">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

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

<span data-ttu-id="8be37-119">Ez a parancs törli az összes címkét a ITSoftware nevű kulcs adott verziójához.</span><span class="sxs-lookup"><span data-stu-id="8be37-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="8be37-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8be37-120">PARAMETERS</span></span>

### <span data-ttu-id="8be37-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be37-121">-DefaultProfile</span></span>
<span data-ttu-id="8be37-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8be37-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8be37-123">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="8be37-123">-Enable</span></span>
<span data-ttu-id="8be37-124">Az igaz érték lehetővé teszi a kulcs és a hamis érték kiírását.</span><span class="sxs-lookup"><span data-stu-id="8be37-124">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="8be37-125">Ha nincs megadva, a meglévő engedélyezett/letiltott állapot továbbra sem változik.</span><span class="sxs-lookup"><span data-stu-id="8be37-125">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="8be37-126">-Lejár</span><span class="sxs-lookup"><span data-stu-id="8be37-126">-Expires</span></span>
<span data-ttu-id="8be37-127">Egy kulcs lejárati ideje az UTC időpontjában.</span><span class="sxs-lookup"><span data-stu-id="8be37-127">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="8be37-128">Ha nincs megadva, a kulcs meglévő lejárati ideje változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="8be37-128">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="8be37-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8be37-129">-InputObject</span></span>
<span data-ttu-id="8be37-130">Fő objektum</span><span class="sxs-lookup"><span data-stu-id="8be37-130">Key object</span></span>

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

### <span data-ttu-id="8be37-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="8be37-131">-KeyOps</span></span>
<span data-ttu-id="8be37-132">A kulccsal elvégezhető műveletek.</span><span class="sxs-lookup"><span data-stu-id="8be37-132">The operations that can be performed with the key.</span></span>
<span data-ttu-id="8be37-133">Ha nem adja meg, a kulcs meglévő fő műveletei változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="8be37-133">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="8be37-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8be37-134">-Name</span></span>
<span data-ttu-id="8be37-135">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="8be37-135">Key name.</span></span>
<span data-ttu-id="8be37-136">Parancsmag: a kulcs FQDN-je a boltozat neve, az aktuálisan kijelölt környezet és a kulcs neve alapján.</span><span class="sxs-lookup"><span data-stu-id="8be37-136">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="8be37-137">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="8be37-137">-NotBefore</span></span>
<span data-ttu-id="8be37-138">A nem használható billentyűt tartalmazó UTC-idő.</span><span class="sxs-lookup"><span data-stu-id="8be37-138">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="8be37-139">Ha nincs megadva, a kulcs meglévő NotBefore attribútuma változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="8be37-139">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="8be37-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8be37-140">-PassThru</span></span>
<span data-ttu-id="8be37-141">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="8be37-141">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8be37-142">Ha ez a kapcsoló van megadva, a frissített kulcs köteg objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8be37-142">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="8be37-143">-Címke</span><span class="sxs-lookup"><span data-stu-id="8be37-143">-Tag</span></span>
<span data-ttu-id="8be37-144">A Hashtable A kulcsok címkéit képviselik.</span><span class="sxs-lookup"><span data-stu-id="8be37-144">A hashtable represents key tags.</span></span>
<span data-ttu-id="8be37-145">Ha nem adja meg, akkor a billentyű meglévő címkéi változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="8be37-145">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="8be37-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8be37-146">-VaultName</span></span>
<span data-ttu-id="8be37-147">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="8be37-147">Vault name.</span></span>
<span data-ttu-id="8be37-148">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="8be37-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8be37-149">-Verzió</span><span class="sxs-lookup"><span data-stu-id="8be37-149">-Version</span></span>
<span data-ttu-id="8be37-150">Fő verzió.</span><span class="sxs-lookup"><span data-stu-id="8be37-150">Key version.</span></span>
<span data-ttu-id="8be37-151">Parancsmag: a kulcs FQDN-je a boltozat neve, az aktuálisan kijelölt környezet, a kulcs neve és a kulcs verziója alapján.</span><span class="sxs-lookup"><span data-stu-id="8be37-151">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="8be37-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8be37-152">-Confirm</span></span>
<span data-ttu-id="8be37-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8be37-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8be37-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8be37-154">-WhatIf</span></span>
<span data-ttu-id="8be37-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8be37-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8be37-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8be37-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8be37-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be37-157">CommonParameters</span></span>
<span data-ttu-id="8be37-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8be37-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be37-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be37-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be37-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8be37-160">INPUTS</span></span>

### <span data-ttu-id="8be37-161">Microsoft. Azure. Command. PSKeyVaultKeyIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="8be37-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="8be37-162">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8be37-162">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8be37-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8be37-163">OUTPUTS</span></span>

### <span data-ttu-id="8be37-164">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="8be37-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="8be37-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8be37-165">NOTES</span></span>

## <span data-ttu-id="8be37-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8be37-166">RELATED LINKS</span></span>
