---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: d3677191bb3a196b97dcb8ff6c5b62b4aafd3a8b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842474"
---
# <span data-ttu-id="ea875-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ea875-101">Start-AzVmss</span></span>

## <span data-ttu-id="ea875-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea875-102">SYNOPSIS</span></span>
<span data-ttu-id="ea875-103">Elindítja a VMSS vagy a virtuális gépeket a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="ea875-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="ea875-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea875-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea875-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea875-105">DESCRIPTION</span></span>
<span data-ttu-id="ea875-106">A **Start-AzVmss** parancsmag a Virtual Machine Scale set (VMSS) vagy a virtuális gépek egy halmazán belül minden virtuális gépet elindít.</span><span class="sxs-lookup"><span data-stu-id="ea875-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="ea875-107">A *InstanceId* paraméterrel kiválaszthatja a virtuális gépek halmazát.</span><span class="sxs-lookup"><span data-stu-id="ea875-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="ea875-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ea875-108">EXAMPLES</span></span>

### <span data-ttu-id="ea875-109">1. példa: a virtuális gépek meghatározott halmazának indítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="ea875-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="ea875-110">Ez a parancs a ContosoVMSS nevű VMSS tartozó példánynév karakterláncban meghatározott virtuális gépek meghatározott halmazát indítja el.</span><span class="sxs-lookup"><span data-stu-id="ea875-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="ea875-111">2. példa: az összes virtuális gép elindítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="ea875-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ea875-112">Ez a parancs elindítja az összes olyan virtuális gépet, amely a ContosoVMSS nevű VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="ea875-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="ea875-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea875-113">PARAMETERS</span></span>

### <span data-ttu-id="ea875-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea875-114">-AsJob</span></span>
<span data-ttu-id="ea875-115">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="ea875-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ea875-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea875-116">-DefaultProfile</span></span>
<span data-ttu-id="ea875-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea875-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea875-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="ea875-118">-InstanceId</span></span>
<span data-ttu-id="ea875-119">Karakterláncként adja meg a parancsmag által elinduló példányok AZONOSÍTÓját vagy azonosítóit.</span><span class="sxs-lookup"><span data-stu-id="ea875-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="ea875-120">Például: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="ea875-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="ea875-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea875-121">-ResourceGroupName</span></span>
<span data-ttu-id="ea875-122">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea875-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="ea875-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ea875-123">-VMScaleSetName</span></span>
<span data-ttu-id="ea875-124">Annak a VMSS a nevét adja meg, amely a parancsmag által a virtuális gépeket indítja el.</span><span class="sxs-lookup"><span data-stu-id="ea875-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="ea875-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ea875-125">-Confirm</span></span>
<span data-ttu-id="ea875-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ea875-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea875-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea875-127">-WhatIf</span></span>
<span data-ttu-id="ea875-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ea875-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea875-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea875-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea875-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea875-130">CommonParameters</span></span>
<span data-ttu-id="ea875-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea875-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea875-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea875-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea875-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea875-133">INPUTS</span></span>

### <span data-ttu-id="ea875-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="ea875-134">None</span></span>
<span data-ttu-id="ea875-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ea875-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea875-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea875-136">OUTPUTS</span></span>

###  
<span data-ttu-id="ea875-137">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ea875-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ea875-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea875-138">NOTES</span></span>

## <span data-ttu-id="ea875-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea875-139">RELATED LINKS</span></span>

[<span data-ttu-id="ea875-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ea875-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="ea875-141">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="ea875-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="ea875-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ea875-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="ea875-143">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="ea875-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="ea875-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ea875-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="ea875-145">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ea875-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="ea875-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ea875-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


