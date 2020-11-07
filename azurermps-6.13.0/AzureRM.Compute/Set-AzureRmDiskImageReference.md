---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmDiskImageReference.md
ms.openlocfilehash: e544007d8e23e20ed311f07eb33f98a5e2d6a409
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672994"
---
# <span data-ttu-id="dc940-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="dc940-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="dc940-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc940-102">SYNOPSIS</span></span>
<span data-ttu-id="dc940-103">A kép hivatkozási tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="dc940-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc940-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc940-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc940-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc940-105">DESCRIPTION</span></span>
<span data-ttu-id="dc940-106">A **set-AzureRmDiskImageReference** parancsmag a Képhivatkozás tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="dc940-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="dc940-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dc940-107">EXAMPLES</span></span>

### <span data-ttu-id="dc940-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dc940-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="dc940-109">Az első parancs létrehoz egy helyi merevlemez-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="dc940-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="dc940-110">A Windows OS típust is beállítja.</span><span class="sxs-lookup"><span data-stu-id="dc940-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="dc940-111">A második parancs beállítja a képazonosítót és a 0 logikai egységet a Disk objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="dc940-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="dc940-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="dc940-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="dc940-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc940-113">PARAMETERS</span></span>

### <span data-ttu-id="dc940-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc940-114">-DefaultProfile</span></span>
<span data-ttu-id="dc940-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc940-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc940-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="dc940-116">-Disk</span></span>
<span data-ttu-id="dc940-117">Helyi lemez-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="dc940-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc940-118">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="dc940-118">-Id</span></span>
<span data-ttu-id="dc940-119">Az azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc940-119">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc940-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="dc940-120">-Lun</span></span>
<span data-ttu-id="dc940-121">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc940-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc940-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dc940-122">-Confirm</span></span>
<span data-ttu-id="dc940-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc940-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc940-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc940-124">-WhatIf</span></span>
<span data-ttu-id="dc940-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dc940-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc940-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dc940-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc940-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc940-127">CommonParameters</span></span>
<span data-ttu-id="dc940-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc940-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc940-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc940-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc940-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc940-130">INPUTS</span></span>

### <span data-ttu-id="dc940-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="dc940-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="dc940-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dc940-132">System.String</span></span>

### <span data-ttu-id="dc940-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="dc940-133">System.Int32</span></span>

## <span data-ttu-id="dc940-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc940-134">OUTPUTS</span></span>

### <span data-ttu-id="dc940-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="dc940-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="dc940-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc940-136">NOTES</span></span>

## <span data-ttu-id="dc940-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc940-137">RELATED LINKS</span></span>
