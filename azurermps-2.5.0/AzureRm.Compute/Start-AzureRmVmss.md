---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2135b6244453cb7d958871c23b64016404d02502
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850418"
---
# <span data-ttu-id="1f4ad-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f4ad-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="1f4ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f4ad-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4ad-103">Elindítja a VMSS vagy a virtuális gépeket a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f4ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f4ad-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f4ad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f4ad-105">DESCRIPTION</span></span>
<span data-ttu-id="1f4ad-106">A **Start-AzureRmVmss** parancsmag a Virtual Machine Scale set (VMSS) vagy a virtuális gépek egy halmazán belül minden virtuális gépet elindít.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="1f4ad-107">A *InstanceId* paraméterrel kiválaszthatja a virtuális gépek halmazát.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="1f4ad-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1f4ad-108">EXAMPLES</span></span>

### <span data-ttu-id="1f4ad-109">1. példa: a virtuális gépek meghatározott halmazának indítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="1f4ad-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="1f4ad-110">Ez a parancs a ContosoVMSS nevű VMSS tartozó példánynév karakterláncban meghatározott virtuális gépek meghatározott halmazát indítja el.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="1f4ad-111">2. példa: az összes virtuális gép elindítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="1f4ad-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="1f4ad-112">Ez a parancs elindítja az összes olyan virtuális gépet, amely a ContosoVMSS nevű VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="1f4ad-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f4ad-113">PARAMETERS</span></span>

### <span data-ttu-id="1f4ad-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f4ad-114">-AsJob</span></span>
<span data-ttu-id="1f4ad-115">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1f4ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4ad-116">-DefaultProfile</span></span>
<span data-ttu-id="1f4ad-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f4ad-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1f4ad-118">-InstanceId</span></span>
<span data-ttu-id="1f4ad-119">Karakterláncként adja meg a parancsmag által elinduló példányok AZONOSÍTÓját vagy azonosítóit.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="1f4ad-120">Például: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="1f4ad-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="1f4ad-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f4ad-121">-ResourceGroupName</span></span>
<span data-ttu-id="1f4ad-122">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="1f4ad-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1f4ad-123">-VMScaleSetName</span></span>
<span data-ttu-id="1f4ad-124">Annak a VMSS a nevét adja meg, amely a parancsmag által a virtuális gépeket indítja el.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="1f4ad-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1f4ad-125">-Confirm</span></span>
<span data-ttu-id="1f4ad-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f4ad-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f4ad-127">-WhatIf</span></span>
<span data-ttu-id="1f4ad-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f4ad-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f4ad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4ad-130">CommonParameters</span></span>
<span data-ttu-id="1f4ad-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f4ad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4ad-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f4ad-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4ad-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f4ad-133">INPUTS</span></span>

### <span data-ttu-id="1f4ad-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="1f4ad-134">None</span></span>
<span data-ttu-id="1f4ad-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f4ad-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f4ad-136">OUTPUTS</span></span>

###  
<span data-ttu-id="1f4ad-137">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1f4ad-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1f4ad-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f4ad-138">NOTES</span></span>

## <span data-ttu-id="1f4ad-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f4ad-139">RELATED LINKS</span></span>

[<span data-ttu-id="1f4ad-140">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f4ad-140">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="1f4ad-141">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f4ad-141">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="1f4ad-142">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f4ad-142">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="1f4ad-143">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f4ad-143">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="1f4ad-144">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f4ad-144">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="1f4ad-145">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f4ad-145">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="1f4ad-146">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f4ad-146">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


