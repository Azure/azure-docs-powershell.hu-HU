---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 6cfe2fd958d74740195b0bb29d3defa34f1310a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339690"
---
# <span data-ttu-id="d1d76-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="d1d76-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="d1d76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1d76-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d76-103">Frissíti a pillanatfelvételt.</span><span class="sxs-lookup"><span data-stu-id="d1d76-103">Updates a snapshot.</span></span>

## <span data-ttu-id="d1d76-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d1d76-104">SYNTAX</span></span>

### <span data-ttu-id="d1d76-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d1d76-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1d76-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d1d76-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1d76-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d1d76-107">DESCRIPTION</span></span>
<span data-ttu-id="d1d76-108">Az **Update-AzSnapshot** parancsmag frissíti a pillanatfelvételt.</span><span class="sxs-lookup"><span data-stu-id="d1d76-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="d1d76-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d1d76-109">EXAMPLES</span></span>

### <span data-ttu-id="d1d76-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d1d76-110">Example 1</span></span>
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

<span data-ttu-id="d1d76-111">Az első parancs egy 10 GB-os méretű helyi üres pillanatkép-frissítő objektumot hoz létre Premium_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="d1d76-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d1d76-112">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="d1d76-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d1d76-113">A második és a harmadik parancs a lemeztitkosítási kulcs és a kulcstitkosítási kulcs beállításait adja meg a pillanatfelvételi frissítési objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="d1d76-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="d1d76-114">Az utolsó parancs az "Erőforráscsoport01" erőforráscsoport pillanatkép-frissítő objektumában egy "Snapshot01" nevű pillanatképet frissít.</span><span class="sxs-lookup"><span data-stu-id="d1d76-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d1d76-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="d1d76-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="d1d76-116">Ez a parancs egy "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoportban 10 GB-os lemezméretre frissíti.</span><span class="sxs-lookup"><span data-stu-id="d1d76-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="d1d76-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="d1d76-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="d1d76-118">Ezek a parancsok a "Snapshot01" nevű meglévő pillanatképet is frissítik az "ResourceGroup01" erőforráscsoportban 10 GB-os lemezméretre.</span><span class="sxs-lookup"><span data-stu-id="d1d76-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="d1d76-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1d76-119">PARAMETERS</span></span>

### <span data-ttu-id="d1d76-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1d76-120">-AsJob</span></span>
<span data-ttu-id="d1d76-121">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="d1d76-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d1d76-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d76-122">-DefaultProfile</span></span>
<span data-ttu-id="d1d76-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1d76-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1d76-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1d76-124">-ResourceGroupName</span></span>
<span data-ttu-id="d1d76-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1d76-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d1d76-126">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="d1d76-126">-Snapshot</span></span>
<span data-ttu-id="d1d76-127">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d1d76-127">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="d1d76-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="d1d76-128">-SnapshotName</span></span>
<span data-ttu-id="d1d76-129">Egy pillanatfelvétel nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1d76-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="d1d76-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d1d76-130">-SnapshotUpdate</span></span>
<span data-ttu-id="d1d76-131">Helyi pillanatkép-frissítő objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d1d76-131">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="d1d76-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1d76-132">-Confirm</span></span>
<span data-ttu-id="d1d76-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d1d76-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1d76-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1d76-134">-WhatIf</span></span>
<span data-ttu-id="d1d76-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d1d76-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1d76-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1d76-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1d76-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d76-137">CommonParameters</span></span>
<span data-ttu-id="d1d76-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1d76-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d76-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1d76-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d76-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1d76-140">INPUTS</span></span>

### <span data-ttu-id="d1d76-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d1d76-141">System.String</span></span>

### <span data-ttu-id="d1d76-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d1d76-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="d1d76-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="d1d76-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="d1d76-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1d76-144">OUTPUTS</span></span>

### <span data-ttu-id="d1d76-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="d1d76-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="d1d76-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d1d76-146">NOTES</span></span>

## <span data-ttu-id="d1d76-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1d76-147">RELATED LINKS</span></span>
