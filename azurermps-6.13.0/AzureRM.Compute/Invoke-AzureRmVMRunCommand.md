---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 89d81387f8a97fe02f607ddc9d13d4645fc9688b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496335"
---
# <span data-ttu-id="df8aa-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="df8aa-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="df8aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="df8aa-103">A Futtatás parancs a VM-ben.</span><span class="sxs-lookup"><span data-stu-id="df8aa-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df8aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df8aa-104">SYNTAX</span></span>

### <span data-ttu-id="df8aa-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df8aa-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df8aa-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="df8aa-106">ResourceIdParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df8aa-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="df8aa-107">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df8aa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="df8aa-108">DESCRIPTION</span></span>
<span data-ttu-id="df8aa-109">Indítsa el a Futtatás parancsot a VM-ben.</span><span class="sxs-lookup"><span data-stu-id="df8aa-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="df8aa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="df8aa-110">EXAMPLES</span></span>

### <span data-ttu-id="df8aa-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="df8aa-111">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="df8aa-112">Hivatkozhat a RunPowerShellScript Futtatás parancsára a "sample.ps1" és a "vmname" erőforráscsoport "rgname" erőforráscsoporthoz tartozó "" parancsfájl felülírásával.</span><span class="sxs-lookup"><span data-stu-id="df8aa-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="df8aa-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df8aa-113">PARAMETERS</span></span>

### <span data-ttu-id="df8aa-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df8aa-114">-AsJob</span></span>
<span data-ttu-id="df8aa-115">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="df8aa-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="df8aa-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="df8aa-116">-CommandId</span></span>
<span data-ttu-id="df8aa-117">A Futtatás parancs azonosítója</span><span class="sxs-lookup"><span data-stu-id="df8aa-117">The run command id.</span></span>

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

### <span data-ttu-id="df8aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df8aa-118">-DefaultProfile</span></span>
<span data-ttu-id="df8aa-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df8aa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df8aa-120">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="df8aa-120">-Parameter</span></span>
<span data-ttu-id="df8aa-121">A Futtatás parancs paraméterei.</span><span class="sxs-lookup"><span data-stu-id="df8aa-121">The run command parameters.</span></span>

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

### <span data-ttu-id="df8aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df8aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="df8aa-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="df8aa-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df8aa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df8aa-124">-ResourceId</span></span>
<span data-ttu-id="df8aa-125">A VM erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="df8aa-125">The resource id for the VM</span></span>

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

### <span data-ttu-id="df8aa-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="df8aa-126">-ScriptPath</span></span>
<span data-ttu-id="df8aa-127">A végrehajtandó parancsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="df8aa-127">Path of the script to be executed.</span></span>  <span data-ttu-id="df8aa-128">Ha ezt az értéket adja meg, akkor a megadott parancsfájl felülírja a parancs alapértelmezett parancsfájlját.</span><span class="sxs-lookup"><span data-stu-id="df8aa-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="df8aa-129">-VM</span><span class="sxs-lookup"><span data-stu-id="df8aa-129">-VM</span></span>
<span data-ttu-id="df8aa-130">A PS virtuális gép objektuma.</span><span class="sxs-lookup"><span data-stu-id="df8aa-130">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="df8aa-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="df8aa-131">-VMName</span></span>
<span data-ttu-id="df8aa-132">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="df8aa-132">The name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df8aa-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df8aa-133">-Confirm</span></span>
<span data-ttu-id="df8aa-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df8aa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df8aa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df8aa-135">-WhatIf</span></span>
<span data-ttu-id="df8aa-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="df8aa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df8aa-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df8aa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df8aa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df8aa-138">CommonParameters</span></span>
<span data-ttu-id="df8aa-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df8aa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df8aa-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df8aa-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df8aa-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df8aa-141">INPUTS</span></span>

### <span data-ttu-id="df8aa-142">System. String</span><span class="sxs-lookup"><span data-stu-id="df8aa-142">System.String</span></span>

### <span data-ttu-id="df8aa-143">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="df8aa-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="df8aa-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df8aa-144">OUTPUTS</span></span>

### <span data-ttu-id="df8aa-145">Microsoft. Azure. commands. számítási. Automation. models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="df8aa-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="df8aa-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df8aa-146">NOTES</span></span>

## <span data-ttu-id="df8aa-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df8aa-147">RELATED LINKS</span></span>
