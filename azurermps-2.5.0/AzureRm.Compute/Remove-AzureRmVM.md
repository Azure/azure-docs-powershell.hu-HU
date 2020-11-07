---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvm
schema: 2.0.0
ms.openlocfilehash: 5f816be5d3c024e43074d6a75c5ba79df4b2fdb3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848886"
---
# <span data-ttu-id="cab17-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cab17-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="cab17-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cab17-102">SYNOPSIS</span></span>
<span data-ttu-id="cab17-103">Eltávolítja a virtuális gépet az Azureról.</span><span class="sxs-lookup"><span data-stu-id="cab17-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cab17-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cab17-104">SYNTAX</span></span>

### <span data-ttu-id="cab17-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cab17-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cab17-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="cab17-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cab17-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cab17-107">DESCRIPTION</span></span>
<span data-ttu-id="cab17-108">A **Remove-AzureRmVM** parancsmag eltávolítja a virtuális gépet az azureról.</span><span class="sxs-lookup"><span data-stu-id="cab17-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="cab17-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cab17-109">EXAMPLES</span></span>

### <span data-ttu-id="cab17-110">Példa 1: virtuális gép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cab17-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="cab17-111">Ez a parancs eltávolítja a VirtualMachine07 nevű virtuális gépet az erőforrás csoport ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cab17-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="cab17-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cab17-112">PARAMETERS</span></span>

### <span data-ttu-id="cab17-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cab17-113">-AsJob</span></span>
<span data-ttu-id="cab17-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="cab17-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cab17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab17-115">-DefaultProfile</span></span>
<span data-ttu-id="cab17-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cab17-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cab17-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cab17-117">-Force</span></span>
<span data-ttu-id="cab17-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="cab17-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab17-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="cab17-119">-Id</span></span>
<span data-ttu-id="cab17-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="cab17-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab17-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cab17-121">-Name</span></span>
<span data-ttu-id="cab17-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cab17-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab17-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cab17-123">-ResourceGroupName</span></span>
<span data-ttu-id="cab17-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cab17-124">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab17-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cab17-125">-Confirm</span></span>
<span data-ttu-id="cab17-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cab17-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab17-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cab17-127">-WhatIf</span></span>
<span data-ttu-id="cab17-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cab17-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="cab17-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cab17-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab17-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab17-130">CommonParameters</span></span>
<span data-ttu-id="cab17-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cab17-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab17-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab17-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab17-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cab17-133">INPUTS</span></span>

### <span data-ttu-id="cab17-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="cab17-134">None</span></span>
<span data-ttu-id="cab17-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cab17-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cab17-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cab17-136">OUTPUTS</span></span>

### <span data-ttu-id="cab17-137">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="cab17-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="cab17-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cab17-138">NOTES</span></span>

## <span data-ttu-id="cab17-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cab17-139">RELATED LINKS</span></span>

[<span data-ttu-id="cab17-140">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cab17-140">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="cab17-141">Új – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cab17-141">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="cab17-142">Újraindítás – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cab17-142">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="cab17-143">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cab17-143">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="cab17-144">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cab17-144">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="cab17-145">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cab17-145">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


