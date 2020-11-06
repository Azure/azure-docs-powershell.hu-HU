---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: a71aed4703158c68d3b156ff1e37d438e5413782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495098"
---
# <span data-ttu-id="d7236-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="d7236-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="d7236-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7236-102">SYNOPSIS</span></span>
<span data-ttu-id="d7236-103">Megosztott hozzáférés-aláírást (SAS) állít be a fő boltozattal egy adott kulcs boltozattal felügyelt Azure Storage-fiókkal.</span><span class="sxs-lookup"><span data-stu-id="d7236-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7236-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7236-104">SYNTAX</span></span>

### <span data-ttu-id="d7236-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7236-105">Default (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7236-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7236-106">ByInputObject</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7236-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7236-107">DESCRIPTION</span></span>
<span data-ttu-id="d7236-108">Megosztott hozzáférés-aláírást (SAS) állít be egy adott kulcsos, felügyelt Azure tárterület-fiókkal.</span><span class="sxs-lookup"><span data-stu-id="d7236-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="d7236-109">Ez azt is megadhatja, hogy milyen titok használható a SAS-token beszerzéséhez a SAS-definícióban.</span><span class="sxs-lookup"><span data-stu-id="d7236-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="d7236-110">A SAS-token az alábbi paraméterekkel és a Key Vault Managed Azure Storage Account aktív kulcsával jön létre.</span><span class="sxs-lookup"><span data-stu-id="d7236-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="d7236-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d7236-111">EXAMPLES</span></span>

### <span data-ttu-id="d7236-112">Példa 1: fiók típusú SAS-definíció beállítása, és a jelenlegi biztonsági társítási jogkivonat beolvasása az alapján</span><span class="sxs-lookup"><span data-stu-id="d7236-112">Example 1 : Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzureRmStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzureRmKeyVault -VaultName mykv
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod 180
PS C:\> $sctx = New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzureStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzureKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="d7236-113">Egy "accountsas" fiókját egy "mysa" "mykv" tárolóban, a "".</span><span class="sxs-lookup"><span data-stu-id="d7236-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="d7236-114">A fenti sorrend konkrétan a következőket hajtja végre:</span><span class="sxs-lookup"><span data-stu-id="d7236-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="d7236-115">egy (meglévő) tárterület-fiókot kap</span><span class="sxs-lookup"><span data-stu-id="d7236-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="d7236-116">beolvassa a (korábbi) kulcs boltozatát</span><span class="sxs-lookup"><span data-stu-id="d7236-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="d7236-117">egy kulcskezelő által felügyelt tárolási fiók hozzáadása a boltozathoz, a Key1 beállítása aktív kulcsként, valamint a 180 napok regenerálási időszaka</span><span class="sxs-lookup"><span data-stu-id="d7236-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="d7236-118">tárolási környezet beállítása a megadott tárterület-fiókhoz a Key1 használatával</span><span class="sxs-lookup"><span data-stu-id="d7236-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="d7236-119">a fiókhoz tartozó SAS-tokent hoz létre a szolgáltatások Blobja, a fájl, a táblázat és a várólista, az erőforrástípusok szolgáltatáshoz, a tárolóhoz és az objektumhoz, az összes engedély, a https és a megadott kezdési és befejezési dátum</span><span class="sxs-lookup"><span data-stu-id="d7236-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="d7236-120">a boltozattal felügyelt tárterület biztonsági társítását állítja be a Vault-ban, és a sablon URI-ja a fenti néven létrehozott SAS-token, a "fiók" vagy 30 napig érvényes</span><span class="sxs-lookup"><span data-stu-id="d7236-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="d7236-121">beolvassa a tényleges hozzáférési jogkivonatot a biztonsági társítás definíciójának megfelelő kulcsból.</span><span class="sxs-lookup"><span data-stu-id="d7236-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="d7236-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7236-122">PARAMETERS</span></span>

### <span data-ttu-id="d7236-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d7236-123">-AccountName</span></span>
<span data-ttu-id="d7236-124">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d7236-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="d7236-125">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="d7236-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="d7236-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7236-126">-DefaultProfile</span></span>
<span data-ttu-id="d7236-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d7236-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7236-128">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="d7236-128">-Disable</span></span>
<span data-ttu-id="d7236-129">Letiltja a sas-definíció használatát a sas-token generálásához.</span><span class="sxs-lookup"><span data-stu-id="d7236-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="d7236-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7236-130">-InputObject</span></span>
<span data-ttu-id="d7236-131">ManagedStorageAccount objektum</span><span class="sxs-lookup"><span data-stu-id="d7236-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="d7236-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7236-132">-Name</span></span>
<span data-ttu-id="d7236-133">Storage sas-definíció neve.</span><span class="sxs-lookup"><span data-stu-id="d7236-133">Storage sas definition name.</span></span> <span data-ttu-id="d7236-134">Parancsmag: a tároló biztonsági társításának FQDN-definícióját a boltozat neve, a jelenleg kijelölt környezet, a tárolási fiók neve és a sas-definíció neve alapján építi ki.</span><span class="sxs-lookup"><span data-stu-id="d7236-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="d7236-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="d7236-135">-SasType</span></span>
<span data-ttu-id="d7236-136">Storage SAS típus.</span><span class="sxs-lookup"><span data-stu-id="d7236-136">Storage SAS type.</span></span>

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

### <span data-ttu-id="d7236-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="d7236-137">-Tag</span></span>
<span data-ttu-id="d7236-138">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="d7236-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d7236-139">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="d7236-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d7236-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="d7236-140">-TemplateUri</span></span>
<span data-ttu-id="d7236-141">Tárolási SAS-definíciós sablon URI-ja</span><span class="sxs-lookup"><span data-stu-id="d7236-141">Storage SAS definition template uri.</span></span>

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

### <span data-ttu-id="d7236-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="d7236-142">-ValidityPeriod</span></span>
<span data-ttu-id="d7236-143">Annak az érvényességi időszaknak a meghatározása, amely a sas-token lejárati időpontjának a generált időponttól való beállításához használatos.</span><span class="sxs-lookup"><span data-stu-id="d7236-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

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

### <span data-ttu-id="d7236-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d7236-144">-VaultName</span></span>
<span data-ttu-id="d7236-145">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="d7236-145">Vault name.</span></span>
<span data-ttu-id="d7236-146">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="d7236-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d7236-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7236-147">-Confirm</span></span>
<span data-ttu-id="d7236-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7236-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7236-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7236-149">-WhatIf</span></span>
<span data-ttu-id="d7236-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7236-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7236-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7236-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7236-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7236-152">CommonParameters</span></span>
<span data-ttu-id="d7236-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7236-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7236-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7236-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7236-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7236-155">INPUTS</span></span>

### <span data-ttu-id="d7236-156">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccountIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="d7236-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="d7236-157">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d7236-157">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d7236-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7236-158">OUTPUTS</span></span>

### <span data-ttu-id="d7236-159">Microsoft. Azure. Command. PSKeyVaultManagedStorageSasDefinition. models.</span><span class="sxs-lookup"><span data-stu-id="d7236-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="d7236-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7236-160">NOTES</span></span>

## <span data-ttu-id="d7236-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7236-161">RELATED LINKS</span></span>

[<span data-ttu-id="d7236-162">Azureâ € ‹ RM. â € ‹ keyĂ € ‹ Vault</span><span class="sxs-lookup"><span data-stu-id="d7236-162">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)
