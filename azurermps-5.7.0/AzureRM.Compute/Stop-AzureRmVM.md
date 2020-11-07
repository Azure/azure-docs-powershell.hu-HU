---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvm
schema: 2.0.0
ms.openlocfilehash: 6cf37c453d47278958ccd84eaf817e6dc118b16b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672654"
---
# <span data-ttu-id="993e1-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993e1-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="993e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="993e1-102">SYNOPSIS</span></span>
<span data-ttu-id="993e1-103">Azure virtuális gép leállítása</span><span class="sxs-lookup"><span data-stu-id="993e1-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="993e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="993e1-104">SYNTAX</span></span>

### <span data-ttu-id="993e1-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="993e1-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="993e1-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="993e1-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="993e1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="993e1-107">DESCRIPTION</span></span>
<span data-ttu-id="993e1-108">A **stop-AzureRmVM** parancsmag leállítja az Azure Virtual machinet.</span><span class="sxs-lookup"><span data-stu-id="993e1-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="993e1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="993e1-109">EXAMPLES</span></span>

### <span data-ttu-id="993e1-110">Példa 1: virtuális gép leállítása</span><span class="sxs-lookup"><span data-stu-id="993e1-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="993e1-111">Ez a parancs leállítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="993e1-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="993e1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="993e1-112">PARAMETERS</span></span>

### <span data-ttu-id="993e1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="993e1-113">-AsJob</span></span>
<span data-ttu-id="993e1-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="993e1-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="993e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="993e1-115">-DefaultProfile</span></span>
<span data-ttu-id="993e1-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="993e1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="993e1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="993e1-117">-Force</span></span>
<span data-ttu-id="993e1-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="993e1-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="993e1-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="993e1-119">-Id</span></span>
<span data-ttu-id="993e1-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="993e1-120">The resource group name.</span></span>

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

### <span data-ttu-id="993e1-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="993e1-121">-Name</span></span>
<span data-ttu-id="993e1-122">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="993e1-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="993e1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="993e1-123">-ResourceGroupName</span></span>
<span data-ttu-id="993e1-124">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="993e1-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="993e1-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="993e1-125">-StayProvisioned</span></span>
<span data-ttu-id="993e1-126">A parancsmag leállítja az összes virtuális gépet a VMSS, de nem osztja fel őket.</span><span class="sxs-lookup"><span data-stu-id="993e1-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="993e1-127">A rendszer a leállított virtuális gépek számláját terheli.</span><span class="sxs-lookup"><span data-stu-id="993e1-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="993e1-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="993e1-128">-Confirm</span></span>
<span data-ttu-id="993e1-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="993e1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="993e1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="993e1-130">-WhatIf</span></span>
<span data-ttu-id="993e1-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="993e1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="993e1-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="993e1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="993e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="993e1-133">CommonParameters</span></span>
<span data-ttu-id="993e1-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="993e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="993e1-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="993e1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="993e1-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="993e1-136">INPUTS</span></span>

### <span data-ttu-id="993e1-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="993e1-137">None</span></span>
<span data-ttu-id="993e1-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="993e1-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="993e1-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="993e1-139">OUTPUTS</span></span>

### <span data-ttu-id="993e1-140">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="993e1-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="993e1-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="993e1-141">NOTES</span></span>

## <span data-ttu-id="993e1-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="993e1-142">RELATED LINKS</span></span>

[<span data-ttu-id="993e1-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993e1-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="993e1-144">Új – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993e1-144">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="993e1-145">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993e1-145">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="993e1-146">Újraindítás – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993e1-146">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="993e1-147">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993e1-147">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="993e1-148">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993e1-148">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


