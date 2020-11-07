---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 349c4590116c05c28c1fc1220e98e946519cd8f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679606"
---
# <span data-ttu-id="c50c5-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c50c5-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="c50c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c50c5-102">SYNOPSIS</span></span>
<span data-ttu-id="c50c5-103">Egy virtuális gépről eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="c50c5-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c50c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c50c5-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c50c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c50c5-105">DESCRIPTION</span></span>
<span data-ttu-id="c50c5-106">A **Remove-AzureRmVMNetworkInterface** parancsmag egy virtuális gépről eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="c50c5-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="c50c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c50c5-107">EXAMPLES</span></span>

## <span data-ttu-id="c50c5-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c50c5-108">PARAMETERS</span></span>

### <span data-ttu-id="c50c5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c50c5-109">-DefaultProfile</span></span>
<span data-ttu-id="c50c5-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c50c5-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c50c5-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="c50c5-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="c50c5-112">A parancsmag által eltávolított hálózati illesztőfelület-azonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c50c5-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c50c5-113">-VM</span><span class="sxs-lookup"><span data-stu-id="c50c5-113">-VM</span></span>
<span data-ttu-id="c50c5-114">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="c50c5-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="c50c5-115">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c50c5-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c50c5-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c50c5-116">-Confirm</span></span>
<span data-ttu-id="c50c5-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c50c5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c50c5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c50c5-118">-WhatIf</span></span>
<span data-ttu-id="c50c5-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c50c5-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c50c5-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c50c5-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c50c5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c50c5-121">CommonParameters</span></span>
<span data-ttu-id="c50c5-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c50c5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c50c5-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c50c5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c50c5-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c50c5-124">INPUTS</span></span>

### <span data-ttu-id="c50c5-125">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c50c5-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c50c5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c50c5-126">OUTPUTS</span></span>

### <span data-ttu-id="c50c5-127">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c50c5-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c50c5-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c50c5-128">NOTES</span></span>

## <span data-ttu-id="c50c5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c50c5-129">RELATED LINKS</span></span>

[<span data-ttu-id="c50c5-130">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c50c5-130">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


