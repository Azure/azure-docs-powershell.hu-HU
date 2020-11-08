---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: a63f945c5af1d5b979a0d8b70546d48233d14f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186793"
---
# <span data-ttu-id="bbbdc-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="bbbdc-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="bbbdc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bbbdc-102">SYNOPSIS</span></span>
<span data-ttu-id="bbbdc-103">A Futtatás parancs a virtuális gép méretarány beállítása VM.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="bbbdc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bbbdc-104">SYNTAX</span></span>

### <span data-ttu-id="bbbdc-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bbbdc-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbbdc-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="bbbdc-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbbdc-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="bbbdc-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbbdc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bbbdc-108">DESCRIPTION</span></span>
<span data-ttu-id="bbbdc-109">Hivatkozhat a Futtatás parancsra a Virtual Machine Scale set VM alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="bbbdc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bbbdc-110">EXAMPLES</span></span>

### <span data-ttu-id="bbbdc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bbbdc-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="bbbdc-112">A RunPowerShellScript Futtatás parancsával megnyithatja a "sample.ps1" parancsfájlt, és a "vmssname" erőforráscsoport "rgname" erőforráscsoporthoz tartozó "0" VM-es AZONOSÍTÓJÚ paramétereit.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="bbbdc-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="bbbdc-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="bbbdc-114">A RunPowerShellScript Futtatás parancsával megnyithatja a "sample.ps1" parancsfájlt, és a "vmssname" erőforráscsoport "rgname" erőforráscsoporthoz tartozó "0" VM-es AZONOSÍTÓJÚ paramétereit.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="bbbdc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bbbdc-115">PARAMETERS</span></span>

### <span data-ttu-id="bbbdc-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbbdc-116">-AsJob</span></span>
<span data-ttu-id="bbbdc-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bbbdc-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbbdc-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="bbbdc-118">-CommandId</span></span>
<span data-ttu-id="bbbdc-119">A Futtatás parancs azonosítója</span><span class="sxs-lookup"><span data-stu-id="bbbdc-119">The run command id.</span></span>

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

### <span data-ttu-id="bbbdc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbbdc-120">-DefaultProfile</span></span>
<span data-ttu-id="bbbdc-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbbdc-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="bbbdc-122">-InstanceId</span></span>
<span data-ttu-id="bbbdc-123">A virtuálisgép-készlet virtuális gép példányának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-123">The instance ID of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbbdc-124">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="bbbdc-124">-Parameter</span></span>
<span data-ttu-id="bbbdc-125">A Futtatás parancs paraméterei.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-125">The run command parameters.</span></span>

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

### <span data-ttu-id="bbbdc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbbdc-126">-ResourceGroupName</span></span>
<span data-ttu-id="bbbdc-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="bbbdc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbbdc-128">-ResourceId</span></span>
<span data-ttu-id="bbbdc-129">A virtuális gép méretarányos VM-készletének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="bbbdc-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="bbbdc-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="bbbdc-130">-ScriptPath</span></span>
<span data-ttu-id="bbbdc-131">A végrehajtandó parancsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-131">Path of the script to be executed.</span></span>  <span data-ttu-id="bbbdc-132">Ha ezt az értéket adja meg, akkor a megadott parancsfájl felülírja a parancs alapértelmezett parancsfájlját.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-132">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="bbbdc-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="bbbdc-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="bbbdc-134">A PS Virtual Machine Scale set VM objektuma.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-134">The PS Virtual Machine Scale Set VM Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbbdc-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bbbdc-135">-VMScaleSetName</span></span>
<span data-ttu-id="bbbdc-136">A virtuális gép méretarány beállítása VM.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="bbbdc-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bbbdc-137">-Confirm</span></span>
<span data-ttu-id="bbbdc-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbbdc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbbdc-139">-WhatIf</span></span>
<span data-ttu-id="bbbdc-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbbdc-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbbdc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbbdc-142">CommonParameters</span></span>
<span data-ttu-id="bbbdc-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bbbdc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbbdc-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbbdc-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbbdc-145">INPUTS</span></span>

### <span data-ttu-id="bbbdc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="bbbdc-146">System.String</span></span>

### <span data-ttu-id="bbbdc-147">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="bbbdc-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="bbbdc-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbbdc-148">OUTPUTS</span></span>

### <span data-ttu-id="bbbdc-149">Microsoft. Azure. commands. számítási. Automation. models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="bbbdc-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="bbbdc-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bbbdc-150">NOTES</span></span>

## <span data-ttu-id="bbbdc-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbbdc-151">RELATED LINKS</span></span>