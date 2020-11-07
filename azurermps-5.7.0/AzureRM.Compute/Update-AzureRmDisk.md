---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
ms.openlocfilehash: 30a6ac1a3d74423302cc8b39e8b494e2f1ee2e22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672028"
---
# <span data-ttu-id="c529d-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c529d-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="c529d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c529d-102">SYNOPSIS</span></span>
<span data-ttu-id="c529d-103">Frissít egy lemezt.</span><span class="sxs-lookup"><span data-stu-id="c529d-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c529d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c529d-104">SYNTAX</span></span>

### <span data-ttu-id="c529d-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c529d-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <DiskUpdate> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c529d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="c529d-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <Disk> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c529d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c529d-107">DESCRIPTION</span></span>
<span data-ttu-id="c529d-108">Az **Update-AzureRmDisk** parancsmag frissíti a lemezt.</span><span class="sxs-lookup"><span data-stu-id="c529d-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="c529d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c529d-109">EXAMPLES</span></span>

### <span data-ttu-id="c529d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c529d-110">Example 1</span></span>
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

<span data-ttu-id="c529d-111">Az első parancs létrehoz egy helyi üres Disk Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="c529d-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="c529d-112">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="c529d-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="c529d-113">A második és a harmadik parancs a Disk Update objektum merevlemez-titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c529d-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="c529d-114">Az utolsó parancs átveszi a Disk Update objektumot, és frissíti a meglévő, "Disk01" nevű lemezt az erőforráscsoport "ResourceGroup01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="c529d-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c529d-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="c529d-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="c529d-116">Ez a parancs frissíti a "Disk01" nevű, a "ResourceGroup01" nevű, 10 GB-nyi méretű kötetet használó meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="c529d-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="c529d-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="c529d-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="c529d-118">Ezek a parancsok frissítik a meglévő, "Disk01" nevű lemezt a "ResourceGroup01" és a 10 GB méretű merevlemezek között is.</span><span class="sxs-lookup"><span data-stu-id="c529d-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="c529d-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c529d-119">PARAMETERS</span></span>

### <span data-ttu-id="c529d-120">-Disk</span><span class="sxs-lookup"><span data-stu-id="c529d-120">-Disk</span></span>
<span data-ttu-id="c529d-121">Helyi lemez-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c529d-121">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c529d-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="c529d-122">-DiskName</span></span>
<span data-ttu-id="c529d-123">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c529d-123">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="c529d-124">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="c529d-124">-DiskUpdate</span></span>
<span data-ttu-id="c529d-125">Helyi merevlemez-frissítő objektum megadása</span><span class="sxs-lookup"><span data-stu-id="c529d-125">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c529d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c529d-126">-ResourceGroupName</span></span>
<span data-ttu-id="c529d-127">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c529d-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c529d-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c529d-128">-Confirm</span></span>
<span data-ttu-id="c529d-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c529d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c529d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c529d-130">-WhatIf</span></span>
<span data-ttu-id="c529d-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c529d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c529d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c529d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c529d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c529d-133">CommonParameters</span></span>
<span data-ttu-id="c529d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c529d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c529d-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c529d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c529d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c529d-136">INPUTS</span></span>

### <span data-ttu-id="c529d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c529d-137">System.String</span></span>
<span data-ttu-id="c529d-138">Microsoft. Azure. Management. számítás. models. DiskUpdate Microsoft. Azure. Management. kiszámítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="c529d-138">Microsoft.Azure.Management.Compute.Models.DiskUpdate Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="c529d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c529d-139">OUTPUTS</span></span>

### <span data-ttu-id="c529d-140">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="c529d-140">System.Object</span></span>

## <span data-ttu-id="c529d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c529d-141">NOTES</span></span>

## <span data-ttu-id="c529d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c529d-142">RELATED LINKS</span></span>

