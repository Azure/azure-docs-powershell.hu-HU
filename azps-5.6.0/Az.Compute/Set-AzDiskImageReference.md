---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: aed0113b229d41665effd7904d2de2357b4b5d93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938850"
---
# <span data-ttu-id="60549-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="60549-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="60549-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60549-102">SYNOPSIS</span></span>
<span data-ttu-id="60549-103">Beállítja egy lemezobjektum képhivatkozási tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="60549-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="60549-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="60549-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60549-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="60549-105">DESCRIPTION</span></span>
<span data-ttu-id="60549-106">A **Set-AzDiskImageReference** parancsmag beállítja a képhivatkozási tulajdonságokat egy lemezobjektumon.</span><span class="sxs-lookup"><span data-stu-id="60549-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="60549-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="60549-107">EXAMPLES</span></span>

### <span data-ttu-id="60549-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="60549-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="60549-109">Az első parancs egy 10 GB méretű helyi lemezobjektumot hoz létre Premium_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="60549-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="60549-110">Emellett beállítja a Windows operációs rendszer típusát is.</span><span class="sxs-lookup"><span data-stu-id="60549-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="60549-111">A második parancs beállítja a lemezobjektum képazonosítóját és 0-s logikai egységszámát.</span><span class="sxs-lookup"><span data-stu-id="60549-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="60549-112">Az utolsó parancs átveszi a lemezobjektumot, és létrehoz egy "Disk01" nevű lemezt az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="60549-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="60549-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60549-113">PARAMETERS</span></span>

### <span data-ttu-id="60549-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60549-114">-DefaultProfile</span></span>
<span data-ttu-id="60549-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60549-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60549-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="60549-116">-Disk</span></span>
<span data-ttu-id="60549-117">Helyi lemezobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="60549-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="60549-118">-Id</span><span class="sxs-lookup"><span data-stu-id="60549-118">-Id</span></span>
<span data-ttu-id="60549-119">Az azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="60549-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="60549-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="60549-120">-Lun</span></span>
<span data-ttu-id="60549-121">A logikai egység számát (LUN) adja meg.</span><span class="sxs-lookup"><span data-stu-id="60549-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="60549-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60549-122">-Confirm</span></span>
<span data-ttu-id="60549-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="60549-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60549-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60549-124">-WhatIf</span></span>
<span data-ttu-id="60549-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="60549-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60549-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60549-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60549-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60549-127">CommonParameters</span></span>
<span data-ttu-id="60549-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60549-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60549-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60549-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60549-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60549-130">INPUTS</span></span>

### <span data-ttu-id="60549-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="60549-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="60549-132">System.String</span><span class="sxs-lookup"><span data-stu-id="60549-132">System.String</span></span>

### <span data-ttu-id="60549-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="60549-133">System.Int32</span></span>

## <span data-ttu-id="60549-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60549-134">OUTPUTS</span></span>

### <span data-ttu-id="60549-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="60549-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="60549-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="60549-136">NOTES</span></span>

## <span data-ttu-id="60549-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60549-137">RELATED LINKS</span></span>
