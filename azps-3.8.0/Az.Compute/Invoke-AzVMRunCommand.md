---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 77ac953e1b67ea896f15b13a2695505aabc05bbb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011482"
---
# <span data-ttu-id="f86b6-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="f86b6-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="f86b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f86b6-102">SYNOPSIS</span></span>
<span data-ttu-id="f86b6-103">Futtassa a parancsot a VM-ben.</span><span class="sxs-lookup"><span data-stu-id="f86b6-103">Run a command on the VM.</span></span>

## <span data-ttu-id="f86b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f86b6-104">SYNTAX</span></span>

### <span data-ttu-id="f86b6-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f86b6-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86b6-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f86b6-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f86b6-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="f86b6-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f86b6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f86b6-108">DESCRIPTION</span></span>
<span data-ttu-id="f86b6-109">Indítsa el a Futtatás parancsot a VM-ben.</span><span class="sxs-lookup"><span data-stu-id="f86b6-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="f86b6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f86b6-110">EXAMPLES</span></span>

### <span data-ttu-id="f86b6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f86b6-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="f86b6-112">Hivatkozhat a RunPowerShellScript Futtatás parancsára a "sample.ps1" és a "vmname" erőforráscsoport "rgname" erőforráscsoporthoz tartozó "" parancsfájl felülírásával.</span><span class="sxs-lookup"><span data-stu-id="f86b6-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="f86b6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f86b6-113">PARAMETERS</span></span>

### <span data-ttu-id="f86b6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f86b6-114">-AsJob</span></span>
<span data-ttu-id="f86b6-115">Futtassa a parancsmagot a háttérben, és adja vissza a projekt állapotát az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="f86b6-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="f86b6-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="f86b6-116">-CommandId</span></span>
<span data-ttu-id="f86b6-117">A Futtatás parancs azonosítója</span><span class="sxs-lookup"><span data-stu-id="f86b6-117">The run command ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f86b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f86b6-118">-DefaultProfile</span></span>
<span data-ttu-id="f86b6-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f86b6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f86b6-120">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="f86b6-120">-Parameter</span></span>
<span data-ttu-id="f86b6-121">A Futtatás parancs paraméterei.</span><span class="sxs-lookup"><span data-stu-id="f86b6-121">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f86b6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f86b6-122">-ResourceGroupName</span></span>
<span data-ttu-id="f86b6-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f86b6-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="f86b6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f86b6-124">-ResourceId</span></span>
<span data-ttu-id="f86b6-125">A VM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f86b6-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="f86b6-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="f86b6-126">-ScriptPath</span></span>
<span data-ttu-id="f86b6-127">A végrehajtandó parancsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f86b6-127">Path of the script to be executed.</span></span>  <span data-ttu-id="f86b6-128">Ha ezt az értéket adja meg, akkor a megadott parancsfájl felülírja a parancs alapértelmezett parancsfájlját.</span><span class="sxs-lookup"><span data-stu-id="f86b6-128">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f86b6-129">-VM</span><span class="sxs-lookup"><span data-stu-id="f86b6-129">-VM</span></span>
<span data-ttu-id="f86b6-130">A PS virtuális gép objektuma.</span><span class="sxs-lookup"><span data-stu-id="f86b6-130">The PS virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f86b6-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="f86b6-131">-VMName</span></span>
<span data-ttu-id="f86b6-132">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="f86b6-132">The name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f86b6-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f86b6-133">-Confirm</span></span>
<span data-ttu-id="f86b6-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f86b6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f86b6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f86b6-135">-WhatIf</span></span>
<span data-ttu-id="f86b6-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f86b6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f86b6-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f86b6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f86b6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f86b6-138">CommonParameters</span></span>
<span data-ttu-id="f86b6-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f86b6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f86b6-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f86b6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f86b6-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f86b6-141">INPUTS</span></span>

### <span data-ttu-id="f86b6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f86b6-142">System.String</span></span>

### <span data-ttu-id="f86b6-143">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f86b6-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f86b6-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f86b6-144">OUTPUTS</span></span>

### <span data-ttu-id="f86b6-145">Microsoft. Azure. commands. számítási. Automation. models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="f86b6-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="f86b6-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f86b6-146">NOTES</span></span>

## <span data-ttu-id="f86b6-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f86b6-147">RELATED LINKS</span></span>
