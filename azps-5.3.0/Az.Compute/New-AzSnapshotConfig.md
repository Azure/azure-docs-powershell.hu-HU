---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 5d9a48fbdc323ffdd232d6d961da6564fecc0dff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480817"
---
# <span data-ttu-id="e4176-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e4176-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="e4176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4176-102">SYNOPSIS</span></span>
<span data-ttu-id="e4176-103">Konfigurálható pillanatkép-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e4176-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="e4176-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e4176-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4176-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e4176-105">DESCRIPTION</span></span>
<span data-ttu-id="e4176-106">A **New-AzSnapshotConfig** parancsmag létrehoz egy konfigurálható pillanatkép-objektumot.</span><span class="sxs-lookup"><span data-stu-id="e4176-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="e4176-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e4176-107">EXAMPLES</span></span>

### <span data-ttu-id="e4176-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e4176-108">Example 1</span></span>
```powershell
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="e4176-109">Az első parancs létrehoz egy 5 GB-os méretű helyi üres pillanatfelvételi objektumot Standard_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="e4176-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="e4176-110">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="e4176-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e4176-111">A második és a harmadik parancs a pillanatfelvételi objektum lemeztitkosítási és kulcstitkosítási kulcsának beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4176-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="e4176-112">Az utolsó parancs a pillanatfelvételi objektumot a "Snapshot01" néven hozza létre az Erőforráscsoport01 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="e4176-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="e4176-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e4176-113">Example 2</span></span>

<span data-ttu-id="e4176-114">Konfigurálható pillanatkép-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e4176-114">Creates a configurable snapshot object.</span></span> <span data-ttu-id="e4176-115">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="e4176-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzSnapshotConfig -CreateOption Empty -Location 'Central US' -SourceUri 'https://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd'
```

## <span data-ttu-id="e4176-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4176-116">PARAMETERS</span></span>

### <span data-ttu-id="e4176-117">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="e4176-117">-CreateOption</span></span>
<span data-ttu-id="e4176-118">Azt adja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépben egy platformról vagy egy felhasználói képről, létrehoz-e egy üres lemezt, vagy csatol-e egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="e4176-118">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="e4176-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4176-119">-DefaultProfile</span></span>
<span data-ttu-id="e4176-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4176-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4176-121">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e4176-121">-DiskEncryptionKey</span></span>
<span data-ttu-id="e4176-122">A lemeztitkosítási kulcs objektumát adja meg egy pillanatfelvételen.</span><span class="sxs-lookup"><span data-stu-id="e4176-122">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="e4176-123">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e4176-123">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e4176-124">Megadja annak a lemeztitkosítási készletnek az erőforrás-azonosítóját, amely a nyugta titkosítás engedélyezéséhez használható.</span><span class="sxs-lookup"><span data-stu-id="e4176-124">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="e4176-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e4176-125">-DiskSizeGB</span></span>
<span data-ttu-id="e4176-126">A lemez mérete GB-ban.</span><span class="sxs-lookup"><span data-stu-id="e4176-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="e4176-127">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="e4176-127">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="e4176-128">Engedélyezze a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="e4176-128">Enable encryption settings.</span></span>

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

### <span data-ttu-id="e4176-129">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="e4176-129">-EncryptionType</span></span>
<span data-ttu-id="e4176-130">A lemez adatainak titkosításához használt kulcs típusa.</span><span class="sxs-lookup"><span data-stu-id="e4176-130">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="e4176-131">A rendelkezésre álló értékek: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="e4176-131">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="e4176-132">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="e4176-132">-DiskAccessId</span></span>
<span data-ttu-id="e4176-133">Beállítja ARM a DiskAccess erőforrás azonosítóját a privát végpontok használatának beállításával.</span><span class="sxs-lookup"><span data-stu-id="e4176-133">Gets or sets ARM id of the DiskAccess resource for using private endpoints on.</span></span>

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

### <span data-ttu-id="e4176-134">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e4176-134">-NetworkAccessPolicy</span></span>
<span data-ttu-id="e4176-135">A hálózati hozzáférési házirend határozza meg a hálózati hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="e4176-135">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="e4176-136">Lehetséges értékek: "AllowAll", "AllowPrivate", "DenyAll"</span><span class="sxs-lookup"><span data-stu-id="e4176-136">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="e4176-137">-HyperVGeneráció</span><span class="sxs-lookup"><span data-stu-id="e4176-137">-HyperVGeneration</span></span>
<span data-ttu-id="e4176-138">A virtuális gép hipervizor-generálása.</span><span class="sxs-lookup"><span data-stu-id="e4176-138">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="e4176-139">Csak operációs rendszer lemezei esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="e4176-139">Applicable to OS disks only.</span></span>  <span data-ttu-id="e4176-140">Az engedélyezett értékek a V1 és a V2.</span><span class="sxs-lookup"><span data-stu-id="e4176-140">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="e4176-141">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="e4176-141">-ImageReference</span></span>
<span data-ttu-id="e4176-142">Egy pillanatfelvétel képhivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4176-142">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4176-143">-Növekményes</span><span class="sxs-lookup"><span data-stu-id="e4176-143">-Incremental</span></span>
<span data-ttu-id="e4176-144">Növekményes pillanatképet ad meg.</span><span class="sxs-lookup"><span data-stu-id="e4176-144">Specifies an incremental snapshot.</span></span> <span data-ttu-id="e4176-145">A növekményes pillanatfelvételek ugyanazon a lemezen kevesebb helyet foglalnak el, mint a teljes pillanatfelvételek, és meg is különböztethetőek.</span><span class="sxs-lookup"><span data-stu-id="e4176-145">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4176-146">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e4176-146">-KeyEncryptionKey</span></span>
<span data-ttu-id="e4176-147">A kulcstitkosítási kulcsot adja meg egy pillanatfelvételen.</span><span class="sxs-lookup"><span data-stu-id="e4176-147">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="e4176-148">-Location</span><span class="sxs-lookup"><span data-stu-id="e4176-148">-Location</span></span>
<span data-ttu-id="e4176-149">Megadja a helyet.</span><span class="sxs-lookup"><span data-stu-id="e4176-149">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4176-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="e4176-150">-OsType</span></span>
<span data-ttu-id="e4176-151">Az operációs rendszer típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e4176-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="e4176-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e4176-152">-SkuName</span></span>
<span data-ttu-id="e4176-153">A tárfiók termékváltozatnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4176-153">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="e4176-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e4176-154">-SourceResourceId</span></span>
<span data-ttu-id="e4176-155">A forráserőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e4176-155">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="e4176-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="e4176-156">-SourceUri</span></span>
<span data-ttu-id="e4176-157">A forrás Uri-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4176-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="e4176-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e4176-158">-StorageAccountId</span></span>
<span data-ttu-id="e4176-159">Megadja a tárfiók azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="e4176-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="e4176-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="e4176-160">-Tag</span></span>
<span data-ttu-id="e4176-161">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="e4176-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e4176-162">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="e4176-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4176-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4176-163">-Confirm</span></span>
<span data-ttu-id="e4176-164">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e4176-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4176-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4176-165">-WhatIf</span></span>
<span data-ttu-id="e4176-166">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e4176-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4176-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4176-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4176-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4176-168">CommonParameters</span></span>
<span data-ttu-id="e4176-169">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4176-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4176-170">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4176-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4176-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4176-171">INPUTS</span></span>

### <span data-ttu-id="e4176-172">System.String</span><span class="sxs-lookup"><span data-stu-id="e4176-172">System.String</span></span>

### <span data-ttu-id="e4176-173">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e4176-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e4176-174">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e4176-174">System.Int32</span></span>

### <span data-ttu-id="e4176-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e4176-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e4176-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="e4176-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="e4176-177">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e4176-177">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e4176-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="e4176-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="e4176-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="e4176-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="e4176-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4176-180">OUTPUTS</span></span>

### <span data-ttu-id="e4176-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="e4176-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="e4176-182">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e4176-182">NOTES</span></span>

## <span data-ttu-id="e4176-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4176-183">RELATED LINKS</span></span>
