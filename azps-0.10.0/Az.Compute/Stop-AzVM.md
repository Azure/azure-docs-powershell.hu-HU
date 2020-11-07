---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: c35326449678578492b5b8a7d4a3f5b8bff5a41d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842462"
---
# <span data-ttu-id="b1a79-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="b1a79-101">Stop-AzVM</span></span>

## <span data-ttu-id="b1a79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1a79-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a79-103">Azure virtuális gép leállítása</span><span class="sxs-lookup"><span data-stu-id="b1a79-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="b1a79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1a79-104">SYNTAX</span></span>

### <span data-ttu-id="b1a79-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b1a79-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1a79-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b1a79-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1a79-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1a79-107">DESCRIPTION</span></span>
<span data-ttu-id="b1a79-108">A **stop-AzVM** parancsmag leállítja az Azure Virtual machinet.</span><span class="sxs-lookup"><span data-stu-id="b1a79-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="b1a79-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b1a79-109">EXAMPLES</span></span>

### <span data-ttu-id="b1a79-110">Példa 1: virtuális gép leállítása</span><span class="sxs-lookup"><span data-stu-id="b1a79-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b1a79-111">Ez a parancs leállítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b1a79-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="b1a79-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1a79-112">PARAMETERS</span></span>

### <span data-ttu-id="b1a79-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1a79-113">-AsJob</span></span>
<span data-ttu-id="b1a79-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="b1a79-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b1a79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a79-115">-DefaultProfile</span></span>
<span data-ttu-id="b1a79-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1a79-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1a79-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b1a79-117">-Force</span></span>
<span data-ttu-id="b1a79-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b1a79-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1a79-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="b1a79-119">-Id</span></span>
<span data-ttu-id="b1a79-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b1a79-120">The resource group name.</span></span>

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

### <span data-ttu-id="b1a79-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b1a79-121">-Name</span></span>
<span data-ttu-id="b1a79-122">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="b1a79-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="b1a79-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a79-123">-ResourceGroupName</span></span>
<span data-ttu-id="b1a79-124">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1a79-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b1a79-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="b1a79-125">-StayProvisioned</span></span>
<span data-ttu-id="b1a79-126">A parancsmag leállítja az összes virtuális gépet a VMSS, de nem osztja fel őket.</span><span class="sxs-lookup"><span data-stu-id="b1a79-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="b1a79-127">A rendszer a leállított virtuális gépek számláját terheli.</span><span class="sxs-lookup"><span data-stu-id="b1a79-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="b1a79-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b1a79-128">-Confirm</span></span>
<span data-ttu-id="b1a79-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b1a79-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1a79-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1a79-130">-WhatIf</span></span>
<span data-ttu-id="b1a79-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b1a79-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1a79-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b1a79-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1a79-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a79-133">CommonParameters</span></span>
<span data-ttu-id="b1a79-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1a79-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a79-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a79-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a79-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1a79-136">INPUTS</span></span>

### <span data-ttu-id="b1a79-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="b1a79-137">None</span></span>
<span data-ttu-id="b1a79-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b1a79-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1a79-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1a79-139">OUTPUTS</span></span>

### <span data-ttu-id="b1a79-140">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="b1a79-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="b1a79-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1a79-141">NOTES</span></span>

## <span data-ttu-id="b1a79-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1a79-142">RELATED LINKS</span></span>

[<span data-ttu-id="b1a79-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b1a79-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b1a79-144">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="b1a79-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="b1a79-145">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="b1a79-145">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="b1a79-146">Újraindítás – AzVM</span><span class="sxs-lookup"><span data-stu-id="b1a79-146">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="b1a79-147">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="b1a79-147">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="b1a79-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b1a79-148">Update-AzVM</span></span>](./Update-AzVM.md)


