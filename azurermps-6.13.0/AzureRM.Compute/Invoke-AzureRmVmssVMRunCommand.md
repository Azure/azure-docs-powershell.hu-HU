---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVmssVMRunCommand.md
ms.openlocfilehash: 1c1cdeff1e1a73de6947855922a4fed45fe387e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680399"
---
# <span data-ttu-id="8896d-101">Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="8896d-101">Invoke-AzureRmVmssVMRunCommand</span></span>

## <span data-ttu-id="8896d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8896d-102">SYNOPSIS</span></span>
<span data-ttu-id="8896d-103">A Futtatás parancs a virtuális gép méretarány beállítása VM.</span><span class="sxs-lookup"><span data-stu-id="8896d-103">Run command on the Virtual Machine Scale Set VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8896d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8896d-104">SYNTAX</span></span>

### <span data-ttu-id="8896d-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8896d-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8896d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="8896d-106">ResourceIdParameter</span></span>
```
Invoke-AzureRmVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8896d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="8896d-107">ObjectParameter</span></span>
```
Invoke-AzureRmVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8896d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8896d-108">DESCRIPTION</span></span>
<span data-ttu-id="8896d-109">Hivatkozhat a Futtatás parancsra a Virtual Machine Scale set VM alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="8896d-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="8896d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8896d-110">EXAMPLES</span></span>

### <span data-ttu-id="8896d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8896d-111">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="8896d-112">A RunPowerShellScript Futtatás parancsával megnyithatja a "sample.ps1" parancsfájlt, és a "vmssname" erőforráscsoport "rgname" erőforráscsoporthoz tartozó "0" VM-es AZONOSÍTÓJÚ paramétereit.</span><span class="sxs-lookup"><span data-stu-id="8896d-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="8896d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8896d-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzureRmVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="8896d-114">A RunPowerShellScript Futtatás parancsával megnyithatja a "sample.ps1" parancsfájlt, és a "vmssname" erőforráscsoport "rgname" erőforráscsoporthoz tartozó "0" VM-es AZONOSÍTÓJÚ paramétereit.</span><span class="sxs-lookup"><span data-stu-id="8896d-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="8896d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8896d-115">PARAMETERS</span></span>

### <span data-ttu-id="8896d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8896d-116">-AsJob</span></span>
<span data-ttu-id="8896d-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8896d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8896d-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="8896d-118">-CommandId</span></span>
<span data-ttu-id="8896d-119">A Futtatás parancs azonosítója</span><span class="sxs-lookup"><span data-stu-id="8896d-119">The run command id.</span></span>

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

### <span data-ttu-id="8896d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8896d-120">-DefaultProfile</span></span>
<span data-ttu-id="8896d-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8896d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8896d-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="8896d-122">-InstanceId</span></span>
<span data-ttu-id="8896d-123">A virtuálisgép-készlet virtuális gép példányának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8896d-123">The instance ID of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="8896d-124">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="8896d-124">-Parameter</span></span>
<span data-ttu-id="8896d-125">A Futtatás parancs paraméterei.</span><span class="sxs-lookup"><span data-stu-id="8896d-125">The run command parameters.</span></span>

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

### <span data-ttu-id="8896d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8896d-126">-ResourceGroupName</span></span>
<span data-ttu-id="8896d-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8896d-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="8896d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8896d-128">-ResourceId</span></span>
<span data-ttu-id="8896d-129">A virtuális gép méretarányos VM-készletének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8896d-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="8896d-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="8896d-130">-ScriptPath</span></span>
<span data-ttu-id="8896d-131">A végrehajtandó parancsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="8896d-131">Path of the script to be executed.</span></span>  <span data-ttu-id="8896d-132">Ha ezt az értéket adja meg, akkor a megadott parancsfájl felülírja a parancs alapértelmezett parancsfájlját.</span><span class="sxs-lookup"><span data-stu-id="8896d-132">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="8896d-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="8896d-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="8896d-134">A PS Virtual Machine Scale set VM objektuma.</span><span class="sxs-lookup"><span data-stu-id="8896d-134">The PS Virtual Machine Scale Set VM Object.</span></span>

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

### <span data-ttu-id="8896d-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8896d-135">-VMScaleSetName</span></span>
<span data-ttu-id="8896d-136">A virtuális gép méretarány beállítása VM.</span><span class="sxs-lookup"><span data-stu-id="8896d-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="8896d-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8896d-137">-Confirm</span></span>
<span data-ttu-id="8896d-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8896d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8896d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8896d-139">-WhatIf</span></span>
<span data-ttu-id="8896d-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8896d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8896d-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8896d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8896d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8896d-142">CommonParameters</span></span>
<span data-ttu-id="8896d-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8896d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8896d-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8896d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8896d-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8896d-145">INPUTS</span></span>

### <span data-ttu-id="8896d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8896d-146">System.String</span></span>

### <span data-ttu-id="8896d-147">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="8896d-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="8896d-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8896d-148">OUTPUTS</span></span>

### <span data-ttu-id="8896d-149">Microsoft. Azure. commands. számítási. Automation. models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="8896d-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="8896d-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8896d-150">NOTES</span></span>

## <span data-ttu-id="8896d-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8896d-151">RELATED LINKS</span></span>
