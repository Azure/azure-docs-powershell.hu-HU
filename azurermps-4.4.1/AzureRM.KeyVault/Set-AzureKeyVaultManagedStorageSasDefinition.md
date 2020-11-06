---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: e32e57932731e788def7a8e27c85c956795b0c4e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504104"
---
# <span data-ttu-id="cf3ee-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="cf3ee-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="cf3ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf3ee-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3ee-103">Megosztott hozzáférés-aláírást (SAS) állít be a fő boltozattal egy adott kulcs boltozattal felügyelt Azure Storage-fiókkal.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf3ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf3ee-104">SYNTAX</span></span>

### <span data-ttu-id="cf3ee-105">RawSas (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf3ee-105">RawSas (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Parameter] <Hashtable> [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3ee-106">AdhocAccountSas</span><span class="sxs-lookup"><span data-stu-id="cf3ee-106">AdhocAccountSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition -Service <String[]> -ResourceType <String[]>
 [-ApiVersion <String>] [-VaultName] <String> [-AccountName] <String> [-Name] <String> [-Disable]
 [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>] [-IPAddressOrRange <String>]
 -ValidityPeriod <TimeSpan> -Permission <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3ee-107">AdhocServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="cf3ee-107">AdhocServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Blob <String>
 -Container <String> [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3ee-108">AdhocServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="cf3ee-108">AdhocServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Container <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf3ee-109">AdhocServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="cf3ee-109">AdhocServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3ee-110">AdhocServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="cf3ee-110">AdhocServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3ee-111">AdhocServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="cf3ee-111">AdhocServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Queue <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3ee-112">AdhocServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="cf3ee-112">AdhocServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Table <String>
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3ee-113">StoredPolicyServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="cf3ee-113">StoredPolicyServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Blob <String> -Container <String> -Policy <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf3ee-114">StoredPolicyServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="cf3ee-114">StoredPolicyServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Container <String> -Policy <String> [-SharedAccessHeader <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3ee-115">StoredPolicyServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="cf3ee-115">StoredPolicyServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String> -Path <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3ee-116">StoredPolicyServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="cf3ee-116">StoredPolicyServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3ee-117">StoredPolicyServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="cf3ee-117">StoredPolicyServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Queue <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3ee-118">StoredPolicyServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="cf3ee-118">StoredPolicyServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Table <String> [-StartPartitionKey <String>]
 [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf3ee-119">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf3ee-119">DESCRIPTION</span></span>
<span data-ttu-id="cf3ee-120">Megosztott hozzáférés-aláírást (SAS) állít be egy adott kulcsos, felügyelt Azure tárterület-fiókkal.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-120">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="cf3ee-121">Ez azt is megadhatja, hogy milyen titok használható a SAS-token beszerzéséhez a SAS-definícióban.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-121">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="cf3ee-122">A SAS-token az alábbi paraméterekkel és a Key Vault Managed Azure Storage Account aktív kulcsával jön létre.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-122">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="cf3ee-123">Példák</span><span class="sxs-lookup"><span data-stu-id="cf3ee-123">EXAMPLES</span></span>

### <span data-ttu-id="cf3ee-124">1. példa: ad hoc szolgáltatás blob-definíciójának beállítása</span><span class="sxs-lookup"><span data-stu-id="cf3ee-124">Example 1 : Set an ad hoc service Blob sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Blob 'blob1' -Container 'container1' -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add -SharedAccessHeader CacheControl,ContentDisposition -Protocol HttpsOnly -IPAddressOrRange '168.1.5.60-168.1.5.70'
```

<span data-ttu-id="cf3ee-125">Az "sas1" ("számítógépfiók1") a ""-as vault1</span><span class="sxs-lookup"><span data-stu-id="cf3ee-125">Sets an ad hoc service blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="cf3ee-126">2. példa: ad hoc fiók sas-definíciójának beállítása</span><span class="sxs-lookup"><span data-stu-id="cf3ee-126">Example 2 : Set an ad hoc account sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Service Blob,File -ResourceType Container,Service -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -Protocol HttpsOrHttp -IPAddressOrRange '168.1.5.60' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add
```

<span data-ttu-id="cf3ee-127">A "sas1" és a "számítógépfiók1"-es "" vault1</span><span class="sxs-lookup"><span data-stu-id="cf3ee-127">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="cf3ee-128">3. példa: sas-definíció beállítása Hashtable használatával</span><span class="sxs-lookup"><span data-stu-id="cf3ee-128">Example 3 : Set a sas definition using a hashtable</span></span>
```
PS C:\> $parameters = @{"sasType"="blob";"signedVersion"="2016-05-31";"signedProtocols"="https";"signedIp"="168.1.5.60-168.1.5.70";"validityPeriod"="P30D";"signedPermissions"="ra";"blobName"="blob1";"containerName"="container1";"rscd"="";"rscc"=""}
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -VaultName vault1 -AccountName account1 -Name sas1 -Parameter $parameters
```

<span data-ttu-id="cf3ee-129">A "sas1" és a "számítógépfiók1" vault1 "" a ""-as tárolóban egy Hashtable segítségével ad hoc blob-definíciót ad</span><span class="sxs-lookup"><span data-stu-id="cf3ee-129">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1' using a hashtable.</span></span>

## <span data-ttu-id="cf3ee-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf3ee-130">PARAMETERS</span></span>

### <span data-ttu-id="cf3ee-131">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cf3ee-131">-AccountName</span></span>
<span data-ttu-id="cf3ee-132">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-132">Key Vault managed storage account name.</span></span> <span data-ttu-id="cf3ee-133">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-133">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cf3ee-134">-ApiVersion</span></span>
<span data-ttu-id="cf3ee-135">Annak a tárterület-verziónak a használatát adja meg, amely a fiók SAS-URI használatával végzett kérés végrehajtását szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-135">Specifies the storage service version to use to execute the request made using the account SAS URI.</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocAccountSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-136">-BLOB</span><span class="sxs-lookup"><span data-stu-id="cf3ee-136">-Blob</span></span>
<span data-ttu-id="cf3ee-137">BLOB neve</span><span class="sxs-lookup"><span data-stu-id="cf3ee-137">Blob Name</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceBlobSas, StoredPolicyServiceBlobSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf3ee-138">-Confirm</span></span>
<span data-ttu-id="cf3ee-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf3ee-140">-Container</span><span class="sxs-lookup"><span data-stu-id="cf3ee-140">-Container</span></span>
<span data-ttu-id="cf3ee-141">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="cf3ee-141">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-142">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="cf3ee-142">-Disable</span></span>
<span data-ttu-id="cf3ee-143">Letiltja a sas-definíció használatát a sas-token generálásához.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-143">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="cf3ee-144">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="cf3ee-144">-EndPartitionKey</span></span>
<span data-ttu-id="cf3ee-145">A partíció befejezése gomb</span><span class="sxs-lookup"><span data-stu-id="cf3ee-145">End Partition Key</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-146">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="cf3ee-146">-EndRowKey</span></span>
<span data-ttu-id="cf3ee-147">Záró sor gombja</span><span class="sxs-lookup"><span data-stu-id="cf3ee-147">End Row Key</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-148">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="cf3ee-148">-IPAddressOrRange</span></span>
<span data-ttu-id="cf3ee-149">Az IP-cím vagy az IP-címtartomány (hozzáférés-vezérlési lista) az Azure Storage által elfogadott kéréshez.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-149">IP, or IP range ACL (access control list) of the request that would be accepted by Azure Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-150">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf3ee-150">-Name</span></span>
<span data-ttu-id="cf3ee-151">Storage sas-definíció neve.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-151">Storage sas definition name.</span></span> <span data-ttu-id="cf3ee-152">Parancsmag: a tároló biztonsági társításának FQDN-definícióját a boltozat neve, a jelenleg kijelölt környezet, a tárolási fiók neve és a sas-definíció neve alapján építi ki.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-152">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-153">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="cf3ee-153">-Parameter</span></span>
<span data-ttu-id="cf3ee-154">A sas-token létrehozásához használandó sas-definíciós paraméterek.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-154">Sas definition parameters that will be used to create the sas token.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: RawSas
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-155">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="cf3ee-155">-Path</span></span>
<span data-ttu-id="cf3ee-156">A felhőalapú fájl elérési útja, amellyel létrehozhatja a sas-tokent.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-156">Path to the cloud file to generate sas token against.</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceFileSas, StoredPolicyServiceFileSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-157">– Engedély</span><span class="sxs-lookup"><span data-stu-id="cf3ee-157">-Permission</span></span>
<span data-ttu-id="cf3ee-158">Jogosultsági.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-158">Permission.</span></span> <span data-ttu-id="cf3ee-159">Az értékek közé tartozik a "Query", "Hozzáadás", "frissítés", "folyamat"</span><span class="sxs-lookup"><span data-stu-id="cf3ee-159">Values include 'Query','Add','Update','Process'</span></span>

```yaml
Type: System.String[]
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases: 
Accepted values: Add, Create, Delete, List, Process, Read, Query, Update, Write

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-160">-Házirend</span><span class="sxs-lookup"><span data-stu-id="cf3ee-160">-Policy</span></span>
<span data-ttu-id="cf3ee-161">Házirend-azonosító</span><span class="sxs-lookup"><span data-stu-id="cf3ee-161">Policy Identifier</span></span>

```yaml
Type: System.String
Parameter Sets: StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-162">-Protocol</span><span class="sxs-lookup"><span data-stu-id="cf3ee-162">-Protocol</span></span>
<span data-ttu-id="cf3ee-163">A protokollt használhatja a kérésben a SAS-jogkivonattal.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-163">Protocol can be used in the request with the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-164">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="cf3ee-164">-Queue</span></span>
<span data-ttu-id="cf3ee-165">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="cf3ee-165">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceQueueSas, StoredPolicyServiceQueueSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-166">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="cf3ee-166">-ResourceType</span></span>
<span data-ttu-id="cf3ee-167">Azok az erőforrástípusok, amelyekre ez a SAS-jogkivonat vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-167">Resource types that this SAS token applies to.</span></span> <span data-ttu-id="cf3ee-168">Az értékek közé tartozik a "szolgáltatás", a "tároló", az "objektum"</span><span class="sxs-lookup"><span data-stu-id="cf3ee-168">Values include 'Service','Container','Object'</span></span>

```yaml
Type: System.String[]
Parameter Sets: AdhocAccountSas
Aliases: 
Accepted values: Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-169">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="cf3ee-169">-Service</span></span>
<span data-ttu-id="cf3ee-170">Azok a szolgáltatások, amelyekre ez a SAS-jogkivonat vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-170">Service types that this SAS token applies to.</span></span> <span data-ttu-id="cf3ee-171">Az értékek közé tartozik a "blob", "fájl", "várólista", "táblázat"</span><span class="sxs-lookup"><span data-stu-id="cf3ee-171">Values include 'Blob','File','Queue','Table'</span></span>

```yaml
Type: System.String[]
Parameter Sets: AdhocAccountSas
Aliases: 
Accepted values: Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-172">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="cf3ee-172">-Share</span></span>
<span data-ttu-id="cf3ee-173">Megosztás neve</span><span class="sxs-lookup"><span data-stu-id="cf3ee-173">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-174">-SharedAccessHeader</span><span class="sxs-lookup"><span data-stu-id="cf3ee-174">-SharedAccessHeader</span></span>
<span data-ttu-id="cf3ee-175">A válasz fejlécének felülírására szolgáló lekérdezési paramétereket adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-175">Specifies the query parameters to override response headers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases: 
Accepted values: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-176">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="cf3ee-176">-StartPartitionKey</span></span>
<span data-ttu-id="cf3ee-177">A Partition Start gomb</span><span class="sxs-lookup"><span data-stu-id="cf3ee-177">Start Partition Key</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-178">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="cf3ee-178">-StartRowKey</span></span>
<span data-ttu-id="cf3ee-179">A sor indítása gomb</span><span class="sxs-lookup"><span data-stu-id="cf3ee-179">Start Row Key</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-180">-Table</span><span class="sxs-lookup"><span data-stu-id="cf3ee-180">-Table</span></span>
<span data-ttu-id="cf3ee-181">Táblázat neve</span><span class="sxs-lookup"><span data-stu-id="cf3ee-181">Table Name</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-182">-Címke</span><span class="sxs-lookup"><span data-stu-id="cf3ee-182">-Tag</span></span>
<span data-ttu-id="cf3ee-183">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cf3ee-184">Példa:</span><span class="sxs-lookup"><span data-stu-id="cf3ee-184">For example:</span></span>

<span data-ttu-id="cf3ee-185">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="cf3ee-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-186">-TargetStorageVersion</span><span class="sxs-lookup"><span data-stu-id="cf3ee-186">-TargetStorageVersion</span></span>
<span data-ttu-id="cf3ee-187">Annak az aláírt tárterület-verziónak a verziószáma, amelyet a SAS-tokenrel végzett kérelmek hitelesítéséhez használ a rendszer.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-187">Specifies the signed storage service version to use to authenticate requests made with the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-188">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="cf3ee-188">-ValidityPeriod</span></span>
<span data-ttu-id="cf3ee-189">Annak az érvényességi időszaknak a meghatározása, amely a sas-token lejárati időpontjának a generált időponttól való beállításához használatos.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-189">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-190">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cf3ee-190">-VaultName</span></span>
<span data-ttu-id="cf3ee-191">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-191">Vault name.</span></span>
<span data-ttu-id="cf3ee-192">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-192">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf3ee-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf3ee-193">-WhatIf</span></span>
<span data-ttu-id="cf3ee-194">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf3ee-195">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf3ee-196">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3ee-196">-DefaultProfile</span></span>
<span data-ttu-id="cf3ee-197">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-197">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf3ee-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3ee-198">CommonParameters</span></span>
<span data-ttu-id="cf3ee-199">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf3ee-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3ee-200">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf3ee-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3ee-201">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf3ee-201">INPUTS</span></span>

## <span data-ttu-id="cf3ee-202">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf3ee-202">OUTPUTS</span></span>

### <span data-ttu-id="cf3ee-203">Microsoft. Azure. Command. ManagedStorageSasDefinition. models.</span><span class="sxs-lookup"><span data-stu-id="cf3ee-203">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="cf3ee-204">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf3ee-204">NOTES</span></span>

## <span data-ttu-id="cf3ee-205">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf3ee-205">RELATED LINKS</span></span>

[<span data-ttu-id="cf3ee-206">Azureâ € ‹ RM. â € ‹ keyĂ € ‹ Vault</span><span class="sxs-lookup"><span data-stu-id="cf3ee-206">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)