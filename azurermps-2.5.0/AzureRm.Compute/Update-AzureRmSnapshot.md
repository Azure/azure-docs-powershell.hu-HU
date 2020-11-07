---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: 2e8b538e9a6f5f9fce2fb768bc0c77d0c82c55f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850861"
---
# <span data-ttu-id="d22f1-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="d22f1-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="d22f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d22f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d22f1-103">Pillanatképek frissítése</span><span class="sxs-lookup"><span data-stu-id="d22f1-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d22f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d22f1-104">SYNTAX</span></span>

### <span data-ttu-id="d22f1-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d22f1-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <PSSnapshotUpdate> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d22f1-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d22f1-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d22f1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d22f1-107">DESCRIPTION</span></span>
<span data-ttu-id="d22f1-108">Az **Update-AzureRmSnapshot** parancsmag frissíti a pillanatképet.</span><span class="sxs-lookup"><span data-stu-id="d22f1-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="d22f1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d22f1-109">EXAMPLES</span></span>

### <span data-ttu-id="d22f1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d22f1-110">Example 1</span></span>
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

<span data-ttu-id="d22f1-111">Az első parancs létrehoz egy helyi üres Snapshot Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="d22f1-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d22f1-112">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="d22f1-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d22f1-113">A második és a harmadik parancs beállítja a merevlemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot Update objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="d22f1-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="d22f1-114">Az utolsó parancs átveszi a Snapshot Update objektumát, és frissíti a "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="d22f1-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d22f1-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="d22f1-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="d22f1-116">Ez a parancs frissíti a meglévő, "Snapshot01" nevű pillanatképet a "ResourceGroup01" és a 10 GB méretű merevlemez között.</span><span class="sxs-lookup"><span data-stu-id="d22f1-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="d22f1-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="d22f1-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="d22f1-118">Ezek a parancsok frissítik a meglévő, "Snapshot01" nevű pillanatképet a "ResourceGroup01" és a 10 GB méretű merevlemezek között.</span><span class="sxs-lookup"><span data-stu-id="d22f1-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="d22f1-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d22f1-119">PARAMETERS</span></span>

### <span data-ttu-id="d22f1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d22f1-120">-AsJob</span></span>
<span data-ttu-id="d22f1-121">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="d22f1-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22f1-122">-DefaultProfile</span></span>
<span data-ttu-id="d22f1-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d22f1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d22f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d22f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="d22f1-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d22f1-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d22f1-126">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="d22f1-126">-Snapshot</span></span>
<span data-ttu-id="d22f1-127">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d22f1-127">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d22f1-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="d22f1-128">-SnapshotName</span></span>
<span data-ttu-id="d22f1-129">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d22f1-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="d22f1-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d22f1-130">-SnapshotUpdate</span></span>
<span data-ttu-id="d22f1-131">Egy helyi Snapshot Update-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d22f1-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d22f1-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d22f1-132">-Confirm</span></span>
<span data-ttu-id="d22f1-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d22f1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d22f1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d22f1-134">-WhatIf</span></span>
<span data-ttu-id="d22f1-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d22f1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d22f1-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d22f1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d22f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22f1-137">CommonParameters</span></span>
<span data-ttu-id="d22f1-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d22f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22f1-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d22f1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22f1-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d22f1-140">INPUTS</span></span>

### <span data-ttu-id="d22f1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d22f1-141">System.String</span></span>
<span data-ttu-id="d22f1-142">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshotUpdate Microsoft. Azure. commands. kiszámítás. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="d22f1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="d22f1-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d22f1-143">OUTPUTS</span></span>

### <span data-ttu-id="d22f1-144">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="d22f1-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="d22f1-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d22f1-145">NOTES</span></span>

## <span data-ttu-id="d22f1-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d22f1-146">RELATED LINKS</span></span>

