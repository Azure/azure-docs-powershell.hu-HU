---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
ms.openlocfilehash: ff70d3879685b0cdc9fcc42732a68e6b85bbd580
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492338"
---
# <span data-ttu-id="d457c-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="d457c-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="d457c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d457c-102">SYNOPSIS</span></span>
<span data-ttu-id="d457c-103">Pillanatképek frissítése</span><span class="sxs-lookup"><span data-stu-id="d457c-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d457c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d457c-104">SYNTAX</span></span>

### <span data-ttu-id="d457c-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d457c-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <SnapshotUpdate> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d457c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d457c-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <Snapshot> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d457c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d457c-107">DESCRIPTION</span></span>
<span data-ttu-id="d457c-108">Az **Update-AzureRmSnapshot** parancsmag frissíti a pillanatképet.</span><span class="sxs-lookup"><span data-stu-id="d457c-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="d457c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d457c-109">EXAMPLES</span></span>

### <span data-ttu-id="d457c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d457c-110">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="d457c-111">Az első parancs létrehoz egy helyi üres Snapshot Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="d457c-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d457c-112">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="d457c-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d457c-113">A második és a harmadik parancs beállítja a merevlemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot Update objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="d457c-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="d457c-114">Az utolsó parancs átveszi a Snapshot Update objektumát, és frissíti a "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="d457c-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d457c-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="d457c-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="d457c-116">Ez a parancs frissíti a meglévő, "Snapshot01" nevű pillanatképet a "ResourceGroup01" és a 10 GB méretű merevlemez között.</span><span class="sxs-lookup"><span data-stu-id="d457c-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="d457c-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="d457c-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="d457c-118">Ezek a parancsok frissítik a meglévő, "Snapshot01" nevű pillanatképet a "ResourceGroup01" és a 10 GB méretű merevlemezek között.</span><span class="sxs-lookup"><span data-stu-id="d457c-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="d457c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d457c-119">PARAMETERS</span></span>

### <span data-ttu-id="d457c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d457c-120">-ResourceGroupName</span></span>
<span data-ttu-id="d457c-121">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d457c-121">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d457c-122">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="d457c-122">-Snapshot</span></span>
<span data-ttu-id="d457c-123">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d457c-123">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d457c-124">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="d457c-124">-SnapshotName</span></span>
<span data-ttu-id="d457c-125">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d457c-125">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d457c-126">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d457c-126">-SnapshotUpdate</span></span>
<span data-ttu-id="d457c-127">Egy helyi Snapshot Update-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d457c-127">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d457c-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d457c-128">-Confirm</span></span>
<span data-ttu-id="d457c-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d457c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d457c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d457c-130">-WhatIf</span></span>
<span data-ttu-id="d457c-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d457c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d457c-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d457c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d457c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d457c-133">CommonParameters</span></span>
<span data-ttu-id="d457c-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d457c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d457c-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d457c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d457c-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d457c-136">INPUTS</span></span>

### <span data-ttu-id="d457c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d457c-137">System.String</span></span>
<span data-ttu-id="d457c-138">Microsoft. Azure. Management. számítás. models. SnapshotUpdate Microsoft. Azure. Management. kiszámítás. models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="d457c-138">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="d457c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d457c-139">OUTPUTS</span></span>

### <span data-ttu-id="d457c-140">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="d457c-140">System.Object</span></span>

## <span data-ttu-id="d457c-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d457c-141">NOTES</span></span>

## <span data-ttu-id="d457c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d457c-142">RELATED LINKS</span></span>

