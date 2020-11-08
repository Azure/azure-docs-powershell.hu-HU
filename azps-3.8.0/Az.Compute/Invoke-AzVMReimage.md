---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011485"
---
# <span data-ttu-id="867d7-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="867d7-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="867d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="867d7-102">SYNOPSIS</span></span>
<span data-ttu-id="867d7-103">Egy Azure Virtual Machine Reimage-et.</span><span class="sxs-lookup"><span data-stu-id="867d7-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="867d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="867d7-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="867d7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="867d7-105">DESCRIPTION</span></span>
<span data-ttu-id="867d7-106">A **meghívó-AzVMReimage** parancsmag egy Azure Virtual Machine-t ábrázol.</span><span class="sxs-lookup"><span data-stu-id="867d7-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="867d7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="867d7-107">EXAMPLES</span></span>

### <span data-ttu-id="867d7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="867d7-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="867d7-109">Ez a parancs a VirtualMachine07 nevű virtuális gépet a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="867d7-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="867d7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="867d7-110">PARAMETERS</span></span>

### <span data-ttu-id="867d7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="867d7-111">-AsJob</span></span>
<span data-ttu-id="867d7-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="867d7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="867d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="867d7-113">-DefaultProfile</span></span>
<span data-ttu-id="867d7-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="867d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="867d7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="867d7-115">-ResourceGroupName</span></span>
<span data-ttu-id="867d7-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="867d7-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="867d7-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="867d7-117">-TempDisk</span></span>
<span data-ttu-id="867d7-118">Itt adhatja meg, hogy a temp Disk-e.</span><span class="sxs-lookup"><span data-stu-id="867d7-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="867d7-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="867d7-119">-VMName</span></span>
<span data-ttu-id="867d7-120">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="867d7-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="867d7-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="867d7-121">-Confirm</span></span>
<span data-ttu-id="867d7-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="867d7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="867d7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="867d7-123">-WhatIf</span></span>
<span data-ttu-id="867d7-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="867d7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="867d7-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="867d7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="867d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="867d7-126">CommonParameters</span></span>
<span data-ttu-id="867d7-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="867d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="867d7-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="867d7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="867d7-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="867d7-129">INPUTS</span></span>

### <span data-ttu-id="867d7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="867d7-130">System.String</span></span>

## <span data-ttu-id="867d7-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="867d7-131">OUTPUTS</span></span>

### <span data-ttu-id="867d7-132">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="867d7-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="867d7-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="867d7-133">NOTES</span></span>

## <span data-ttu-id="867d7-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="867d7-134">RELATED LINKS</span></span>
