---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 8f2d061fa67ed8e588ae162fbf7bd0a094ae6b1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495422"
---
# <span data-ttu-id="943fa-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="943fa-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="943fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="943fa-102">SYNOPSIS</span></span>
<span data-ttu-id="943fa-103">Hálózati illesztőfelület-konfiguráció eltávolítása egy VMSS.</span><span class="sxs-lookup"><span data-stu-id="943fa-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="943fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="943fa-104">SYNTAX</span></span>

### <span data-ttu-id="943fa-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="943fa-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="943fa-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="943fa-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Id] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="943fa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="943fa-107">DESCRIPTION</span></span>
<span data-ttu-id="943fa-108">A **Remove-AzureRmVmssNetworkInterfaceConfiguration** parancsmag eltávolítja a hálózati felület konfigurációját egy virtuális gép Méretarányi készletéről (VMSS).</span><span class="sxs-lookup"><span data-stu-id="943fa-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="943fa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="943fa-109">EXAMPLES</span></span>

### <span data-ttu-id="943fa-110">1. példa: illesztőfelület-konfiguráció eltávolítása</span><span class="sxs-lookup"><span data-stu-id="943fa-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="943fa-111">Az első parancs az Get-AzureRmVmss parancsmag használatával kap egy VMSS, majd a $VMSS változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="943fa-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="943fa-112">A második parancs eltávolítja a ContosoVmssInterface02 nevű hálózati felület konfigurációját a $VMSS készletből.</span><span class="sxs-lookup"><span data-stu-id="943fa-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="943fa-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="943fa-113">PARAMETERS</span></span>

### <span data-ttu-id="943fa-114">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="943fa-114">-Id</span></span>
<span data-ttu-id="943fa-115">A parancsmag által eltávolított hálózati illesztőfelület-konfiguráció AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="943fa-115">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="943fa-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="943fa-116">-Name</span></span>
<span data-ttu-id="943fa-117">Megadja a parancsmag által eltávolított hálózati kapcsolat konfigurációjának nevét.</span><span class="sxs-lookup"><span data-stu-id="943fa-117">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="943fa-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="943fa-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="943fa-119">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="943fa-119">Specifies the VMSS object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="943fa-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="943fa-120">-Confirm</span></span>
<span data-ttu-id="943fa-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="943fa-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="943fa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="943fa-122">-WhatIf</span></span>
<span data-ttu-id="943fa-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="943fa-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="943fa-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="943fa-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="943fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="943fa-125">CommonParameters</span></span>
<span data-ttu-id="943fa-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="943fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="943fa-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="943fa-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="943fa-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="943fa-128">INPUTS</span></span>

### <span data-ttu-id="943fa-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="943fa-129">None</span></span>
<span data-ttu-id="943fa-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="943fa-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="943fa-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="943fa-131">OUTPUTS</span></span>

## <span data-ttu-id="943fa-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="943fa-132">NOTES</span></span>

## <span data-ttu-id="943fa-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="943fa-133">RELATED LINKS</span></span>

[<span data-ttu-id="943fa-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="943fa-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="943fa-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="943fa-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


