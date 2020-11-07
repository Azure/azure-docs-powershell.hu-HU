---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDisk.md
ms.openlocfilehash: 1eea8504f974e7ffc504520a5b5abc036c4d3e2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844509"
---
# <span data-ttu-id="c3589-101">New-AzDisk</span><span class="sxs-lookup"><span data-stu-id="c3589-101">New-AzDisk</span></span>

## <span data-ttu-id="c3589-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3589-102">SYNOPSIS</span></span>
<span data-ttu-id="c3589-103">Felügyelt lemezt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c3589-103">Creates a managed disk.</span></span>

## <span data-ttu-id="c3589-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3589-104">SYNTAX</span></span>

```
New-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3589-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3589-105">DESCRIPTION</span></span>
<span data-ttu-id="c3589-106">A **New-AzDisk** parancsmag létrehoz egy felügyelt lemezt.</span><span class="sxs-lookup"><span data-stu-id="c3589-106">The **New-AzDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="c3589-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c3589-107">EXAMPLES</span></span>

### <span data-ttu-id="c3589-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c3589-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="c3589-109">Az első parancs létrehoz egy helyi üres lemez-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="c3589-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="c3589-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="c3589-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="c3589-111">A második és a harmadik parancs a Disk-objektum titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3589-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="c3589-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="c3589-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c3589-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3589-113">PARAMETERS</span></span>

### <span data-ttu-id="c3589-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3589-114">-AsJob</span></span>
<span data-ttu-id="c3589-115">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="c3589-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c3589-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3589-116">-DefaultProfile</span></span>
<span data-ttu-id="c3589-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3589-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3589-118">-Disk</span><span class="sxs-lookup"><span data-stu-id="c3589-118">-Disk</span></span>
<span data-ttu-id="c3589-119">Helyi lemez-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c3589-119">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3589-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="c3589-120">-DiskName</span></span>
<span data-ttu-id="c3589-121">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3589-121">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="c3589-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3589-122">-ResourceGroupName</span></span>
<span data-ttu-id="c3589-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3589-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c3589-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3589-124">-Confirm</span></span>
<span data-ttu-id="c3589-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3589-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3589-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3589-126">-WhatIf</span></span>
<span data-ttu-id="c3589-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3589-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3589-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3589-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3589-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3589-129">CommonParameters</span></span>
<span data-ttu-id="c3589-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3589-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3589-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3589-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3589-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3589-132">INPUTS</span></span>

### <span data-ttu-id="c3589-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c3589-133">System.String</span></span>
<span data-ttu-id="c3589-134">Microsoft. Azure. Management. számítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="c3589-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="c3589-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3589-135">OUTPUTS</span></span>

### <span data-ttu-id="c3589-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="c3589-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="c3589-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3589-137">NOTES</span></span>

## <span data-ttu-id="c3589-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3589-138">RELATED LINKS</span></span>

