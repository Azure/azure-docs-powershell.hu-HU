---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 6582b8d0a141522e6ac8bb4dad23f1da5e31000d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850446"
---
# <span data-ttu-id="fdf63-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fdf63-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="fdf63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fdf63-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf63-103">A VMSS vagy egy virtuális gép újraindítása a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="fdf63-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdf63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fdf63-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdf63-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fdf63-105">DESCRIPTION</span></span>
<span data-ttu-id="fdf63-106">Az **Újraindítás-AzureRmVmss** parancsmag újraindítja a virtuálisgép-készletet (VMSS).</span><span class="sxs-lookup"><span data-stu-id="fdf63-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="fdf63-107">Ez a parancsmag azt is megteheti, hogy a *InstanceId* paraméterrel az adott virtuális gép újraindítása a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="fdf63-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="fdf63-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fdf63-108">EXAMPLES</span></span>

### <span data-ttu-id="fdf63-109">Példa 1: a VMSS újraindítása</span><span class="sxs-lookup"><span data-stu-id="fdf63-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="fdf63-110">Ez a parancs elindítja a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf63-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="fdf63-111">2. példa: egy adott virtuális gép újraindítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="fdf63-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="fdf63-112">Ez a parancs egy olyan virtuális gépet indít elő, amely az 1-es azonosítójú példány azonosítóját tartalmazza a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf63-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="fdf63-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fdf63-113">PARAMETERS</span></span>

### <span data-ttu-id="fdf63-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdf63-114">-AsJob</span></span>
<span data-ttu-id="fdf63-115">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="fdf63-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fdf63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf63-116">-DefaultProfile</span></span>
<span data-ttu-id="fdf63-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdf63-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdf63-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="fdf63-118">-InstanceId</span></span>
<span data-ttu-id="fdf63-119">Karakterláncként adja meg az újraindítani kívánt példányok AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="fdf63-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="fdf63-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf63-120">-ResourceGroupName</span></span>
<span data-ttu-id="fdf63-121">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdf63-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="fdf63-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fdf63-122">-VMScaleSetName</span></span>
<span data-ttu-id="fdf63-123">Faj: annak a VMSS a neve, amelyre a parancsmag újraindult.</span><span class="sxs-lookup"><span data-stu-id="fdf63-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="fdf63-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fdf63-124">-Confirm</span></span>
<span data-ttu-id="fdf63-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fdf63-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdf63-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdf63-126">-WhatIf</span></span>
<span data-ttu-id="fdf63-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fdf63-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdf63-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fdf63-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdf63-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf63-129">CommonParameters</span></span>
<span data-ttu-id="fdf63-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fdf63-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf63-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdf63-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf63-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdf63-132">INPUTS</span></span>

### <span data-ttu-id="fdf63-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="fdf63-133">None</span></span>
<span data-ttu-id="fdf63-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fdf63-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fdf63-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdf63-135">OUTPUTS</span></span>

###  
<span data-ttu-id="fdf63-136">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fdf63-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="fdf63-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fdf63-137">NOTES</span></span>

## <span data-ttu-id="fdf63-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdf63-138">RELATED LINKS</span></span>

[<span data-ttu-id="fdf63-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fdf63-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="fdf63-140">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fdf63-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="fdf63-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fdf63-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="fdf63-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fdf63-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="fdf63-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fdf63-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="fdf63-144">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fdf63-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="fdf63-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fdf63-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


