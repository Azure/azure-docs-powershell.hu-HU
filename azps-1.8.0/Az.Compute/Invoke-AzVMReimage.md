---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 6c8744d68abfab882e56b0b7e33674d48232c900
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836764"
---
# <span data-ttu-id="92210-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="92210-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="92210-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92210-102">SYNOPSIS</span></span>
<span data-ttu-id="92210-103">Egy Azure Virtual Machine Reimage-et.</span><span class="sxs-lookup"><span data-stu-id="92210-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="92210-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92210-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92210-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="92210-105">DESCRIPTION</span></span>
<span data-ttu-id="92210-106">A **meghívó-AzVMReimage** parancsmag egy Azure Virtual Machine-t ábrázol.</span><span class="sxs-lookup"><span data-stu-id="92210-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="92210-107">Példák</span><span class="sxs-lookup"><span data-stu-id="92210-107">EXAMPLES</span></span>

### <span data-ttu-id="92210-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="92210-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="92210-109">Ez a parancs a VirtualMachine07 nevű virtuális gépet a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="92210-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="92210-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92210-110">PARAMETERS</span></span>

### <span data-ttu-id="92210-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92210-111">-AsJob</span></span>
<span data-ttu-id="92210-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="92210-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92210-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92210-113">-DefaultProfile</span></span>
<span data-ttu-id="92210-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92210-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92210-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92210-115">-ResourceGroupName</span></span>
<span data-ttu-id="92210-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="92210-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="92210-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="92210-117">-TempDisk</span></span>
<span data-ttu-id="92210-118">Itt adhatja meg, hogy a temp Disk-e.</span><span class="sxs-lookup"><span data-stu-id="92210-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="92210-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="92210-119">-VMName</span></span>
<span data-ttu-id="92210-120">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="92210-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="92210-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="92210-121">-Confirm</span></span>
<span data-ttu-id="92210-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="92210-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92210-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92210-123">-WhatIf</span></span>
<span data-ttu-id="92210-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="92210-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92210-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92210-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92210-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92210-126">CommonParameters</span></span>
<span data-ttu-id="92210-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92210-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92210-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92210-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92210-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92210-129">INPUTS</span></span>

### <span data-ttu-id="92210-130">System. String</span><span class="sxs-lookup"><span data-stu-id="92210-130">System.String</span></span>

## <span data-ttu-id="92210-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92210-131">OUTPUTS</span></span>

### <span data-ttu-id="92210-132">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="92210-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="92210-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92210-133">NOTES</span></span>

## <span data-ttu-id="92210-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92210-134">RELATED LINKS</span></span>
