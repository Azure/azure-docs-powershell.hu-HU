---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 3c9e19c30d89d73a52be4defd18166f88b700889
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936273"
---
# <span data-ttu-id="378de-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="378de-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="378de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="378de-102">SYNOPSIS</span></span>
<span data-ttu-id="378de-103">Eltávolítja a hálózati felület konfigurációját a VMSS-ről.</span><span class="sxs-lookup"><span data-stu-id="378de-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="378de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="378de-104">SYNTAX</span></span>

### <span data-ttu-id="378de-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="378de-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="378de-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="378de-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="378de-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="378de-107">DESCRIPTION</span></span>
<span data-ttu-id="378de-108">A **Remove-AzVmssNetworkInterfaceConfiguration** parancsmag eltávolítja a hálózati felület konfigurációját a virtuális gép mérethalmazból (VMSS).</span><span class="sxs-lookup"><span data-stu-id="378de-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="378de-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="378de-109">EXAMPLES</span></span>

### <span data-ttu-id="378de-110">1. példa: Felületkonfiguráció eltávolítása</span><span class="sxs-lookup"><span data-stu-id="378de-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="378de-111">Az első parancs egy VMSS-t kap a Get-AzVmss parancsmag használatával, majd tárolja azt a $VMSS változóban.</span><span class="sxs-lookup"><span data-stu-id="378de-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="378de-112">A második parancs eltávolítja a ContosoVmssInterface02 nevű hálózati felület-konfigurációt a $VMSS.</span><span class="sxs-lookup"><span data-stu-id="378de-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="378de-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="378de-113">PARAMETERS</span></span>

### <span data-ttu-id="378de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378de-114">-DefaultProfile</span></span>
<span data-ttu-id="378de-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="378de-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="378de-116">-Id</span><span class="sxs-lookup"><span data-stu-id="378de-116">-Id</span></span>
<span data-ttu-id="378de-117">Annak a hálózatifelület-konfigurációnak az azonosítóját adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="378de-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="378de-118">-Name</span><span class="sxs-lookup"><span data-stu-id="378de-118">-Name</span></span>
<span data-ttu-id="378de-119">Annak a hálózatifelület-konfigurációnak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="378de-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="378de-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="378de-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="378de-121">A VMSS-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="378de-121">Specifies the VMSS object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="378de-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="378de-122">-Confirm</span></span>
<span data-ttu-id="378de-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="378de-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="378de-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="378de-124">-WhatIf</span></span>
<span data-ttu-id="378de-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="378de-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="378de-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="378de-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="378de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378de-127">CommonParameters</span></span>
<span data-ttu-id="378de-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="378de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378de-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="378de-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378de-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="378de-130">INPUTS</span></span>

### <span data-ttu-id="378de-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="378de-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="378de-132">System.String</span><span class="sxs-lookup"><span data-stu-id="378de-132">System.String</span></span>

## <span data-ttu-id="378de-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="378de-133">OUTPUTS</span></span>

### <span data-ttu-id="378de-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="378de-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="378de-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="378de-135">NOTES</span></span>

## <span data-ttu-id="378de-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="378de-136">RELATED LINKS</span></span>

[<span data-ttu-id="378de-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="378de-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="378de-138">Get-AzVms</span><span class="sxs-lookup"><span data-stu-id="378de-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


