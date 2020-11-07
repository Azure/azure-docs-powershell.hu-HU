---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 293e894704509fe1b869ca23bd726c49f400de48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671309"
---
# <span data-ttu-id="643f6-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="643f6-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="643f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="643f6-102">SYNOPSIS</span></span>
<span data-ttu-id="643f6-103">Konfigurálható pillanatkép-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="643f6-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="643f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="643f6-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="643f6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="643f6-105">DESCRIPTION</span></span>
<span data-ttu-id="643f6-106">A **New-AzSnapshotConfig** parancsmag létrehoz egy konfigurálható pillanatkép-objektumot.</span><span class="sxs-lookup"><span data-stu-id="643f6-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="643f6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="643f6-107">EXAMPLES</span></span>

### <span data-ttu-id="643f6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="643f6-108">Example 1</span></span>
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

<span data-ttu-id="643f6-109">Az első parancs létrehoz egy helyi üres pillanatkép-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="643f6-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="643f6-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="643f6-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="643f6-111">A második és a harmadik parancs beállítja a lemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="643f6-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="643f6-112">Az utolsó parancs átveszi a pillanatkép-objektumot, és egy "Snapshot01" nevű pillanatképet hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="643f6-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="643f6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="643f6-113">PARAMETERS</span></span>

### <span data-ttu-id="643f6-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="643f6-114">-CreateOption</span></span>
<span data-ttu-id="643f6-115">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="643f6-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="643f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="643f6-116">-DefaultProfile</span></span>
<span data-ttu-id="643f6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="643f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="643f6-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="643f6-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="643f6-119">A lemez titkosítási kulcs objektumát adja meg egy pillanatképen.</span><span class="sxs-lookup"><span data-stu-id="643f6-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="643f6-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="643f6-120">-DiskSizeGB</span></span>
<span data-ttu-id="643f6-121">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="643f6-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="643f6-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="643f6-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="643f6-123">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="643f6-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="643f6-124">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="643f6-124">-HyperVGeneration</span></span>
<span data-ttu-id="643f6-125">A virtuális gép hypervisor-generációja.</span><span class="sxs-lookup"><span data-stu-id="643f6-125">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="643f6-126">Csak az operációsrendszer-lemezekre érvényes.</span><span class="sxs-lookup"><span data-stu-id="643f6-126">Applicable to OS disks only.</span></span>  <span data-ttu-id="643f6-127">A megengedett értékek a v1 és a v2.</span><span class="sxs-lookup"><span data-stu-id="643f6-127">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="643f6-128">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="643f6-128">-ImageReference</span></span>
<span data-ttu-id="643f6-129">A kép hivatkozását adja meg egy pillanatképen.</span><span class="sxs-lookup"><span data-stu-id="643f6-129">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="643f6-130">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="643f6-130">-KeyEncryptionKey</span></span>
<span data-ttu-id="643f6-131">Egy pillanatkép kulcs titkosítási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="643f6-131">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="643f6-132">-Hely</span><span class="sxs-lookup"><span data-stu-id="643f6-132">-Location</span></span>
<span data-ttu-id="643f6-133">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="643f6-133">Specifies a location.</span></span>

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

### <span data-ttu-id="643f6-134">-OsType</span><span class="sxs-lookup"><span data-stu-id="643f6-134">-OsType</span></span>
<span data-ttu-id="643f6-135">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="643f6-135">Specifies the OS type.</span></span>

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

### <span data-ttu-id="643f6-136">-SkuName</span><span class="sxs-lookup"><span data-stu-id="643f6-136">-SkuName</span></span>
<span data-ttu-id="643f6-137">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="643f6-137">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="643f6-138">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="643f6-138">-SourceResourceId</span></span>
<span data-ttu-id="643f6-139">A forrás erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="643f6-139">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="643f6-140">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="643f6-140">-SourceUri</span></span>
<span data-ttu-id="643f6-141">A forrás URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="643f6-141">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="643f6-142">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="643f6-142">-StorageAccountId</span></span>
<span data-ttu-id="643f6-143">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="643f6-143">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="643f6-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="643f6-144">-Tag</span></span>
<span data-ttu-id="643f6-145">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="643f6-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="643f6-146">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="643f6-146">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="643f6-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="643f6-147">-Confirm</span></span>
<span data-ttu-id="643f6-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="643f6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="643f6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="643f6-149">-WhatIf</span></span>
<span data-ttu-id="643f6-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="643f6-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="643f6-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="643f6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="643f6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643f6-152">CommonParameters</span></span>
<span data-ttu-id="643f6-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="643f6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="643f6-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="643f6-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643f6-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="643f6-155">INPUTS</span></span>

### <span data-ttu-id="643f6-156">System. String</span><span class="sxs-lookup"><span data-stu-id="643f6-156">System.String</span></span>

### <span data-ttu-id="643f6-157">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="643f6-157">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="643f6-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="643f6-158">System.Int32</span></span>

### <span data-ttu-id="643f6-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="643f6-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="643f6-160">Microsoft. Azure. Management. kiszámítás. models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="643f6-160">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="643f6-161">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="643f6-161">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="643f6-162">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="643f6-162">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="643f6-163">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="643f6-163">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="643f6-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="643f6-164">OUTPUTS</span></span>

### <span data-ttu-id="643f6-165">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="643f6-165">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="643f6-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="643f6-166">NOTES</span></span>

## <span data-ttu-id="643f6-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="643f6-167">RELATED LINKS</span></span>
