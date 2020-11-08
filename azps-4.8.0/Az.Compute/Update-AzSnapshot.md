---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 6cfe2fd958d74740195b0bb29d3defa34f1310a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018100"
---
# <span data-ttu-id="80f6c-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="80f6c-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="80f6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="80f6c-103">Pillanatképek frissítése</span><span class="sxs-lookup"><span data-stu-id="80f6c-103">Updates a snapshot.</span></span>

## <span data-ttu-id="80f6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80f6c-104">SYNTAX</span></span>

### <span data-ttu-id="80f6c-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80f6c-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80f6c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="80f6c-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80f6c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="80f6c-107">DESCRIPTION</span></span>
<span data-ttu-id="80f6c-108">Az **Update-AzSnapshot** parancsmag frissíti a pillanatképet.</span><span class="sxs-lookup"><span data-stu-id="80f6c-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="80f6c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="80f6c-109">EXAMPLES</span></span>

### <span data-ttu-id="80f6c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="80f6c-110">Example 1</span></span>
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

<span data-ttu-id="80f6c-111">Az első parancs létrehoz egy helyi üres Snapshot Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="80f6c-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="80f6c-112">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="80f6c-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="80f6c-113">A második és a harmadik parancs beállítja a merevlemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot Update objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="80f6c-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="80f6c-114">Az utolsó parancs átveszi a Snapshot Update objektumát, és frissíti a "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="80f6c-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="80f6c-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="80f6c-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="80f6c-116">Ez a parancs frissíti a meglévő, "Snapshot01" nevű pillanatképet a "ResourceGroup01" és a 10 GB méretű merevlemez között.</span><span class="sxs-lookup"><span data-stu-id="80f6c-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="80f6c-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="80f6c-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="80f6c-118">Ezek a parancsok frissítik a meglévő, "Snapshot01" nevű pillanatképet a "ResourceGroup01" és a 10 GB méretű merevlemezek között.</span><span class="sxs-lookup"><span data-stu-id="80f6c-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="80f6c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80f6c-119">PARAMETERS</span></span>

### <span data-ttu-id="80f6c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80f6c-120">-AsJob</span></span>
<span data-ttu-id="80f6c-121">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="80f6c-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80f6c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f6c-122">-DefaultProfile</span></span>
<span data-ttu-id="80f6c-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80f6c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80f6c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80f6c-124">-ResourceGroupName</span></span>
<span data-ttu-id="80f6c-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80f6c-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f6c-126">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="80f6c-126">-Snapshot</span></span>
<span data-ttu-id="80f6c-127">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="80f6c-127">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80f6c-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="80f6c-128">-SnapshotName</span></span>
<span data-ttu-id="80f6c-129">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80f6c-129">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f6c-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="80f6c-130">-SnapshotUpdate</span></span>
<span data-ttu-id="80f6c-131">Egy helyi Snapshot Update-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="80f6c-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80f6c-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="80f6c-132">-Confirm</span></span>
<span data-ttu-id="80f6c-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="80f6c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80f6c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80f6c-134">-WhatIf</span></span>
<span data-ttu-id="80f6c-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="80f6c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80f6c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="80f6c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80f6c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f6c-137">CommonParameters</span></span>
<span data-ttu-id="80f6c-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80f6c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f6c-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="80f6c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f6c-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80f6c-140">INPUTS</span></span>

### <span data-ttu-id="80f6c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="80f6c-141">System.String</span></span>

### <span data-ttu-id="80f6c-142">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="80f6c-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="80f6c-143">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="80f6c-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="80f6c-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80f6c-144">OUTPUTS</span></span>

### <span data-ttu-id="80f6c-145">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="80f6c-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="80f6c-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80f6c-146">NOTES</span></span>

## <span data-ttu-id="80f6c-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80f6c-147">RELATED LINKS</span></span>
