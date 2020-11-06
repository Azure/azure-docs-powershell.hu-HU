---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 479aaf61169cb09d8561e9f09b05a5852c93b58d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492526"
---
# <span data-ttu-id="bb368-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb368-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="bb368-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb368-102">SYNOPSIS</span></span>
<span data-ttu-id="bb368-103">A VMSS vagy egy virtuális gép újraindítása a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="bb368-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb368-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb368-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb368-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb368-105">DESCRIPTION</span></span>
<span data-ttu-id="bb368-106">Az **Újraindítás-AzureRmVmss** parancsmag újraindítja a virtuálisgép-készletet (VMSS).</span><span class="sxs-lookup"><span data-stu-id="bb368-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="bb368-107">Ez a parancsmag azt is megteheti, hogy a *InstanceId* paraméterrel az adott virtuális gép újraindítása a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="bb368-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="bb368-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bb368-108">EXAMPLES</span></span>

### <span data-ttu-id="bb368-109">Példa 1: a VMSS újraindítása</span><span class="sxs-lookup"><span data-stu-id="bb368-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="bb368-110">Ez a parancs elindítja a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS.</span><span class="sxs-lookup"><span data-stu-id="bb368-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="bb368-111">2. példa: egy adott virtuális gép újraindítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="bb368-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="bb368-112">Ez a parancs egy olyan virtuális gépet indít elő, amely az 1-es azonosítójú példány azonosítóját tartalmazza a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS.</span><span class="sxs-lookup"><span data-stu-id="bb368-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="bb368-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb368-113">PARAMETERS</span></span>

### <span data-ttu-id="bb368-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb368-114">-DefaultProfile</span></span>
<span data-ttu-id="bb368-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb368-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb368-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="bb368-116">-InstanceId</span></span>
<span data-ttu-id="bb368-117">Karakterláncként adja meg az újraindítani kívánt példányok AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="bb368-117">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb368-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb368-118">-ResourceGroupName</span></span>
<span data-ttu-id="bb368-119">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb368-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="bb368-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bb368-120">-VMScaleSetName</span></span>
<span data-ttu-id="bb368-121">Faj: annak a VMSS a neve, amelyre a parancsmag újraindult.</span><span class="sxs-lookup"><span data-stu-id="bb368-121">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="bb368-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bb368-122">-Confirm</span></span>
<span data-ttu-id="bb368-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bb368-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb368-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb368-124">-WhatIf</span></span>
<span data-ttu-id="bb368-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bb368-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb368-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb368-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb368-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb368-127">CommonParameters</span></span>
<span data-ttu-id="bb368-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb368-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb368-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb368-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb368-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb368-130">INPUTS</span></span>

## <span data-ttu-id="bb368-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb368-131">OUTPUTS</span></span>

###  
<span data-ttu-id="bb368-132">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bb368-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="bb368-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb368-133">NOTES</span></span>

## <span data-ttu-id="bb368-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb368-134">RELATED LINKS</span></span>

[<span data-ttu-id="bb368-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb368-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="bb368-136">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb368-136">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="bb368-137">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb368-137">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="bb368-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb368-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="bb368-139">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb368-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="bb368-140">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb368-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="bb368-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bb368-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


