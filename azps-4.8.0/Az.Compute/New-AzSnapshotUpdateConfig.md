---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 1a90a1ff260d143cf4df52ad160b4c05e781bd2e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025739"
---
# <span data-ttu-id="3b1fc-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="3b1fc-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="3b1fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b1fc-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1fc-103">Konfigurálható Snapshot Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="3b1fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b1fc-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b1fc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b1fc-105">DESCRIPTION</span></span>
<span data-ttu-id="3b1fc-106">A **New-AzSnapshotUpdateConfig** parancsmag egy konfigurálható Snapshot Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="3b1fc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3b1fc-107">EXAMPLES</span></span>

### <span data-ttu-id="3b1fc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3b1fc-108">Example 1</span></span>
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

<span data-ttu-id="3b1fc-109">Az első parancs létrehoz egy helyi üres Snapshot Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="3b1fc-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="3b1fc-111">A második és a harmadik parancs beállítja a merevlemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot Update objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="3b1fc-112">Az utolsó parancs átveszi a Snapshot Update objektumát, és frissíti a "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="3b1fc-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="3b1fc-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="3b1fc-114">Ez a parancs frissíti a meglévő, "Snapshot01" nevű pillanatképet a "ResourceGroup01" és a 10 GB méretű merevlemez között.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="3b1fc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b1fc-115">PARAMETERS</span></span>

### <span data-ttu-id="3b1fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b1fc-116">-DefaultProfile</span></span>
<span data-ttu-id="3b1fc-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b1fc-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3b1fc-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="3b1fc-119">A lemez titkosítási kulcs objektumát adja meg egy pillanatképen.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="3b1fc-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="3b1fc-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="3b1fc-121">A titkosításnak a REST szolgáltatáshoz való engedélyezéséhez használt titkosító erőforrás azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="3b1fc-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="3b1fc-122">-DiskSizeGB</span></span>
<span data-ttu-id="3b1fc-123">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="3b1fc-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="3b1fc-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="3b1fc-125">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="3b1fc-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="3b1fc-126">-EncryptionType</span></span>
<span data-ttu-id="3b1fc-127">A lemez adatainak titkosításához használt kulcs típusa.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="3b1fc-128">A rendelkezésre álló értékek a következők: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="3b1fc-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="3b1fc-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3b1fc-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="3b1fc-130">Egy pillanatkép kulcs titkosítási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="3b1fc-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="3b1fc-131">-OsType</span></span>
<span data-ttu-id="3b1fc-132">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="3b1fc-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3b1fc-133">-SkuName</span></span>
<span data-ttu-id="3b1fc-134">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="3b1fc-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="3b1fc-135">-Tag</span></span>
<span data-ttu-id="3b1fc-136">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3b1fc-137">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="3b1fc-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3b1fc-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b1fc-138">-Confirm</span></span>
<span data-ttu-id="3b1fc-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b1fc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b1fc-140">-WhatIf</span></span>
<span data-ttu-id="3b1fc-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b1fc-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b1fc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1fc-143">CommonParameters</span></span>
<span data-ttu-id="3b1fc-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b1fc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b1fc-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3b1fc-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1fc-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b1fc-146">INPUTS</span></span>

### <span data-ttu-id="3b1fc-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3b1fc-147">System.String</span></span>

### <span data-ttu-id="3b1fc-148">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3b1fc-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="3b1fc-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3b1fc-149">System.Int32</span></span>

### <span data-ttu-id="3b1fc-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3b1fc-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3b1fc-151">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3b1fc-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3b1fc-152">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="3b1fc-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="3b1fc-153">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="3b1fc-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="3b1fc-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b1fc-154">OUTPUTS</span></span>

### <span data-ttu-id="3b1fc-155">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="3b1fc-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="3b1fc-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b1fc-156">NOTES</span></span>

## <span data-ttu-id="3b1fc-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b1fc-157">RELATED LINKS</span></span>
