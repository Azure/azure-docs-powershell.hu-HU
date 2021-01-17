---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: 18f013643ad65bd4f7c70f3181e5950e10aa08ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480674"
---
# <span data-ttu-id="8e791-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="8e791-101">Update-AzDisk</span></span>

## <span data-ttu-id="8e791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e791-102">SYNOPSIS</span></span>
<span data-ttu-id="8e791-103">Frissíti a lemezeket.</span><span class="sxs-lookup"><span data-stu-id="8e791-103">Updates a disk.</span></span>

## <span data-ttu-id="8e791-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e791-104">SYNTAX</span></span>

### <span data-ttu-id="8e791-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e791-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e791-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="8e791-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e791-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e791-107">DESCRIPTION</span></span>
<span data-ttu-id="8e791-108">Az **Update-AzDisk** parancsmag frissíti a lemezeket.</span><span class="sxs-lookup"><span data-stu-id="8e791-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="8e791-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e791-109">EXAMPLES</span></span>

### <span data-ttu-id="8e791-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="8e791-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="8e791-111">Az első parancs egy 10 GB-os helyi üres lemezfrissítési objektumot hoz létre Premium_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="8e791-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="8e791-112">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="8e791-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="8e791-113">A második és a harmadik parancs a lemezfrissítési objektum lemeztitkosítási kulcsának és kulcstitkosítási kulcsának beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e791-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="8e791-114">Az utolsó parancs átveszi a lemezfrissítési objektumot, és frissíti a "Disk01" nevű meglévő lemez nevét az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="8e791-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="8e791-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="8e791-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="8e791-116">Ez a parancs 10 GB-os lemezméretre frissíti az "ResourceGroup01" erőforráscsoport "Disk01" nevű meglévő lemezét.</span><span class="sxs-lookup"><span data-stu-id="8e791-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="8e791-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="8e791-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="8e791-118">Ezek a parancsok a "ResourceGroup01" erőforráscsoportban a "Disk01" nevű meglévő lemezeket is frissítik 10 GB-os lemezméretre.</span><span class="sxs-lookup"><span data-stu-id="8e791-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="8e791-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e791-119">PARAMETERS</span></span>

### <span data-ttu-id="8e791-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e791-120">-AsJob</span></span>
<span data-ttu-id="8e791-121">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="8e791-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8e791-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e791-122">-DefaultProfile</span></span>
<span data-ttu-id="8e791-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e791-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e791-124">-Disk</span><span class="sxs-lookup"><span data-stu-id="8e791-124">-Disk</span></span>
<span data-ttu-id="8e791-125">Helyi lemezobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8e791-125">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e791-126">-DiskName</span><span class="sxs-lookup"><span data-stu-id="8e791-126">-DiskName</span></span>
<span data-ttu-id="8e791-127">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e791-127">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="8e791-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="8e791-128">-DiskUpdate</span></span>
<span data-ttu-id="8e791-129">Helyi lemezfrissítési objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8e791-129">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e791-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e791-130">-ResourceGroupName</span></span>
<span data-ttu-id="8e791-131">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e791-131">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8e791-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e791-132">-Confirm</span></span>
<span data-ttu-id="8e791-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8e791-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e791-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e791-134">-WhatIf</span></span>
<span data-ttu-id="8e791-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8e791-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e791-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e791-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e791-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e791-137">CommonParameters</span></span>
<span data-ttu-id="8e791-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e791-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e791-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e791-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e791-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e791-140">INPUTS</span></span>

### <span data-ttu-id="8e791-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8e791-141">System.String</span></span>

### <span data-ttu-id="8e791-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="8e791-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="8e791-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="8e791-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="8e791-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e791-144">OUTPUTS</span></span>

### <span data-ttu-id="8e791-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="8e791-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="8e791-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e791-146">NOTES</span></span>

## <span data-ttu-id="8e791-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e791-147">RELATED LINKS</span></span>
