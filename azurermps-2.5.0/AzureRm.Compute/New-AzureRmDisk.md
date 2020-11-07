---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 2cb1cad343f57f164529e3607c1ad0b1ec74df05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848526"
---
# <span data-ttu-id="bea4b-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="bea4b-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="bea4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bea4b-102">SYNOPSIS</span></span>
<span data-ttu-id="bea4b-103">Felügyelt lemezt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bea4b-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bea4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bea4b-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bea4b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bea4b-105">DESCRIPTION</span></span>
<span data-ttu-id="bea4b-106">A **New-AzureRmDisk** parancsmag létrehoz egy felügyelt lemezt.</span><span class="sxs-lookup"><span data-stu-id="bea4b-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="bea4b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bea4b-107">EXAMPLES</span></span>

### <span data-ttu-id="bea4b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bea4b-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="bea4b-109">Az első parancs létrehoz egy helyi üres lemez-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="bea4b-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="bea4b-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="bea4b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="bea4b-111">A második és a harmadik parancs a Disk-objektum titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="bea4b-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="bea4b-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="bea4b-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bea4b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bea4b-113">PARAMETERS</span></span>

### <span data-ttu-id="bea4b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bea4b-114">-AsJob</span></span>
<span data-ttu-id="bea4b-115">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="bea4b-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bea4b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea4b-116">-DefaultProfile</span></span>
<span data-ttu-id="bea4b-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bea4b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bea4b-118">-Disk</span><span class="sxs-lookup"><span data-stu-id="bea4b-118">-Disk</span></span>
<span data-ttu-id="bea4b-119">Helyi lemez-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="bea4b-119">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="bea4b-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="bea4b-120">-DiskName</span></span>
<span data-ttu-id="bea4b-121">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bea4b-121">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="bea4b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea4b-122">-ResourceGroupName</span></span>
<span data-ttu-id="bea4b-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bea4b-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bea4b-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bea4b-124">-Confirm</span></span>
<span data-ttu-id="bea4b-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bea4b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bea4b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bea4b-126">-WhatIf</span></span>
<span data-ttu-id="bea4b-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bea4b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bea4b-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bea4b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bea4b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea4b-129">CommonParameters</span></span>
<span data-ttu-id="bea4b-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bea4b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea4b-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea4b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea4b-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bea4b-132">INPUTS</span></span>

### <span data-ttu-id="bea4b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bea4b-133">System.String</span></span>
<span data-ttu-id="bea4b-134">Microsoft. Azure. Management. számítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="bea4b-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="bea4b-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bea4b-135">OUTPUTS</span></span>

### <span data-ttu-id="bea4b-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="bea4b-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="bea4b-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bea4b-137">NOTES</span></span>

## <span data-ttu-id="bea4b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bea4b-138">RELATED LINKS</span></span>

