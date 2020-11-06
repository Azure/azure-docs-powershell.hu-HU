---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 4c1bc282b4a5aa0bf8c324ec523b5c823ce3cd14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497676"
---
# <span data-ttu-id="1e2c3-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1e2c3-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="1e2c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="1e2c3-103">Elindítja a VMSS vagy a virtuális gépeket a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e2c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e2c3-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e2c3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e2c3-105">DESCRIPTION</span></span>
<span data-ttu-id="1e2c3-106">A **Start-AzureRmVmss** parancsmag a Virtual Machine Scale set (VMSS) vagy a virtuális gépek egy halmazán belül minden virtuális gépet elindít.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="1e2c3-107">A *InstanceId* paraméterrel kiválaszthatja a virtuális gépek halmazát.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="1e2c3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1e2c3-108">EXAMPLES</span></span>

### <span data-ttu-id="1e2c3-109">1. példa: a virtuális gépek meghatározott halmazának indítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="1e2c3-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="1e2c3-110">Ez a parancs a ContosoVMSS nevű VMSS tartozó példánynév karakterláncban meghatározott virtuális gépek meghatározott halmazát indítja el.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="1e2c3-111">2. példa: az összes virtuális gép elindítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="1e2c3-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="1e2c3-112">Ez a parancs elindítja az összes olyan virtuális gépet, amely a ContosoVMSS nevű VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="1e2c3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e2c3-113">PARAMETERS</span></span>

### <span data-ttu-id="1e2c3-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1e2c3-114">-InstanceId</span></span>
<span data-ttu-id="1e2c3-115">Karakterláncként adja meg a parancsmag által elinduló példányok AZONOSÍTÓját vagy azonosítóit.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-115">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="1e2c3-116">Például: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="1e2c3-116">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2c3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e2c3-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e2c3-118">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-118">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2c3-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1e2c3-119">-VMScaleSetName</span></span>
<span data-ttu-id="1e2c3-120">Annak a VMSS a nevét adja meg, amely a parancsmag által a virtuális gépeket indítja el.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-120">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2c3-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1e2c3-121">-Confirm</span></span>
<span data-ttu-id="1e2c3-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e2c3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e2c3-123">-WhatIf</span></span>
<span data-ttu-id="1e2c3-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e2c3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e2c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e2c3-126">CommonParameters</span></span>
<span data-ttu-id="1e2c3-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e2c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e2c3-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e2c3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e2c3-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e2c3-129">INPUTS</span></span>

### <span data-ttu-id="1e2c3-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="1e2c3-130">None</span></span>
<span data-ttu-id="1e2c3-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e2c3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e2c3-132">OUTPUTS</span></span>

###  
<span data-ttu-id="1e2c3-133">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1e2c3-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e2c3-134">NOTES</span></span>

## <span data-ttu-id="1e2c3-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e2c3-135">RELATED LINKS</span></span>

[<span data-ttu-id="1e2c3-136">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1e2c3-136">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="1e2c3-137">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1e2c3-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="1e2c3-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1e2c3-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="1e2c3-139">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1e2c3-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="1e2c3-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1e2c3-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="1e2c3-141">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1e2c3-141">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="1e2c3-142">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1e2c3-142">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


