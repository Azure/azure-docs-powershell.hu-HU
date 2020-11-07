---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: c2c17fe3329170d65d61e5439e614717a8119f26
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844481"
---
# <span data-ttu-id="00dd5-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="00dd5-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="00dd5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="00dd5-103">Konfigurálható Snapshot Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="00dd5-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="00dd5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00dd5-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00dd5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="00dd5-105">DESCRIPTION</span></span>
<span data-ttu-id="00dd5-106">A **New-AzSnapshotUpdateConfig** parancsmag egy konfigurálható Snapshot Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="00dd5-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="00dd5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="00dd5-107">EXAMPLES</span></span>

### <span data-ttu-id="00dd5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="00dd5-108">Example 1</span></span>
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

<span data-ttu-id="00dd5-109">Az első parancs létrehoz egy helyi üres Snapshot Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="00dd5-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="00dd5-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="00dd5-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="00dd5-111">A második és a harmadik parancs beállítja a merevlemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot Update objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="00dd5-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="00dd5-112">Az utolsó parancs átveszi a Snapshot Update objektumát, és frissíti a "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="00dd5-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="00dd5-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="00dd5-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="00dd5-114">Ez a parancs frissíti a meglévő, "Snapshot01" nevű pillanatképet a "ResourceGroup01" és a 10 GB méretű merevlemez között.</span><span class="sxs-lookup"><span data-stu-id="00dd5-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="00dd5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00dd5-115">PARAMETERS</span></span>

### <span data-ttu-id="00dd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00dd5-116">-DefaultProfile</span></span>
<span data-ttu-id="00dd5-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00dd5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dd5-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="00dd5-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="00dd5-119">A lemez titkosítási kulcs objektumát adja meg egy pillanatképen.</span><span class="sxs-lookup"><span data-stu-id="00dd5-119">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00dd5-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="00dd5-120">-DiskSizeGB</span></span>
<span data-ttu-id="00dd5-121">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="00dd5-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00dd5-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="00dd5-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="00dd5-123">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="00dd5-123">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00dd5-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="00dd5-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="00dd5-125">Egy pillanatkép kulcs titkosítási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="00dd5-125">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00dd5-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="00dd5-126">-OsType</span></span>
<span data-ttu-id="00dd5-127">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="00dd5-127">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00dd5-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="00dd5-128">-SkuName</span></span>
<span data-ttu-id="00dd5-129">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="00dd5-129">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00dd5-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="00dd5-130">-Tag</span></span>
<span data-ttu-id="00dd5-131">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="00dd5-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="00dd5-132">Példa:</span><span class="sxs-lookup"><span data-stu-id="00dd5-132">For example:</span></span>

<span data-ttu-id="00dd5-133">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="00dd5-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00dd5-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="00dd5-134">-Confirm</span></span>
<span data-ttu-id="00dd5-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="00dd5-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dd5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00dd5-136">-WhatIf</span></span>
<span data-ttu-id="00dd5-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="00dd5-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00dd5-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00dd5-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dd5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00dd5-139">CommonParameters</span></span>
<span data-ttu-id="00dd5-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00dd5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00dd5-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00dd5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00dd5-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00dd5-142">INPUTS</span></span>

### <span data-ttu-id="00dd5-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="00dd5-143">None</span></span>
<span data-ttu-id="00dd5-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="00dd5-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00dd5-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00dd5-145">OUTPUTS</span></span>

### <span data-ttu-id="00dd5-146">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="00dd5-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="00dd5-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00dd5-147">NOTES</span></span>

## <span data-ttu-id="00dd5-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00dd5-148">RELATED LINKS</span></span>

