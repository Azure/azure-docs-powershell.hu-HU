---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
ms.openlocfilehash: 5ccaccdc5d447ac9ccdc49cf53230c58a5758e4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181179"
---
# <span data-ttu-id="3ddda-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="3ddda-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="3ddda-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ddda-102">SYNOPSIS</span></span>
<span data-ttu-id="3ddda-103">A virtuális gép patch állapotának felmérése</span><span class="sxs-lookup"><span data-stu-id="3ddda-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="3ddda-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ddda-104">SYNTAX</span></span>

### <span data-ttu-id="3ddda-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ddda-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ddda-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ddda-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ddda-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ddda-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ddda-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ddda-108">DESCRIPTION</span></span>
<span data-ttu-id="3ddda-109">A VM javítás állapotát értékeli, és a telepítéshez elérhető összes észlelt javítást jelenti.</span><span class="sxs-lookup"><span data-stu-id="3ddda-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="3ddda-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3ddda-110">EXAMPLES</span></span>

### <span data-ttu-id="3ddda-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3ddda-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="3ddda-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ddda-112">PARAMETERS</span></span>

### <span data-ttu-id="3ddda-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ddda-113">-AsJob</span></span>
<span data-ttu-id="3ddda-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3ddda-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ddda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ddda-115">-DefaultProfile</span></span>
<span data-ttu-id="3ddda-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ddda-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ddda-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ddda-117">-ResourceGroupName</span></span>
<span data-ttu-id="3ddda-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ddda-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ddda-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ddda-119">-ResourceId</span></span>
<span data-ttu-id="3ddda-120">A virtuális gép erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3ddda-120">Resource ID for your virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ddda-121">-VM</span><span class="sxs-lookup"><span data-stu-id="3ddda-121">-VM</span></span>
<span data-ttu-id="3ddda-122">PowerShell virtuálisgép-objektum</span><span class="sxs-lookup"><span data-stu-id="3ddda-122">PowerShell Virtual Machine Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: InputObjectParameterSet
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ddda-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="3ddda-123">-VMName</span></span>
<span data-ttu-id="3ddda-124">Virtuális gép neve</span><span class="sxs-lookup"><span data-stu-id="3ddda-124">Virtual Machine name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ddda-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ddda-125">-Confirm</span></span>
<span data-ttu-id="3ddda-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ddda-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ddda-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ddda-127">-WhatIf</span></span>
<span data-ttu-id="3ddda-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ddda-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ddda-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ddda-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ddda-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ddda-130">CommonParameters</span></span>
<span data-ttu-id="3ddda-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ddda-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ddda-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3ddda-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ddda-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ddda-133">INPUTS</span></span>

### <span data-ttu-id="3ddda-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3ddda-134">System.String</span></span>

## <span data-ttu-id="3ddda-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ddda-135">OUTPUTS</span></span>

### <span data-ttu-id="3ddda-136">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="3ddda-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="3ddda-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ddda-137">NOTES</span></span>

## <span data-ttu-id="3ddda-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ddda-138">RELATED LINKS</span></span>
