---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff73d5db0b16d7176b9c49aa6e70bc13fc9f3fba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334110"
---
# <span data-ttu-id="7f8b6-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="7f8b6-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="7f8b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f8b6-102">SYNOPSIS</span></span>
<span data-ttu-id="7f8b6-103">Egy megosztott hozzáférés-aláírás (SAS) definícióját állítja be egy adott, kulcstárolóval felügyelt Azure Storage-fiók kulcstárával.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="7f8b6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7f8b6-104">SYNTAX</span></span>

### <span data-ttu-id="7f8b6-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f8b6-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f8b6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7f8b6-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f8b6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7f8b6-107">DESCRIPTION</span></span>
<span data-ttu-id="7f8b6-108">Megosztott hozzáférés-aláírás (SAS) definícióját állítja be egy adott kulcstároló által felügyelt Azure Storage-fiókkal.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="7f8b6-109">Ez egy olyan titkos halmazt is beállítja, amellyel be lehet szerezni az SAS-jogkivonatot ebben az SAS-definícióban.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="7f8b6-110">Az SAS-jogkivonat generálása ezekkel a paraméterekkel és a kulcstároló által felügyelt Azure Storage-fiók aktív kulcsával jön létre.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="7f8b6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7f8b6-111">EXAMPLES</span></span>

### <span data-ttu-id="7f8b6-112">1. példa: Fióktípusú SAS-definíció beállítása és az alapján aktuális SAS-jogkivonat beszerzése</span><span class="sxs-lookup"><span data-stu-id="7f8b6-112">Example 1: Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzKeyVault -VaultName mykv
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod ([System.Timespan]::FromDays(180))
PS C:\> $sctx = New-AzStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="7f8b6-113">Egy "mykv" tárolóban egy KeyVault-felügyelt tárfiók "mysa" szolgáltatásában beállítja a fiók SAS-definíciójának "accountsas" beállítását.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="7f8b6-114">Konkrétan a fenti sorozat az alábbi műveleteket végzi el:</span><span class="sxs-lookup"><span data-stu-id="7f8b6-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="7f8b6-115">(meglévő) tárfiókot kap</span><span class="sxs-lookup"><span data-stu-id="7f8b6-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="7f8b6-116">kap egy (meglévő) kulcstárat</span><span class="sxs-lookup"><span data-stu-id="7f8b6-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="7f8b6-117">hozzáad egy KeyVault-kezelt tárfiókot a tárolóhoz, a Kulcs1 értéket aktív kulcsként 180 napos időszakkal megszabadítva</span><span class="sxs-lookup"><span data-stu-id="7f8b6-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="7f8b6-118">beállítja a tárterület környezetét a megadott tárfiókhoz a Kulcs1 billentyűvel</span><span class="sxs-lookup"><span data-stu-id="7f8b6-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="7f8b6-119">létrehoz egy fiók SAS-jogkivonatot a szolgáltatások blobjának, fájljának, táblázatának és várólistájának, az erőforrástípusok szolgáltatásának, tárolójának és objektumának, az összes engedélyével a https protokollon keresztül, valamint a megadott kezdési és befejezési dátummal</span><span class="sxs-lookup"><span data-stu-id="7f8b6-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="7f8b6-120">Egy KeyVault-kezelt tároló SAS-definíciót állít be a tárolóban úgy, hogy a fent létrehozott SAS-tokenként a uri sablon "fiók" típusú, és 30 napig érvényes legyen</span><span class="sxs-lookup"><span data-stu-id="7f8b6-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="7f8b6-121">Lekéri a tényleges hozzáférési jogkivonatot az SAS-definíciónak megfelelő KeyVault-titkos kulcsból</span><span class="sxs-lookup"><span data-stu-id="7f8b6-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="7f8b6-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f8b6-122">PARAMETERS</span></span>

### <span data-ttu-id="7f8b6-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7f8b6-123">-AccountName</span></span>
<span data-ttu-id="7f8b6-124">Key Vault managed storage account name.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="7f8b6-125">A parancsmag egy felügyelt tárfiók nevének FQDN-ét építi fel a tárolónévből, az aktuálisan kijelölt környezetből és a felügyelt tárfiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8b6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f8b6-126">-DefaultProfile</span></span>
<span data-ttu-id="7f8b6-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7f8b6-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f8b6-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="7f8b6-128">-Disable</span></span>
<span data-ttu-id="7f8b6-129">Letiltja a sas-definíció használatát a sas tokenek generálásához.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="7f8b6-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f8b6-130">-InputObject</span></span>
<span data-ttu-id="7f8b6-131">ManagedStorageAccount objektum.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-131">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f8b6-132">-Name</span><span class="sxs-lookup"><span data-stu-id="7f8b6-132">-Name</span></span>
<span data-ttu-id="7f8b6-133">Tárterület sas-definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-133">Storage sas definition name.</span></span> <span data-ttu-id="7f8b6-134">A parancsmag egy tárolónévből ( jelenleg kijelölt környezetből, tárfiók neve és sas-definíció neve) származó tár sas-definíciójának teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8b6-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="7f8b6-135">-SasType</span></span>
<span data-ttu-id="7f8b6-136">Tárterület SAS-típusa.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-136">Storage SAS type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8b6-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f8b6-137">-Tag</span></span>
<span data-ttu-id="7f8b6-138">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7f8b6-139">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="7f8b6-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7f8b6-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="7f8b6-140">-TemplateUri</span></span>
<span data-ttu-id="7f8b6-141">Storage SAS-definíciós sablon uri.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-141">Storage SAS definition template uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8b6-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="7f8b6-142">-ValidityPeriod</span></span>
<span data-ttu-id="7f8b6-143">A sas token lejárati idejének a generálástól való beállításakor használt érvényességi idő</span><span class="sxs-lookup"><span data-stu-id="7f8b6-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8b6-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7f8b6-144">-VaultName</span></span>
<span data-ttu-id="7f8b6-145">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-145">Vault name.</span></span>
<span data-ttu-id="7f8b6-146">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="7f8b6-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f8b6-147">-Confirm</span></span>
<span data-ttu-id="7f8b6-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f8b6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f8b6-149">-WhatIf</span></span>
<span data-ttu-id="7f8b6-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f8b6-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f8b6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f8b6-152">CommonParameters</span></span>
<span data-ttu-id="7f8b6-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f8b6-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f8b6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f8b6-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f8b6-155">INPUTS</span></span>

### <span data-ttu-id="7f8b6-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7f8b6-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="7f8b6-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f8b6-157">OUTPUTS</span></span>

### <span data-ttu-id="7f8b6-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="7f8b6-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="7f8b6-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7f8b6-159">NOTES</span></span>

## <span data-ttu-id="7f8b6-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f8b6-160">RELATED LINKS</span></span>

[<span data-ttu-id="7f8b6-161">Azureâ€™RM.â€</span><span class="sxs-lookup"><span data-stu-id="7f8b6-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
