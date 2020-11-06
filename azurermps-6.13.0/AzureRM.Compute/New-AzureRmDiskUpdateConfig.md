---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
ms.openlocfilehash: 1aee03af5a326585f9578a2f3eef378c3b783431
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504496"
---
# <span data-ttu-id="618a6-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="618a6-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="618a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="618a6-102">SYNOPSIS</span></span>
<span data-ttu-id="618a6-103">Konfigurálható Disk Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="618a6-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="618a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="618a6-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="618a6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="618a6-105">DESCRIPTION</span></span>
<span data-ttu-id="618a6-106">A **New-AzureRmDiskUpdateConfig** parancsmag egy konfigurálható Disk Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="618a6-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="618a6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="618a6-107">EXAMPLES</span></span>

### <span data-ttu-id="618a6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="618a6-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="618a6-109">Az első parancs létrehoz egy helyi üres Disk Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="618a6-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="618a6-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="618a6-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="618a6-111">A második és a harmadik parancs a Disk Update objektum merevlemez-titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="618a6-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="618a6-112">Az utolsó parancs átveszi a Disk Update objektumot, és frissíti a meglévő, "Disk01" nevű lemezt az erőforráscsoport "ResourceGroup01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="618a6-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="618a6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="618a6-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="618a6-114">Ez a parancs frissíti a "Disk01" nevű, a "ResourceGroup01" nevű, 10 GB-nyi méretű kötetet használó meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="618a6-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="618a6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="618a6-115">PARAMETERS</span></span>

### <span data-ttu-id="618a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="618a6-116">-DefaultProfile</span></span>
<span data-ttu-id="618a6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="618a6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="618a6-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="618a6-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="618a6-119">A lemez titkosítási kulcs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="618a6-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="618a6-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="618a6-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="618a6-121">A lemezre engedélyezett IOPS száma; csak a UltraSSD-lemezek állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="618a6-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="618a6-122">Egy művelet átadható a 4k és a 256k között.</span><span class="sxs-lookup"><span data-stu-id="618a6-122">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="618a6-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="618a6-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="618a6-124">A lemezre engedélyezett sávszélesség; csak a UltraSSD-lemezek állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="618a6-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="618a6-125">MBps: a 10 MB/s sebességű bájtok száma itt az ISO-jelölést használja, a 10-es hatáskörökkel.</span><span class="sxs-lookup"><span data-stu-id="618a6-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="618a6-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="618a6-126">-DiskSizeGB</span></span>
<span data-ttu-id="618a6-127">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="618a6-127">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="618a6-128">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="618a6-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="618a6-129">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="618a6-129">Enable encryption settings.</span></span>

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

### <span data-ttu-id="618a6-130">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="618a6-130">-KeyEncryptionKey</span></span>
<span data-ttu-id="618a6-131">A kulcs titkosítási kulcsát adja meg a lemezen.</span><span class="sxs-lookup"><span data-stu-id="618a6-131">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="618a6-132">-OsType</span><span class="sxs-lookup"><span data-stu-id="618a6-132">-OsType</span></span>
<span data-ttu-id="618a6-133">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="618a6-133">Specifies the OS type.</span></span>

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

### <span data-ttu-id="618a6-134">-SkuName</span><span class="sxs-lookup"><span data-stu-id="618a6-134">-SkuName</span></span>
<span data-ttu-id="618a6-135">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="618a6-135">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="618a6-136">A rendelkezésre álló értékek az Standard_LRS, a Premium_LRS, a StandardSSD_LRS és a UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="618a6-136">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="618a6-137">A UltraSSD_LRS csak a CreateOption paraméter üres értékével használható.</span><span class="sxs-lookup"><span data-stu-id="618a6-137">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="618a6-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="618a6-138">-Tag</span></span>
<span data-ttu-id="618a6-139">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="618a6-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="618a6-140">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="618a6-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="618a6-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="618a6-141">-Confirm</span></span>
<span data-ttu-id="618a6-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="618a6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="618a6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="618a6-143">-WhatIf</span></span>
<span data-ttu-id="618a6-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="618a6-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="618a6-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="618a6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="618a6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="618a6-146">CommonParameters</span></span>
<span data-ttu-id="618a6-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="618a6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="618a6-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="618a6-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="618a6-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="618a6-149">INPUTS</span></span>

### <span data-ttu-id="618a6-150">System. String</span><span class="sxs-lookup"><span data-stu-id="618a6-150">System.String</span></span>

### <span data-ttu-id="618a6-151">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes, Microsoft. Azure. Management. kiszámítás, Version = 21.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="618a6-151">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="618a6-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="618a6-152">System.Int32</span></span>

### <span data-ttu-id="618a6-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="618a6-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="618a6-154">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="618a6-154">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="618a6-155">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="618a6-155">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="618a6-156">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="618a6-156">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="618a6-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="618a6-157">OUTPUTS</span></span>

### <span data-ttu-id="618a6-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="618a6-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="618a6-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="618a6-159">NOTES</span></span>

## <span data-ttu-id="618a6-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="618a6-160">RELATED LINKS</span></span>