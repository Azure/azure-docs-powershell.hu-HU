---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 58029017f4a6a272856f7badd6b09a9ba1f37ac3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667273"
---
# <span data-ttu-id="5d103-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d103-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="5d103-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d103-102">SYNOPSIS</span></span>
<span data-ttu-id="5d103-103">Hálózati illesztőfelület-konfiguráció eltávolítása egy VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d103-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="5d103-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d103-104">SYNTAX</span></span>

### <span data-ttu-id="5d103-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d103-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d103-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d103-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d103-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d103-107">DESCRIPTION</span></span>
<span data-ttu-id="5d103-108">A **Remove-AzVmssNetworkInterfaceConfiguration** parancsmag eltávolítja a hálózati felület konfigurációját egy virtuális gép Méretarányi készletéről (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5d103-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5d103-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5d103-109">EXAMPLES</span></span>

### <span data-ttu-id="5d103-110">1. példa: illesztőfelület-konfiguráció eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5d103-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="5d103-111">Az első parancs az Get-AzVmss parancsmag használatával kap egy VMSS, majd a $VMSS változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5d103-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="5d103-112">A második parancs eltávolítja a ContosoVmssInterface02 nevű hálózati felület konfigurációját a $VMSS készletből.</span><span class="sxs-lookup"><span data-stu-id="5d103-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="5d103-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d103-113">PARAMETERS</span></span>

### <span data-ttu-id="5d103-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d103-114">-DefaultProfile</span></span>
<span data-ttu-id="5d103-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d103-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d103-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5d103-116">-Id</span></span>
<span data-ttu-id="5d103-117">A parancsmag által eltávolított hálózati illesztőfelület-konfiguráció AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d103-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5d103-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d103-118">-Name</span></span>
<span data-ttu-id="5d103-119">Megadja a parancsmag által eltávolított hálózati kapcsolat konfigurációjának nevét.</span><span class="sxs-lookup"><span data-stu-id="5d103-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5d103-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5d103-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5d103-121">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d103-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="5d103-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5d103-122">-Confirm</span></span>
<span data-ttu-id="5d103-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5d103-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d103-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d103-124">-WhatIf</span></span>
<span data-ttu-id="5d103-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5d103-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d103-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d103-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d103-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d103-127">CommonParameters</span></span>
<span data-ttu-id="5d103-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d103-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d103-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5d103-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d103-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d103-130">INPUTS</span></span>

### <span data-ttu-id="5d103-131">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5d103-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="5d103-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5d103-132">System.String</span></span>

## <span data-ttu-id="5d103-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d103-133">OUTPUTS</span></span>

### <span data-ttu-id="5d103-134">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5d103-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5d103-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d103-135">NOTES</span></span>

## <span data-ttu-id="5d103-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d103-136">RELATED LINKS</span></span>

[<span data-ttu-id="5d103-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d103-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="5d103-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5d103-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


