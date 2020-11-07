---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: c42aae31bb525f9da6a2963a945a6244373ac8db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667362"
---
# <span data-ttu-id="19b18-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="19b18-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="19b18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19b18-102">SYNOPSIS</span></span>
<span data-ttu-id="19b18-103">Konfigurálható pillanatkép-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="19b18-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="19b18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19b18-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19b18-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19b18-105">DESCRIPTION</span></span>
<span data-ttu-id="19b18-106">A **New-AzSnapshotConfig** parancsmag létrehoz egy konfigurálható pillanatkép-objektumot.</span><span class="sxs-lookup"><span data-stu-id="19b18-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="19b18-107">Példák</span><span class="sxs-lookup"><span data-stu-id="19b18-107">EXAMPLES</span></span>

### <span data-ttu-id="19b18-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19b18-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="19b18-109">Az első parancs létrehoz egy helyi üres pillanatkép-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="19b18-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="19b18-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="19b18-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="19b18-111">A második és a harmadik parancs beállítja a lemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="19b18-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="19b18-112">Az utolsó parancs átveszi a pillanatkép-objektumot, és egy "Snapshot01" nevű pillanatképet hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="19b18-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="19b18-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19b18-113">PARAMETERS</span></span>

### <span data-ttu-id="19b18-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="19b18-114">-CreateOption</span></span>
<span data-ttu-id="19b18-115">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="19b18-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="19b18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b18-116">-DefaultProfile</span></span>
<span data-ttu-id="19b18-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19b18-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19b18-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="19b18-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="19b18-119">A lemez titkosítási kulcs objektumát adja meg egy pillanatképen.</span><span class="sxs-lookup"><span data-stu-id="19b18-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="19b18-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="19b18-120">-DiskSizeGB</span></span>
<span data-ttu-id="19b18-121">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="19b18-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="19b18-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="19b18-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="19b18-123">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="19b18-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="19b18-124">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="19b18-124">-HyperVGeneration</span></span>
<span data-ttu-id="19b18-125">A virtuális gép hypervisor-generációja.</span><span class="sxs-lookup"><span data-stu-id="19b18-125">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="19b18-126">Csak az operációsrendszer-lemezekre érvényes.</span><span class="sxs-lookup"><span data-stu-id="19b18-126">Applicable to OS disks only.</span></span>  <span data-ttu-id="19b18-127">A megengedett értékek a v1 és a v2.</span><span class="sxs-lookup"><span data-stu-id="19b18-127">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="19b18-128">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="19b18-128">-ImageReference</span></span>
<span data-ttu-id="19b18-129">A kép hivatkozását adja meg egy pillanatképen.</span><span class="sxs-lookup"><span data-stu-id="19b18-129">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="19b18-130">-Növekményes</span><span class="sxs-lookup"><span data-stu-id="19b18-130">-Incremental</span></span>
<span data-ttu-id="19b18-131">Növekményes pillanatképet ad meg.</span><span class="sxs-lookup"><span data-stu-id="19b18-131">Specifies an incremental snapshot.</span></span> <span data-ttu-id="19b18-132">Ugyanannak a lemeznek a növekményes pillanatképei kevesebb helyet foglalnak el, mint a teljes Pillanatképek, és így lehet.</span><span class="sxs-lookup"><span data-stu-id="19b18-132">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

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

### <span data-ttu-id="19b18-133">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="19b18-133">-KeyEncryptionKey</span></span>
<span data-ttu-id="19b18-134">Egy pillanatkép kulcs titkosítási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="19b18-134">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="19b18-135">-Hely</span><span class="sxs-lookup"><span data-stu-id="19b18-135">-Location</span></span>
<span data-ttu-id="19b18-136">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="19b18-136">Specifies a location.</span></span>

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

### <span data-ttu-id="19b18-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="19b18-137">-OsType</span></span>
<span data-ttu-id="19b18-138">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="19b18-138">Specifies the OS type.</span></span>

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

### <span data-ttu-id="19b18-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="19b18-139">-SkuName</span></span>
<span data-ttu-id="19b18-140">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="19b18-140">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="19b18-141">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="19b18-141">-SourceResourceId</span></span>
<span data-ttu-id="19b18-142">A forrás erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19b18-142">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="19b18-143">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="19b18-143">-SourceUri</span></span>
<span data-ttu-id="19b18-144">A forrás URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19b18-144">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="19b18-145">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="19b18-145">-StorageAccountId</span></span>
<span data-ttu-id="19b18-146">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19b18-146">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="19b18-147">-Címke</span><span class="sxs-lookup"><span data-stu-id="19b18-147">-Tag</span></span>
<span data-ttu-id="19b18-148">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="19b18-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="19b18-149">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="19b18-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="19b18-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="19b18-150">-Confirm</span></span>
<span data-ttu-id="19b18-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19b18-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19b18-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19b18-152">-WhatIf</span></span>
<span data-ttu-id="19b18-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="19b18-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19b18-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19b18-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19b18-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b18-155">CommonParameters</span></span>
<span data-ttu-id="19b18-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19b18-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b18-157">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="19b18-157">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b18-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19b18-158">INPUTS</span></span>

### <span data-ttu-id="19b18-159">System. String</span><span class="sxs-lookup"><span data-stu-id="19b18-159">System.String</span></span>

### <span data-ttu-id="19b18-160">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="19b18-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="19b18-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="19b18-161">System.Int32</span></span>

### <span data-ttu-id="19b18-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="19b18-162">System.Collections.Hashtable</span></span>

### <span data-ttu-id="19b18-163">Microsoft. Azure. Management. kiszámítás. models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="19b18-163">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="19b18-164">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="19b18-164">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="19b18-165">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="19b18-165">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="19b18-166">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="19b18-166">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="19b18-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19b18-167">OUTPUTS</span></span>

### <span data-ttu-id="19b18-168">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="19b18-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="19b18-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19b18-169">NOTES</span></span>

## <span data-ttu-id="19b18-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19b18-170">RELATED LINKS</span></span>
