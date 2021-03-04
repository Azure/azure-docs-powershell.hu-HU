---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: e73a6bc0d1bf1d2930396bce779bcb03f91d9936
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921409"
---
# <span data-ttu-id="181eb-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="181eb-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="181eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="181eb-102">SYNOPSIS</span></span>
<span data-ttu-id="181eb-103">Konfigurálható lemezfrissítési objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="181eb-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="181eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="181eb-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-BurstingEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="181eb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="181eb-105">DESCRIPTION</span></span>
<span data-ttu-id="181eb-106">A **New-AzDiskUpdateConfig parancsmag** létrehoz egy konfigurálható lemezfrissítési objektumot.</span><span class="sxs-lookup"><span data-stu-id="181eb-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="181eb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="181eb-107">EXAMPLES</span></span>

### <span data-ttu-id="181eb-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="181eb-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="181eb-109">Az első parancs egy 10 GB-os helyi üres lemezfrissítési objektumot hoz létre Premium_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="181eb-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="181eb-110">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="181eb-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="181eb-111">A második és a harmadik parancs a lemezfrissítési objektum lemeztitkosítási kulcsának és kulcstitkosítási kulcsának beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="181eb-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="181eb-112">Az utolsó parancs a lemezfrissítési objektumot veszi fel, és frissíti a "Disk01" nevű meglévő lemez nevét az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="181eb-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="181eb-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="181eb-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="181eb-114">Ez a parancs 10 GB-os lemezméretre frissíti az "ResourceGroup01" erőforráscsoport "Disk01" nevű meglévő lemezét.</span><span class="sxs-lookup"><span data-stu-id="181eb-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="181eb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="181eb-115">PARAMETERS</span></span>

### <span data-ttu-id="181eb-116">-TetszetvesEnabled</span><span class="sxs-lookup"><span data-stu-id="181eb-116">-BurstingEnabled</span></span>
<span data-ttu-id="181eb-117">Lehetővé teszi, hogy a program a kiépített teljesítménycélon túlra sorozatos sorozatot létesítsen a lemezen.</span><span class="sxs-lookup"><span data-stu-id="181eb-117">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="181eb-118">A sorozatfelvétel alapértelmezés szerint le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="181eb-118">Bursting is disabled by default.</span></span> <span data-ttu-id="181eb-119">Az Ultra lemezre nem érvényes.</span><span class="sxs-lookup"><span data-stu-id="181eb-119">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="181eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181eb-120">-DefaultProfile</span></span>
<span data-ttu-id="181eb-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="181eb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="181eb-122">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="181eb-122">-DiskAccessId</span></span>
<span data-ttu-id="181eb-123">{{ Fill DiskAccessId Description }}</span><span class="sxs-lookup"><span data-stu-id="181eb-123">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="181eb-124">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="181eb-124">-DiskEncryptionKey</span></span>
<span data-ttu-id="181eb-125">A lemezen található lemeztitkosítási kulcsobjektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="181eb-125">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="181eb-126">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="181eb-126">-DiskEncryptionSetId</span></span>
<span data-ttu-id="181eb-127">Megadja annak a lemeztitkosítási készletnek az erőforrás-azonosítóját, amely a nyugta titkosítás engedélyezéséhez használható.</span><span class="sxs-lookup"><span data-stu-id="181eb-127">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="181eb-128">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="181eb-128">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="181eb-129">Az összes olyan VM-hez engedélyezett IOPS-fájlok száma, amelyek a megosztott lemezhez ReadOnly-ként lesznek rögzítve.</span><span class="sxs-lookup"><span data-stu-id="181eb-129">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="181eb-130">Egy művelet 4 és 256 bájt közötti átvitelt tud.</span><span class="sxs-lookup"><span data-stu-id="181eb-130">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="181eb-131">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="181eb-131">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="181eb-132">Az ehhez a lemezhez engedélyezett IOPS-k száma; csak az UltraSSD-lemezhez van beállítva.</span><span class="sxs-lookup"><span data-stu-id="181eb-132">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="181eb-133">Egy művelet 4 és 256 bájt közötti átvitelt tud.</span><span class="sxs-lookup"><span data-stu-id="181eb-133">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="181eb-134">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="181eb-134">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="181eb-135">Az a teljes átviteli sebesség (MBps), amely az összes olyan virtuális gép számára engedélyezett, amely a megosztott lemezhez ReadOnly átvitelt rögzít.</span><span class="sxs-lookup"><span data-stu-id="181eb-135">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="181eb-136">A MBps másodpercenként több millió bájtot jelent – a MB itt a 10-eshatalmak ISO-ként való meghatalmazását használja.</span><span class="sxs-lookup"><span data-stu-id="181eb-136">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="181eb-137">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="181eb-137">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="181eb-138">A lemezhez engedélyezett sávszélesség; csak az UltraSSD-lemezhez van beállítva.</span><span class="sxs-lookup"><span data-stu-id="181eb-138">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="181eb-139">A MBps másodpercenként több millió bájtot jelent – a MB itt a 10-eshatalmak ISO-ként való meghatalmazását használja.</span><span class="sxs-lookup"><span data-stu-id="181eb-139">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="181eb-140">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="181eb-140">-DiskSizeGB</span></span>
<span data-ttu-id="181eb-141">A lemez mérete GB-ban.</span><span class="sxs-lookup"><span data-stu-id="181eb-141">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="181eb-142">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="181eb-142">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="181eb-143">Engedélyezze a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="181eb-143">Enable encryption settings.</span></span>

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

### <span data-ttu-id="181eb-144">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="181eb-144">-EncryptionType</span></span>
<span data-ttu-id="181eb-145">A lemez adatainak titkosításához használt kulcs típusa.</span><span class="sxs-lookup"><span data-stu-id="181eb-145">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="181eb-146">A rendelkezésre álló értékek: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="181eb-146">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="181eb-147">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="181eb-147">-KeyEncryptionKey</span></span>
<span data-ttu-id="181eb-148">A lemez kulcstitkosítási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="181eb-148">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="181eb-149">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="181eb-149">-MaxSharesCount</span></span>
<span data-ttu-id="181eb-150">A lemezhez egyszerre csatolhat virtuális gépek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="181eb-150">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="181eb-151">Az egynél nagyobb érték olyan lemez, amely egyszerre több virtuális gépre is fel lehet szerelve.</span><span class="sxs-lookup"><span data-stu-id="181eb-151">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="181eb-152">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="181eb-152">-NetworkAccessPolicy</span></span>
<span data-ttu-id="181eb-153">{{ Fill NetworkAccessPolicy Description }}</span><span class="sxs-lookup"><span data-stu-id="181eb-153">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="181eb-154">-OsType</span><span class="sxs-lookup"><span data-stu-id="181eb-154">-OsType</span></span>
<span data-ttu-id="181eb-155">Az operációs rendszer típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="181eb-155">Specifies the OS type.</span></span>

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

### <span data-ttu-id="181eb-156">-SkuName</span><span class="sxs-lookup"><span data-stu-id="181eb-156">-SkuName</span></span>
<span data-ttu-id="181eb-157">A tárfiók termékváltozatnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="181eb-157">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="181eb-158">A rendelkezésre álló értékek a következő értékek: Standard_LRS, Premium_LRS, StandardSSD_LRS és UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="181eb-158">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="181eb-159">UltraSSD_LRS a CreateOption paraméterhez csak üres érték használható.</span><span class="sxs-lookup"><span data-stu-id="181eb-159">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="181eb-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="181eb-160">-Tag</span></span>
<span data-ttu-id="181eb-161">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="181eb-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="181eb-162">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="181eb-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="181eb-163">-Tier</span><span class="sxs-lookup"><span data-stu-id="181eb-163">-Tier</span></span>
<span data-ttu-id="181eb-164">A lemez teljesítményrétege.</span><span class="sxs-lookup"><span data-stu-id="181eb-164">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="181eb-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="181eb-165">-Confirm</span></span>
<span data-ttu-id="181eb-166">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="181eb-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="181eb-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="181eb-167">-WhatIf</span></span>
<span data-ttu-id="181eb-168">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="181eb-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="181eb-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="181eb-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="181eb-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181eb-170">CommonParameters</span></span>
<span data-ttu-id="181eb-171">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="181eb-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181eb-172">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="181eb-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181eb-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="181eb-173">INPUTS</span></span>

### <span data-ttu-id="181eb-174">System.String</span><span class="sxs-lookup"><span data-stu-id="181eb-174">System.String</span></span>

### <span data-ttu-id="181eb-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="181eb-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="181eb-176">System.Int32</span><span class="sxs-lookup"><span data-stu-id="181eb-176">System.Int32</span></span>

### <span data-ttu-id="181eb-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="181eb-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="181eb-178">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="181eb-178">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="181eb-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="181eb-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="181eb-180">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="181eb-180">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="181eb-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="181eb-181">OUTPUTS</span></span>

### <span data-ttu-id="181eb-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="181eb-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="181eb-183">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="181eb-183">NOTES</span></span>

## <span data-ttu-id="181eb-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="181eb-184">RELATED LINKS</span></span>
