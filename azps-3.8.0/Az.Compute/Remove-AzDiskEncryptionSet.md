---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847650"
---
# <span data-ttu-id="13149-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="13149-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="13149-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13149-102">SYNOPSIS</span></span>
<span data-ttu-id="13149-103">A Lemezkarbantartó-készlet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="13149-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="13149-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13149-104">SYNTAX</span></span>

### <span data-ttu-id="13149-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13149-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13149-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="13149-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13149-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="13149-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13149-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="13149-108">DESCRIPTION</span></span>
<span data-ttu-id="13149-109">A Lemezkarbantartó-készlet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="13149-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="13149-110">Példák</span><span class="sxs-lookup"><span data-stu-id="13149-110">EXAMPLES</span></span>

### <span data-ttu-id="13149-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13149-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="13149-112">A "enc1" titkosítási készlet törlése a "rg1"-ban</span><span class="sxs-lookup"><span data-stu-id="13149-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="13149-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13149-113">PARAMETERS</span></span>

### <span data-ttu-id="13149-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13149-114">-AsJob</span></span>
<span data-ttu-id="13149-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="13149-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13149-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13149-116">-DefaultProfile</span></span>
<span data-ttu-id="13149-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13149-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13149-118">-Force</span><span class="sxs-lookup"><span data-stu-id="13149-118">-Force</span></span>
<span data-ttu-id="13149-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="13149-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="13149-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13149-120">-InputObject</span></span>
<span data-ttu-id="13149-121">A merevlemez-titkosítási készlet helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="13149-121">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13149-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13149-122">-Name</span></span>
<span data-ttu-id="13149-123">A lemez titkosítási készletének neve.</span><span class="sxs-lookup"><span data-stu-id="13149-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13149-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13149-124">-ResourceGroupName</span></span>
<span data-ttu-id="13149-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13149-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13149-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13149-126">-ResourceId</span></span>
<span data-ttu-id="13149-127">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="13149-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13149-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13149-128">-Confirm</span></span>
<span data-ttu-id="13149-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13149-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13149-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13149-130">-WhatIf</span></span>
<span data-ttu-id="13149-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13149-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13149-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13149-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13149-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13149-133">CommonParameters</span></span>
<span data-ttu-id="13149-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13149-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13149-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="13149-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13149-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13149-136">INPUTS</span></span>

### <span data-ttu-id="13149-137">System. String</span><span class="sxs-lookup"><span data-stu-id="13149-137">System.String</span></span>

### <span data-ttu-id="13149-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="13149-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="13149-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13149-139">OUTPUTS</span></span>

### <span data-ttu-id="13149-140">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="13149-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="13149-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13149-141">NOTES</span></span>

## <span data-ttu-id="13149-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13149-142">RELATED LINKS</span></span>
