---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: f7adb9ef086b233d44f2e5d9c6eb132669b102e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162195"
---
# <span data-ttu-id="53f8a-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="53f8a-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="53f8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="53f8a-103">Elindítja a VMSS-példány manuális frissítését.</span><span class="sxs-lookup"><span data-stu-id="53f8a-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="53f8a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53f8a-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53f8a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53f8a-105">DESCRIPTION</span></span>
<span data-ttu-id="53f8a-106">A Update-AzVmssInstance parancsmag elindítja a virtuálisgép-mérethalmaz (VMSS) adott példányának manuális frissítését.</span><span class="sxs-lookup"><span data-stu-id="53f8a-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="53f8a-107">Ezt akkor használja a rendszer, ha a VMSS scale set frissítési házirend beállítása manuális.</span><span class="sxs-lookup"><span data-stu-id="53f8a-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="53f8a-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53f8a-108">EXAMPLES</span></span>

### <span data-ttu-id="53f8a-109">1. példa: A VMSS-példány frissítésének kezdése</span><span class="sxs-lookup"><span data-stu-id="53f8a-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="53f8a-110">Ez a parancs elindítja a VMScaleSet001 nevű VMSS-frissítését, amely 0 példányazonosítóval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="53f8a-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="53f8a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53f8a-111">PARAMETERS</span></span>

### <span data-ttu-id="53f8a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53f8a-112">-AsJob</span></span>
<span data-ttu-id="53f8a-113">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="53f8a-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="53f8a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f8a-114">-DefaultProfile</span></span>
<span data-ttu-id="53f8a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53f8a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53f8a-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="53f8a-116">-InstanceId</span></span>
<span data-ttu-id="53f8a-117">Karakterlánc-tömbként megadja a frissíthető példány azonosítóját vagy azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="53f8a-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

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

### <span data-ttu-id="53f8a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f8a-118">-ResourceGroupName</span></span>
<span data-ttu-id="53f8a-119">A VMSS erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53f8a-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="53f8a-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="53f8a-120">-VMScaleSetName</span></span>
<span data-ttu-id="53f8a-121">Annak a VMSS-példánynak a nevét adja meg, amelyről a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="53f8a-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="53f8a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53f8a-122">-Confirm</span></span>
<span data-ttu-id="53f8a-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="53f8a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53f8a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53f8a-124">-WhatIf</span></span>
<span data-ttu-id="53f8a-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="53f8a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53f8a-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53f8a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53f8a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f8a-127">CommonParameters</span></span>
<span data-ttu-id="53f8a-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f8a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f8a-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53f8a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f8a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53f8a-130">INPUTS</span></span>

### <span data-ttu-id="53f8a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="53f8a-131">System.String</span></span>

### <span data-ttu-id="53f8a-132">System.String[]</span><span class="sxs-lookup"><span data-stu-id="53f8a-132">System.String[]</span></span>

## <span data-ttu-id="53f8a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53f8a-133">OUTPUTS</span></span>

### <span data-ttu-id="53f8a-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="53f8a-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="53f8a-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53f8a-135">NOTES</span></span>

## <span data-ttu-id="53f8a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53f8a-136">RELATED LINKS</span></span>

[<span data-ttu-id="53f8a-137">Update-AzVms</span><span class="sxs-lookup"><span data-stu-id="53f8a-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


