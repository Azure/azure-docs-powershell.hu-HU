---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: b0e01f462bfb7576e942138cb42b3171fb6660b3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844322"
---
# <span data-ttu-id="6fd83-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6fd83-101">Restart-AzVmss</span></span>

## <span data-ttu-id="6fd83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6fd83-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd83-103">A VMSS vagy egy virtuális gép újraindítása a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="6fd83-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="6fd83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6fd83-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fd83-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6fd83-105">DESCRIPTION</span></span>
<span data-ttu-id="6fd83-106">Az **Újraindítás-AzVmss** parancsmag újraindítja a virtuálisgép-készletet (VMSS).</span><span class="sxs-lookup"><span data-stu-id="6fd83-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="6fd83-107">Ez a parancsmag azt is megteheti, hogy a *InstanceId* paraméterrel az adott virtuális gép újraindítása a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="6fd83-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="6fd83-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6fd83-108">EXAMPLES</span></span>

### <span data-ttu-id="6fd83-109">Példa 1: a VMSS újraindítása</span><span class="sxs-lookup"><span data-stu-id="6fd83-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="6fd83-110">Ez a parancs elindítja a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS.</span><span class="sxs-lookup"><span data-stu-id="6fd83-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="6fd83-111">2. példa: egy adott virtuális gép újraindítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="6fd83-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="6fd83-112">Ez a parancs egy olyan virtuális gépet indít elő, amely az 1-es azonosítójú példány azonosítóját tartalmazza a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS.</span><span class="sxs-lookup"><span data-stu-id="6fd83-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="6fd83-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6fd83-113">PARAMETERS</span></span>

### <span data-ttu-id="6fd83-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fd83-114">-AsJob</span></span>
<span data-ttu-id="6fd83-115">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="6fd83-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6fd83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd83-116">-DefaultProfile</span></span>
<span data-ttu-id="6fd83-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6fd83-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fd83-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="6fd83-118">-InstanceId</span></span>
<span data-ttu-id="6fd83-119">Karakterláncként adja meg az újraindítani kívánt példányok AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="6fd83-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="6fd83-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd83-120">-ResourceGroupName</span></span>
<span data-ttu-id="6fd83-121">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fd83-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="6fd83-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6fd83-122">-VMScaleSetName</span></span>
<span data-ttu-id="6fd83-123">Faj: annak a VMSS a neve, amelyre a parancsmag újraindult.</span><span class="sxs-lookup"><span data-stu-id="6fd83-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="6fd83-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6fd83-124">-Confirm</span></span>
<span data-ttu-id="6fd83-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6fd83-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fd83-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd83-126">-WhatIf</span></span>
<span data-ttu-id="6fd83-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6fd83-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fd83-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6fd83-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fd83-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd83-129">CommonParameters</span></span>
<span data-ttu-id="6fd83-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6fd83-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd83-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd83-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd83-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fd83-132">INPUTS</span></span>

### <span data-ttu-id="6fd83-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="6fd83-133">None</span></span>
<span data-ttu-id="6fd83-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6fd83-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6fd83-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fd83-135">OUTPUTS</span></span>

###  
<span data-ttu-id="6fd83-136">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6fd83-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="6fd83-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6fd83-137">NOTES</span></span>

## <span data-ttu-id="6fd83-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fd83-138">RELATED LINKS</span></span>

[<span data-ttu-id="6fd83-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6fd83-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="6fd83-140">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="6fd83-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="6fd83-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6fd83-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="6fd83-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6fd83-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="6fd83-143">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6fd83-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="6fd83-144">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6fd83-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="6fd83-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6fd83-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


