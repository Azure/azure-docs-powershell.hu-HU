---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 33847b9a86d5fa39511102e964f8f2a63fce6960
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210071"
---
# <span data-ttu-id="7da74-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="7da74-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="7da74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7da74-102">SYNOPSIS</span></span>
<span data-ttu-id="7da74-103">Egy VMSS virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7da74-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="7da74-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7da74-104">SYNTAX</span></span>

### <span data-ttu-id="7da74-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7da74-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7da74-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="7da74-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7da74-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7da74-107">DESCRIPTION</span></span>
<span data-ttu-id="7da74-108">A **Get-AzVmssVM** parancsmag egy virtuális gép méretkészletének (VMSS) modellnézetét és példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7da74-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="7da74-109">A modellnézet a virtuális gép felhasználó által megadott tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="7da74-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="7da74-110">A példánynézet a virtuális gép példányszintű állapota.</span><span class="sxs-lookup"><span data-stu-id="7da74-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="7da74-111">Adja meg *az Állapot* paramétert úgy, hogy csak a virtuális gép példánynézetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7da74-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="7da74-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7da74-112">EXAMPLES</span></span>

### <span data-ttu-id="7da74-113">1. példa: VMSS virtuális gép tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="7da74-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="7da74-114">Ez a parancs a VMSS virtuális gép tulajdonságait kapja meg, amely a Group0001 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="7da74-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="7da74-115">Mivel a parancs nem adja meg a *InstanceView* kapcsoló paramétert, a parancsmag a virtuális gép modellnézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7da74-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="7da74-116">2. példa: A VMSS virtuális gép modellnézet-tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="7da74-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="7da74-117">Ez a parancs a VMSS virtuális gép tulajdonságait kapja meg, amely a Group002 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="7da74-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="7da74-118">A parancs a változóban tárolt példányazonosítót $ID, amelyhez a modellnézetet meg kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="7da74-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="7da74-119">3. példa: A VMSS virtuális gép példánynézet-tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="7da74-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="7da74-120">Ez a parancs a VMSS virtuális gép tulajdonságait kapja meg, amely a Group002 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="7da74-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="7da74-121">Mivel a parancs a *InstanceView* kapcsoló paramétert adja meg, a parancsmag a virtuális gép példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7da74-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="7da74-122">A parancs a példányazonosítót abban a változóban $ID, amelyhez meg kell kapnia a példánynézetet.</span><span class="sxs-lookup"><span data-stu-id="7da74-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="7da74-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7da74-123">PARAMETERS</span></span>

### <span data-ttu-id="7da74-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da74-124">-DefaultProfile</span></span>
<span data-ttu-id="7da74-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7da74-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7da74-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="7da74-126">-InstanceId</span></span>
<span data-ttu-id="7da74-127">Azt a példányazonosítót adja meg, amelynek a modellnézetét le kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="7da74-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da74-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="7da74-128">-InstanceView</span></span>
<span data-ttu-id="7da74-129">Azt jelzi, hogy ez a parancsmag csak a virtuális gép példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7da74-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7da74-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da74-130">-ResourceGroupName</span></span>
<span data-ttu-id="7da74-131">A VMSS erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7da74-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da74-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7da74-132">-VMScaleSetName</span></span>
<span data-ttu-id="7da74-133">A VMSS nevének fakása.</span><span class="sxs-lookup"><span data-stu-id="7da74-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da74-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da74-134">CommonParameters</span></span>
<span data-ttu-id="7da74-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da74-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da74-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7da74-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da74-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7da74-137">INPUTS</span></span>

### <span data-ttu-id="7da74-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7da74-138">System.String</span></span>

## <span data-ttu-id="7da74-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7da74-139">OUTPUTS</span></span>

### <span data-ttu-id="7da74-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="7da74-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="7da74-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7da74-141">NOTES</span></span>

## <span data-ttu-id="7da74-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7da74-142">RELATED LINKS</span></span>

[<span data-ttu-id="7da74-143">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="7da74-143">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="7da74-144">Get-AzVms</span><span class="sxs-lookup"><span data-stu-id="7da74-144">Get-AzVmss</span></span>](./Get-AzVmss.md)


