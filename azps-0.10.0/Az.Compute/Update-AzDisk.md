---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: 8925e294b329b76f996a21d24597a4a8b5388a74
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842446"
---
# <span data-ttu-id="4debb-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="4debb-101">Update-AzDisk</span></span>

## <span data-ttu-id="4debb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4debb-102">SYNOPSIS</span></span>
<span data-ttu-id="4debb-103">Frissít egy lemezt.</span><span class="sxs-lookup"><span data-stu-id="4debb-103">Updates a disk.</span></span>

## <span data-ttu-id="4debb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4debb-104">SYNTAX</span></span>

### <span data-ttu-id="4debb-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4debb-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4debb-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="4debb-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4debb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4debb-107">DESCRIPTION</span></span>
<span data-ttu-id="4debb-108">Az **Update-AzDisk** parancsmag frissíti a lemezt.</span><span class="sxs-lookup"><span data-stu-id="4debb-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="4debb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4debb-109">EXAMPLES</span></span>

### <span data-ttu-id="4debb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4debb-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="4debb-111">Az első parancs létrehoz egy helyi üres Disk Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="4debb-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="4debb-112">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="4debb-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="4debb-113">A második és a harmadik parancs a Disk Update objektum merevlemez-titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="4debb-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="4debb-114">Az utolsó parancs átveszi a Disk Update objektumot, és frissíti a meglévő, "Disk01" nevű lemezt az erőforráscsoport "ResourceGroup01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="4debb-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="4debb-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="4debb-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="4debb-116">Ez a parancs frissíti a "Disk01" nevű, a "ResourceGroup01" nevű, 10 GB-nyi méretű kötetet használó meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="4debb-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="4debb-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="4debb-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="4debb-118">Ezek a parancsok frissítik a meglévő, "Disk01" nevű lemezt a "ResourceGroup01" és a 10 GB méretű merevlemezek között is.</span><span class="sxs-lookup"><span data-stu-id="4debb-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="4debb-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4debb-119">PARAMETERS</span></span>

### <span data-ttu-id="4debb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4debb-120">-AsJob</span></span>
<span data-ttu-id="4debb-121">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="4debb-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4debb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4debb-122">-DefaultProfile</span></span>
<span data-ttu-id="4debb-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4debb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4debb-124">-Disk</span><span class="sxs-lookup"><span data-stu-id="4debb-124">-Disk</span></span>
<span data-ttu-id="4debb-125">Helyi lemez-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4debb-125">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4debb-126">-DiskName</span><span class="sxs-lookup"><span data-stu-id="4debb-126">-DiskName</span></span>
<span data-ttu-id="4debb-127">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4debb-127">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="4debb-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="4debb-128">-DiskUpdate</span></span>
<span data-ttu-id="4debb-129">Helyi merevlemez-frissítő objektum megadása</span><span class="sxs-lookup"><span data-stu-id="4debb-129">Specifies a local disk update object.</span></span>

```yaml
Type: PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4debb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4debb-130">-ResourceGroupName</span></span>
<span data-ttu-id="4debb-131">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4debb-131">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4debb-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4debb-132">-Confirm</span></span>
<span data-ttu-id="4debb-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4debb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4debb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4debb-134">-WhatIf</span></span>
<span data-ttu-id="4debb-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4debb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4debb-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4debb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4debb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4debb-137">CommonParameters</span></span>
<span data-ttu-id="4debb-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4debb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4debb-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4debb-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4debb-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4debb-140">INPUTS</span></span>

### <span data-ttu-id="4debb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4debb-141">System.String</span></span>
<span data-ttu-id="4debb-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="4debb-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="4debb-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4debb-143">OUTPUTS</span></span>

### <span data-ttu-id="4debb-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="4debb-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="4debb-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4debb-145">NOTES</span></span>

## <span data-ttu-id="4debb-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4debb-146">RELATED LINKS</span></span>

