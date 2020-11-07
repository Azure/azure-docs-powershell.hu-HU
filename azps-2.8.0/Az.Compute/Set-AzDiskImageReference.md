---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 3a18c56d01481e9e8096725685a9a60aff7dc8f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667254"
---
# <span data-ttu-id="7915e-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="7915e-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="7915e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7915e-102">SYNOPSIS</span></span>
<span data-ttu-id="7915e-103">A kép hivatkozási tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="7915e-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="7915e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7915e-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7915e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7915e-105">DESCRIPTION</span></span>
<span data-ttu-id="7915e-106">A **set-AzDiskImageReference** parancsmag a Képhivatkozás tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="7915e-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="7915e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7915e-107">EXAMPLES</span></span>

### <span data-ttu-id="7915e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7915e-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="7915e-109">Az első parancs létrehoz egy helyi merevlemez-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="7915e-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="7915e-110">A Windows OS típust is beállítja.</span><span class="sxs-lookup"><span data-stu-id="7915e-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="7915e-111">A második parancs beállítja a képazonosítót és a 0 logikai egységet a Disk objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="7915e-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="7915e-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="7915e-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7915e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7915e-113">PARAMETERS</span></span>

### <span data-ttu-id="7915e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7915e-114">-DefaultProfile</span></span>
<span data-ttu-id="7915e-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7915e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7915e-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="7915e-116">-Disk</span></span>
<span data-ttu-id="7915e-117">Helyi lemez-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7915e-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="7915e-118">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="7915e-118">-Id</span></span>
<span data-ttu-id="7915e-119">Az azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="7915e-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="7915e-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="7915e-120">-Lun</span></span>
<span data-ttu-id="7915e-121">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7915e-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="7915e-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7915e-122">-Confirm</span></span>
<span data-ttu-id="7915e-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7915e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7915e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7915e-124">-WhatIf</span></span>
<span data-ttu-id="7915e-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7915e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7915e-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7915e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7915e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7915e-127">CommonParameters</span></span>
<span data-ttu-id="7915e-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7915e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7915e-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7915e-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7915e-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7915e-130">INPUTS</span></span>

### <span data-ttu-id="7915e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="7915e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="7915e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7915e-132">System.String</span></span>

### <span data-ttu-id="7915e-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7915e-133">System.Int32</span></span>

## <span data-ttu-id="7915e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7915e-134">OUTPUTS</span></span>

### <span data-ttu-id="7915e-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="7915e-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="7915e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7915e-136">NOTES</span></span>

## <span data-ttu-id="7915e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7915e-137">RELATED LINKS</span></span>
