---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 82d7c1768b9e7f702b87a2bd23afcc76257b937f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927234"
---
# <span data-ttu-id="f84f8-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="f84f8-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="f84f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f84f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f84f8-103">Konfigurálható pillanatkép-frissítő objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f84f8-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="f84f8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f84f8-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f84f8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f84f8-105">DESCRIPTION</span></span>
<span data-ttu-id="f84f8-106">A **New-AzSnapshotUpdateConfig parancsmag** létrehoz egy konfigurálható pillanatkép-frissítő objektumot.</span><span class="sxs-lookup"><span data-stu-id="f84f8-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="f84f8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f84f8-107">EXAMPLES</span></span>

### <span data-ttu-id="f84f8-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f84f8-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="f84f8-109">Az első parancs létrehoz egy 10 GB-os helyi üres pillanatkép-frissítő objektumot Premium_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="f84f8-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="f84f8-110">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="f84f8-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="f84f8-111">A második és a harmadik parancs a lemeztitkosítási kulcs és a kulcstitkosítási kulcs beállításait adja meg a pillanatfelvételi frissítési objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="f84f8-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="f84f8-112">Az utolsó parancs az "Erőforráscsoport01" erőforráscsoport "Snapshot01" nevű pillanatképét frissíti a pillanatkép-frissítő objektummal.</span><span class="sxs-lookup"><span data-stu-id="f84f8-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f84f8-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="f84f8-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="f84f8-114">Ez a parancs egy "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoportban 10 GB-os lemezméretre frissíti.</span><span class="sxs-lookup"><span data-stu-id="f84f8-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="f84f8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f84f8-115">PARAMETERS</span></span>

### <span data-ttu-id="f84f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84f8-116">-DefaultProfile</span></span>
<span data-ttu-id="f84f8-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f84f8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f84f8-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f84f8-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="f84f8-119">A lemeztitkosítási kulcs objektumát adja meg egy pillanatfelvételen.</span><span class="sxs-lookup"><span data-stu-id="f84f8-119">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84f8-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="f84f8-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="f84f8-121">Megadja annak a lemeztitkosítási készletnek az erőforrás-azonosítóját, amely a nyugta titkosítás engedélyezéséhez használható.</span><span class="sxs-lookup"><span data-stu-id="f84f8-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84f8-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="f84f8-122">-DiskSizeGB</span></span>
<span data-ttu-id="f84f8-123">A lemez mérete GB-ban.</span><span class="sxs-lookup"><span data-stu-id="f84f8-123">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84f8-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="f84f8-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="f84f8-125">Engedélyezze a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="f84f8-125">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84f8-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="f84f8-126">-EncryptionType</span></span>
<span data-ttu-id="f84f8-127">A lemez adatainak titkosításához használt kulcs típusa.</span><span class="sxs-lookup"><span data-stu-id="f84f8-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="f84f8-128">A rendelkezésre álló értékek: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="f84f8-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84f8-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f84f8-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="f84f8-130">A kulcstitkosítási kulcsot adja meg egy pillanatfelvételen.</span><span class="sxs-lookup"><span data-stu-id="f84f8-130">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84f8-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="f84f8-131">-OsType</span></span>
<span data-ttu-id="f84f8-132">Az operációs rendszer típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f84f8-132">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84f8-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f84f8-133">-SkuName</span></span>
<span data-ttu-id="f84f8-134">A tárfiók termékváltozatnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f84f8-134">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84f8-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f84f8-135">-Tag</span></span>
<span data-ttu-id="f84f8-136">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="f84f8-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f84f8-137">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="f84f8-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84f8-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f84f8-138">-Confirm</span></span>
<span data-ttu-id="f84f8-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f84f8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f84f8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f84f8-140">-WhatIf</span></span>
<span data-ttu-id="f84f8-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f84f8-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f84f8-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f84f8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f84f8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84f8-143">CommonParameters</span></span>
<span data-ttu-id="f84f8-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f84f8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84f8-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f84f8-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84f8-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f84f8-146">INPUTS</span></span>

### <span data-ttu-id="f84f8-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f84f8-147">System.String</span></span>

### <span data-ttu-id="f84f8-148">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f84f8-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f84f8-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f84f8-149">System.Int32</span></span>

### <span data-ttu-id="f84f8-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f84f8-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f84f8-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f84f8-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f84f8-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="f84f8-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="f84f8-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="f84f8-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="f84f8-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f84f8-154">OUTPUTS</span></span>

### <span data-ttu-id="f84f8-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="f84f8-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="f84f8-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f84f8-156">NOTES</span></span>

## <span data-ttu-id="f84f8-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f84f8-157">RELATED LINKS</span></span>
