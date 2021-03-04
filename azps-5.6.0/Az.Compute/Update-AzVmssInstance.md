---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: ed0ad08d94cbc67832b6a0dbb85882bd18692d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939642"
---
# <span data-ttu-id="86e2f-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="86e2f-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="86e2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="86e2f-103">Elindítja a VMSS-példány manuális frissítését.</span><span class="sxs-lookup"><span data-stu-id="86e2f-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="86e2f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="86e2f-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86e2f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="86e2f-105">DESCRIPTION</span></span>
<span data-ttu-id="86e2f-106">A Update-AzVmssInstance parancsmag elindítja a virtuálisgép-mérethalmaz (VMSS) adott példányának manuális frissítését.</span><span class="sxs-lookup"><span data-stu-id="86e2f-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="86e2f-107">Ezt akkor használja a rendszer, ha a VMSS scale set frissítési házirend beállítása manuális.</span><span class="sxs-lookup"><span data-stu-id="86e2f-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="86e2f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="86e2f-108">EXAMPLES</span></span>

### <span data-ttu-id="86e2f-109">1. példa: A VMSS-példány frissítésének kezdése</span><span class="sxs-lookup"><span data-stu-id="86e2f-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="86e2f-110">Ez a parancs elindítja a VMScaleSet001 nevű VMSS frissítését, amely 0 példányazonosítóval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="86e2f-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="86e2f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86e2f-111">PARAMETERS</span></span>

### <span data-ttu-id="86e2f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86e2f-112">-AsJob</span></span>
<span data-ttu-id="86e2f-113">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="86e2f-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="86e2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e2f-114">-DefaultProfile</span></span>
<span data-ttu-id="86e2f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86e2f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86e2f-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="86e2f-116">-InstanceId</span></span>
<span data-ttu-id="86e2f-117">Karakterlánc-tömbként megadja a frissíthető példány azonosítóját vagy azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="86e2f-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86e2f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86e2f-118">-ResourceGroupName</span></span>
<span data-ttu-id="86e2f-119">A VMSS erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86e2f-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="86e2f-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="86e2f-120">-VMScaleSetName</span></span>
<span data-ttu-id="86e2f-121">Annak a VMSS-példánynak a nevét adja meg, amelyről a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="86e2f-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="86e2f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86e2f-122">-Confirm</span></span>
<span data-ttu-id="86e2f-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="86e2f-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e2f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86e2f-124">-WhatIf</span></span>
<span data-ttu-id="86e2f-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="86e2f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86e2f-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86e2f-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e2f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e2f-127">CommonParameters</span></span>
<span data-ttu-id="86e2f-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86e2f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e2f-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86e2f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e2f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86e2f-130">INPUTS</span></span>

### <span data-ttu-id="86e2f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="86e2f-131">System.String</span></span>

### <span data-ttu-id="86e2f-132">System.String[]</span><span class="sxs-lookup"><span data-stu-id="86e2f-132">System.String[]</span></span>

## <span data-ttu-id="86e2f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86e2f-133">OUTPUTS</span></span>

### <span data-ttu-id="86e2f-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="86e2f-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="86e2f-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="86e2f-135">NOTES</span></span>

## <span data-ttu-id="86e2f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86e2f-136">RELATED LINKS</span></span>

[<span data-ttu-id="86e2f-137">Update-AzVms</span><span class="sxs-lookup"><span data-stu-id="86e2f-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


