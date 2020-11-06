---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 44022fe8ea12c8f341952bd023aa41bf4ead92c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499172"
---
# <span data-ttu-id="faff4-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faff4-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="faff4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="faff4-102">SYNOPSIS</span></span>
<span data-ttu-id="faff4-103">Frissíti egy VMSS állapotát.</span><span class="sxs-lookup"><span data-stu-id="faff4-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faff4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="faff4-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faff4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="faff4-105">DESCRIPTION</span></span>
<span data-ttu-id="faff4-106">Az **Update-AzureRmVmss** parancsmag a virtuálisgép-készlet (VMSS) állapotát egy helyi VMSS objektum állapotára frissíti.</span><span class="sxs-lookup"><span data-stu-id="faff4-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="faff4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="faff4-107">EXAMPLES</span></span>

### <span data-ttu-id="faff4-108">Példa 1: egy VMSS állapotának frissítése egy helyi VMSS-objektum állapotával.</span><span class="sxs-lookup"><span data-stu-id="faff4-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="faff4-109">Ez a parancs frissíti a Group001 nevű VMSS001 nevű VMSS állapotát a LocalVMSS nevű helyi VMSS-objektum állapotával.</span><span class="sxs-lookup"><span data-stu-id="faff4-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="faff4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="faff4-110">PARAMETERS</span></span>

### <span data-ttu-id="faff4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faff4-111">-DefaultProfile</span></span>
<span data-ttu-id="faff4-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="faff4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faff4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faff4-113">-ResourceGroupName</span></span>
<span data-ttu-id="faff4-114">Annak a csoportnak a neve, amelyhez a VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="faff4-114">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faff4-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="faff4-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="faff4-116">Helyi VMSS-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="faff4-116">Specifies a local VMSS object.</span></span>
<span data-ttu-id="faff4-117">VMSS objektum beolvasásához használja az Get-AzureRmVmss parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="faff4-117">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="faff4-118">Ez a virtuálisgép-objektum a VMSS frissített állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="faff4-118">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faff4-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="faff4-119">-VMScaleSetName</span></span>
<span data-ttu-id="faff4-120">Annak a VMSS a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="faff4-120">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faff4-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="faff4-121">-Confirm</span></span>
<span data-ttu-id="faff4-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="faff4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faff4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faff4-123">-WhatIf</span></span>
<span data-ttu-id="faff4-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="faff4-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="faff4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="faff4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faff4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faff4-126">CommonParameters</span></span>
<span data-ttu-id="faff4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="faff4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faff4-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faff4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faff4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="faff4-129">INPUTS</span></span>

## <span data-ttu-id="faff4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="faff4-130">OUTPUTS</span></span>

## <span data-ttu-id="faff4-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="faff4-131">NOTES</span></span>

## <span data-ttu-id="faff4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="faff4-132">RELATED LINKS</span></span>

[<span data-ttu-id="faff4-133">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faff4-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="faff4-134">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faff4-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="faff4-135">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faff4-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="faff4-136">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faff4-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="faff4-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faff4-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="faff4-138">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faff4-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="faff4-139">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faff4-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


