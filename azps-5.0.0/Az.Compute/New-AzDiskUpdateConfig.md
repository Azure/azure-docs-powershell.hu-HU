---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: a738ec606fc982573c4062879e9da4becee43df2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186244"
---
# <span data-ttu-id="1dffa-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="1dffa-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="1dffa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1dffa-102">SYNOPSIS</span></span>
<span data-ttu-id="1dffa-103">Konfigurálható Disk Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1dffa-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="1dffa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1dffa-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dffa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1dffa-105">DESCRIPTION</span></span>
<span data-ttu-id="1dffa-106">A **New-AzDiskUpdateConfig** parancsmag egy konfigurálható Disk Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1dffa-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="1dffa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1dffa-107">EXAMPLES</span></span>

### <span data-ttu-id="1dffa-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1dffa-108">Example 1</span></span>
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

<span data-ttu-id="1dffa-109">Az első parancs létrehoz egy helyi üres Disk Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="1dffa-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="1dffa-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="1dffa-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="1dffa-111">A második és a harmadik parancs a Disk Update objektum merevlemez-titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="1dffa-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="1dffa-112">Az utolsó parancs átveszi a Disk Update objektumot, és frissíti a meglévő, "Disk01" nevű lemezt az erőforráscsoport "ResourceGroup01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="1dffa-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1dffa-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="1dffa-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="1dffa-114">Ez a parancs frissíti a "Disk01" nevű, a "ResourceGroup01" nevű, 10 GB-nyi méretű kötetet használó meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="1dffa-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="1dffa-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1dffa-115">PARAMETERS</span></span>

### <span data-ttu-id="1dffa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dffa-116">-DefaultProfile</span></span>
<span data-ttu-id="1dffa-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1dffa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dffa-118">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="1dffa-118">-DiskAccessId</span></span>
<span data-ttu-id="1dffa-119">{{Fill DiskAccessId Description}}</span><span class="sxs-lookup"><span data-stu-id="1dffa-119">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="1dffa-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1dffa-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="1dffa-121">A lemez titkosítási kulcs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1dffa-121">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="1dffa-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="1dffa-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="1dffa-123">A titkosításnak a REST szolgáltatáshoz való engedélyezéséhez használt titkosító erőforrás azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1dffa-123">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="1dffa-124">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="1dffa-124">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="1dffa-125">Annak a IOPS a teljes száma, amelyet az összes VMs-meghajtón meg kell adni az írásvédett példányban.</span><span class="sxs-lookup"><span data-stu-id="1dffa-125">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="1dffa-126">Egy művelet átadható a 4k és a 256k között.</span><span class="sxs-lookup"><span data-stu-id="1dffa-126">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="1dffa-127">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="1dffa-127">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="1dffa-128">A lemezre engedélyezett IOPS száma; csak a UltraSSD-lemezek állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="1dffa-128">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="1dffa-129">Egy művelet átadható a 4k és a 256k között.</span><span class="sxs-lookup"><span data-stu-id="1dffa-129">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="1dffa-130">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="1dffa-130">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="1dffa-131">A teljes átviteli sebesség (Mbit/s), amelyet a rendszer minden VMs-meghajtón a megosztott merevlemez írásvédett módú csatlakoztatásakor megenged.</span><span class="sxs-lookup"><span data-stu-id="1dffa-131">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="1dffa-132">MBps: a 10 MB/s sebességű bájtok száma itt az ISO-jelölést használja, a 10-es hatáskörökkel.</span><span class="sxs-lookup"><span data-stu-id="1dffa-132">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="1dffa-133">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="1dffa-133">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="1dffa-134">A lemezre engedélyezett sávszélesség; csak a UltraSSD-lemezek állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="1dffa-134">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="1dffa-135">MBps: a 10 MB/s sebességű bájtok száma itt az ISO-jelölést használja, a 10-es hatáskörökkel.</span><span class="sxs-lookup"><span data-stu-id="1dffa-135">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="1dffa-136">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="1dffa-136">-DiskSizeGB</span></span>
<span data-ttu-id="1dffa-137">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="1dffa-137">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="1dffa-138">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="1dffa-138">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="1dffa-139">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="1dffa-139">Enable encryption settings.</span></span>

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

### <span data-ttu-id="1dffa-140">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="1dffa-140">-EncryptionType</span></span>
<span data-ttu-id="1dffa-141">A lemez adatainak titkosításához használt kulcs típusa.</span><span class="sxs-lookup"><span data-stu-id="1dffa-141">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="1dffa-142">A rendelkezésre álló értékek a következők: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="1dffa-142">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="1dffa-143">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1dffa-143">-KeyEncryptionKey</span></span>
<span data-ttu-id="1dffa-144">A kulcs titkosítási kulcsát adja meg a lemezen.</span><span class="sxs-lookup"><span data-stu-id="1dffa-144">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="1dffa-145">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="1dffa-145">-MaxSharesCount</span></span>
<span data-ttu-id="1dffa-146">A merevlemezhez egyidejűleg használható VMs-tartomány maximális száma.</span><span class="sxs-lookup"><span data-stu-id="1dffa-146">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="1dffa-147">Az értéknél nagyobb érték azt jelzi, hogy egyszerre több VMs-eszközön lehet csatlakoztatni egy lemezt.</span><span class="sxs-lookup"><span data-stu-id="1dffa-147">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="1dffa-148">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1dffa-148">-NetworkAccessPolicy</span></span>
<span data-ttu-id="1dffa-149">{{Fill NetworkAccessPolicy Description}}</span><span class="sxs-lookup"><span data-stu-id="1dffa-149">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="1dffa-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="1dffa-150">-OsType</span></span>
<span data-ttu-id="1dffa-151">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1dffa-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="1dffa-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1dffa-152">-SkuName</span></span>
<span data-ttu-id="1dffa-153">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="1dffa-153">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="1dffa-154">A rendelkezésre álló értékek az Standard_LRS, a Premium_LRS, a StandardSSD_LRS és a UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="1dffa-154">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="1dffa-155">A UltraSSD_LRS csak a CreateOption paraméter üres értékével használható.</span><span class="sxs-lookup"><span data-stu-id="1dffa-155">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="1dffa-156">-Címke</span><span class="sxs-lookup"><span data-stu-id="1dffa-156">-Tag</span></span>
<span data-ttu-id="1dffa-157">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="1dffa-157">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1dffa-158">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="1dffa-158">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1dffa-159">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="1dffa-159">-Tier</span></span>
<span data-ttu-id="1dffa-160">A lemez teljesítőképességi szintje.</span><span class="sxs-lookup"><span data-stu-id="1dffa-160">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="1dffa-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1dffa-161">-Confirm</span></span>
<span data-ttu-id="1dffa-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1dffa-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dffa-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dffa-163">-WhatIf</span></span>
<span data-ttu-id="1dffa-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1dffa-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dffa-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1dffa-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dffa-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dffa-166">CommonParameters</span></span>
<span data-ttu-id="1dffa-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1dffa-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dffa-168">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1dffa-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dffa-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1dffa-169">INPUTS</span></span>

### <span data-ttu-id="1dffa-170">System. String</span><span class="sxs-lookup"><span data-stu-id="1dffa-170">System.String</span></span>

### <span data-ttu-id="1dffa-171">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1dffa-171">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1dffa-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1dffa-172">System.Int32</span></span>

### <span data-ttu-id="1dffa-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1dffa-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1dffa-174">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1dffa-174">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1dffa-175">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="1dffa-175">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="1dffa-176">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="1dffa-176">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="1dffa-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1dffa-177">OUTPUTS</span></span>

### <span data-ttu-id="1dffa-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="1dffa-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="1dffa-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1dffa-179">NOTES</span></span>

## <span data-ttu-id="1dffa-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1dffa-180">RELATED LINKS</span></span>
