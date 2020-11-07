---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 7d3c27ad8dacb288aeb0d15235aacc48405b8a6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680182"
---
# <span data-ttu-id="75a7d-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="75a7d-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="75a7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="75a7d-103">A Futtatás parancs a VM-ben.</span><span class="sxs-lookup"><span data-stu-id="75a7d-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75a7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75a7d-104">SYNTAX</span></span>

### <span data-ttu-id="75a7d-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="75a7d-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75a7d-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="75a7d-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75a7d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="75a7d-107">DESCRIPTION</span></span>
<span data-ttu-id="75a7d-108">Indítsa el a Futtatás parancsot a VM-ben.</span><span class="sxs-lookup"><span data-stu-id="75a7d-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="75a7d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="75a7d-109">EXAMPLES</span></span>

### <span data-ttu-id="75a7d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="75a7d-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="75a7d-111">Hivatkozhat a RunPowerShellScript Futtatás parancsára a "sample.ps1" és a "vmname" erőforráscsoport "rgname" erőforráscsoporthoz tartozó "" parancsfájl felülírásával.</span><span class="sxs-lookup"><span data-stu-id="75a7d-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="75a7d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75a7d-112">PARAMETERS</span></span>

### <span data-ttu-id="75a7d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75a7d-113">-AsJob</span></span>
<span data-ttu-id="75a7d-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="75a7d-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a7d-115">-CommandId</span><span class="sxs-lookup"><span data-stu-id="75a7d-115">-CommandId</span></span>
<span data-ttu-id="75a7d-116">A Futtatás parancs azonosítója</span><span class="sxs-lookup"><span data-stu-id="75a7d-116">The run command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a7d-117">-DefaultProfile</span></span>
<span data-ttu-id="75a7d-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75a7d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a7d-119">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="75a7d-119">-Parameter</span></span>
<span data-ttu-id="75a7d-120">A Futtatás parancs paraméterei.</span><span class="sxs-lookup"><span data-stu-id="75a7d-120">The run command parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a7d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a7d-121">-ResourceGroupName</span></span>
<span data-ttu-id="75a7d-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="75a7d-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a7d-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="75a7d-123">-ScriptPath</span></span>
<span data-ttu-id="75a7d-124">A végrehajtandó parancsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="75a7d-124">Path of the script to be executed.</span></span>  <span data-ttu-id="75a7d-125">Ha ezt az értéket adja meg, akkor a megadott parancsfájl felülírja a parancs alapértelmezett parancsfájlját.</span><span class="sxs-lookup"><span data-stu-id="75a7d-125">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a7d-126">-VM</span><span class="sxs-lookup"><span data-stu-id="75a7d-126">-VM</span></span>
<span data-ttu-id="75a7d-127">A PS virtuális gép objektuma.</span><span class="sxs-lookup"><span data-stu-id="75a7d-127">The PS virtual Machine Object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75a7d-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="75a7d-128">-VMName</span></span>
<span data-ttu-id="75a7d-129">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="75a7d-129">The name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a7d-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="75a7d-130">-Confirm</span></span>
<span data-ttu-id="75a7d-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="75a7d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a7d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75a7d-132">-WhatIf</span></span>
<span data-ttu-id="75a7d-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="75a7d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75a7d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75a7d-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a7d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a7d-135">CommonParameters</span></span>
<span data-ttu-id="75a7d-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75a7d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a7d-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a7d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a7d-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75a7d-138">INPUTS</span></span>

### <span data-ttu-id="75a7d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="75a7d-139">System.String</span></span>
<span data-ttu-id="75a7d-140">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="75a7d-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="75a7d-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75a7d-141">OUTPUTS</span></span>

### <span data-ttu-id="75a7d-142">Microsoft. Azure. commands. számítási. Automation. models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="75a7d-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="75a7d-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75a7d-143">NOTES</span></span>

## <span data-ttu-id="75a7d-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75a7d-144">RELATED LINKS</span></span>
