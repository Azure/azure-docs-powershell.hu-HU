---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 5d9a48fbdc323ffdd232d6d961da6564fecc0dff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301523"
---
# <span data-ttu-id="95999-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="95999-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="95999-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95999-102">SYNOPSIS</span></span>
<span data-ttu-id="95999-103">Konfigurálható pillanatkép-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="95999-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="95999-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95999-104">SYNTAX</span></span>

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

## <span data-ttu-id="95999-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="95999-105">DESCRIPTION</span></span>
<span data-ttu-id="95999-106">A **New-AzSnapshotConfig** parancsmag létrehoz egy konfigurálható pillanatkép-objektumot.</span><span class="sxs-lookup"><span data-stu-id="95999-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="95999-107">Példák</span><span class="sxs-lookup"><span data-stu-id="95999-107">EXAMPLES</span></span>

### <span data-ttu-id="95999-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="95999-108">Example 1</span></span>
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

<span data-ttu-id="95999-109">Az első parancs létrehoz egy helyi üres pillanatkép-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="95999-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="95999-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="95999-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="95999-111">A második és a harmadik parancs beállítja a lemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="95999-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="95999-112">Az utolsó parancs átveszi a pillanatkép-objektumot, és egy "Snapshot01" nevű pillanatképet hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="95999-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="95999-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="95999-113">Example 2</span></span>

<span data-ttu-id="95999-114">Konfigurálható pillanatkép-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="95999-114">Creates a configurable snapshot object.</span></span> <span data-ttu-id="95999-115">autogenerated</span><span class="sxs-lookup"><span data-stu-id="95999-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzSnapshotConfig -CreateOption Empty -Location 'Central US' -SourceUri 'https://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd'
```

## <span data-ttu-id="95999-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95999-116">PARAMETERS</span></span>

### <span data-ttu-id="95999-117">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="95999-117">-CreateOption</span></span>
<span data-ttu-id="95999-118">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="95999-118">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="95999-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95999-119">-DefaultProfile</span></span>
<span data-ttu-id="95999-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95999-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95999-121">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="95999-121">-DiskEncryptionKey</span></span>
<span data-ttu-id="95999-122">A lemez titkosítási kulcs objektumát adja meg egy pillanatképen.</span><span class="sxs-lookup"><span data-stu-id="95999-122">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="95999-123">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="95999-123">-DiskEncryptionSetId</span></span>
<span data-ttu-id="95999-124">A titkosításnak a REST szolgáltatáshoz való engedélyezéséhez használt titkosító erőforrás azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="95999-124">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="95999-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="95999-125">-DiskSizeGB</span></span>
<span data-ttu-id="95999-126">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="95999-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="95999-127">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="95999-127">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="95999-128">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="95999-128">Enable encryption settings.</span></span>

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

### <span data-ttu-id="95999-129">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="95999-129">-EncryptionType</span></span>
<span data-ttu-id="95999-130">A lemez adatainak titkosításához használt kulcs típusa.</span><span class="sxs-lookup"><span data-stu-id="95999-130">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="95999-131">A rendelkezésre álló értékek a következők: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="95999-131">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="95999-132">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="95999-132">-DiskAccessId</span></span>
<span data-ttu-id="95999-133">Beolvassa vagy beállítja a DiskAccess-erőforrás ARM azonosítóját a privát végpontok beállításához.</span><span class="sxs-lookup"><span data-stu-id="95999-133">Gets or sets ARM id of the DiskAccess resource for using private endpoints on.</span></span>

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

### <span data-ttu-id="95999-134">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="95999-134">-NetworkAccessPolicy</span></span>
<span data-ttu-id="95999-135">A hálózat-hozzáférési házirend a hálózat-hozzáférési házirendet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="95999-135">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="95999-136">A lehetséges értékek a következők: "AllowAll", "AllowPrivate", "DenyAll"</span><span class="sxs-lookup"><span data-stu-id="95999-136">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="95999-137">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="95999-137">-HyperVGeneration</span></span>
<span data-ttu-id="95999-138">A virtuális gép hypervisor-generációja.</span><span class="sxs-lookup"><span data-stu-id="95999-138">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="95999-139">Csak az operációsrendszer-lemezekre érvényes.</span><span class="sxs-lookup"><span data-stu-id="95999-139">Applicable to OS disks only.</span></span>  <span data-ttu-id="95999-140">A megengedett értékek a v1 és a v2.</span><span class="sxs-lookup"><span data-stu-id="95999-140">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="95999-141">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="95999-141">-ImageReference</span></span>
<span data-ttu-id="95999-142">A kép hivatkozását adja meg egy pillanatképen.</span><span class="sxs-lookup"><span data-stu-id="95999-142">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="95999-143">-Növekményes</span><span class="sxs-lookup"><span data-stu-id="95999-143">-Incremental</span></span>
<span data-ttu-id="95999-144">Növekményes pillanatképet ad meg.</span><span class="sxs-lookup"><span data-stu-id="95999-144">Specifies an incremental snapshot.</span></span> <span data-ttu-id="95999-145">Ugyanannak a lemeznek a növekményes pillanatképei kevesebb helyet foglalnak el, mint a teljes Pillanatképek, és így lehet.</span><span class="sxs-lookup"><span data-stu-id="95999-145">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

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

### <span data-ttu-id="95999-146">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="95999-146">-KeyEncryptionKey</span></span>
<span data-ttu-id="95999-147">Egy pillanatkép kulcs titkosítási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="95999-147">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="95999-148">-Hely</span><span class="sxs-lookup"><span data-stu-id="95999-148">-Location</span></span>
<span data-ttu-id="95999-149">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="95999-149">Specifies a location.</span></span>

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

### <span data-ttu-id="95999-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="95999-150">-OsType</span></span>
<span data-ttu-id="95999-151">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="95999-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="95999-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="95999-152">-SkuName</span></span>
<span data-ttu-id="95999-153">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="95999-153">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="95999-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="95999-154">-SourceResourceId</span></span>
<span data-ttu-id="95999-155">A forrás erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="95999-155">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="95999-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="95999-156">-SourceUri</span></span>
<span data-ttu-id="95999-157">A forrás URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="95999-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="95999-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="95999-158">-StorageAccountId</span></span>
<span data-ttu-id="95999-159">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="95999-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="95999-160">-Címke</span><span class="sxs-lookup"><span data-stu-id="95999-160">-Tag</span></span>
<span data-ttu-id="95999-161">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="95999-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="95999-162">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="95999-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="95999-163">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="95999-163">-Confirm</span></span>
<span data-ttu-id="95999-164">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="95999-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95999-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95999-165">-WhatIf</span></span>
<span data-ttu-id="95999-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="95999-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95999-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="95999-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95999-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95999-168">CommonParameters</span></span>
<span data-ttu-id="95999-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95999-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95999-170">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="95999-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95999-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95999-171">INPUTS</span></span>

### <span data-ttu-id="95999-172">System. String</span><span class="sxs-lookup"><span data-stu-id="95999-172">System.String</span></span>

### <span data-ttu-id="95999-173">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="95999-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="95999-174">System. Int32</span><span class="sxs-lookup"><span data-stu-id="95999-174">System.Int32</span></span>

### <span data-ttu-id="95999-175">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="95999-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="95999-176">Microsoft. Azure. Management. kiszámítás. models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="95999-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="95999-177">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="95999-177">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="95999-178">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="95999-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="95999-179">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="95999-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="95999-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95999-180">OUTPUTS</span></span>

### <span data-ttu-id="95999-181">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="95999-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="95999-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95999-182">NOTES</span></span>

## <span data-ttu-id="95999-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95999-183">RELATED LINKS</span></span>
