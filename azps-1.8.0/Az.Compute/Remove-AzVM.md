---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 5a7f03cbd4fdac75743fed491697ac2bb4ff6dac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836727"
---
# <span data-ttu-id="e8ccd-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="e8ccd-101">Remove-AzVM</span></span>

## <span data-ttu-id="e8ccd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ccd-103">Eltávolítja a virtuális gépet az Azureról.</span><span class="sxs-lookup"><span data-stu-id="e8ccd-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="e8ccd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8ccd-104">SYNTAX</span></span>

### <span data-ttu-id="e8ccd-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8ccd-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ccd-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e8ccd-106">IdParameterSetName</span></span>
```
Remove-AzVM [[-Name] <String>] [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8ccd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8ccd-107">DESCRIPTION</span></span>
<span data-ttu-id="e8ccd-108">A **Remove-AzVM** parancsmag eltávolítja a virtuális gépet az azureról.</span><span class="sxs-lookup"><span data-stu-id="e8ccd-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="e8ccd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e8ccd-109">EXAMPLES</span></span>

### <span data-ttu-id="e8ccd-110">Példa 1: virtuális gép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e8ccd-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="e8ccd-111">Ez a parancs eltávolítja a VirtualMachine07 nevű virtuális gépet az erőforrás csoport ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e8ccd-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="e8ccd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8ccd-112">PARAMETERS</span></span>

### <span data-ttu-id="e8ccd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8ccd-113">-AsJob</span></span>
<span data-ttu-id="e8ccd-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="e8ccd-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ccd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ccd-115">-DefaultProfile</span></span>
<span data-ttu-id="e8ccd-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8ccd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ccd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e8ccd-117">-Force</span></span>
<span data-ttu-id="e8ccd-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e8ccd-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ccd-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e8ccd-119">-Id</span></span>
<span data-ttu-id="e8ccd-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e8ccd-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ccd-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8ccd-121">-Name</span></span>
<span data-ttu-id="e8ccd-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e8ccd-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ccd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ccd-123">-ResourceGroupName</span></span>
<span data-ttu-id="e8ccd-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8ccd-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ccd-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e8ccd-125">-Confirm</span></span>
<span data-ttu-id="e8ccd-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e8ccd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ccd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ccd-127">-WhatIf</span></span>
<span data-ttu-id="e8ccd-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e8ccd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8ccd-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8ccd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ccd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ccd-130">CommonParameters</span></span>
<span data-ttu-id="e8ccd-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8ccd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ccd-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ccd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ccd-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8ccd-133">INPUTS</span></span>

### <span data-ttu-id="e8ccd-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e8ccd-134">System.String</span></span>

## <span data-ttu-id="e8ccd-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8ccd-135">OUTPUTS</span></span>

### <span data-ttu-id="e8ccd-136">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="e8ccd-136">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="e8ccd-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8ccd-137">NOTES</span></span>

## <span data-ttu-id="e8ccd-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8ccd-138">RELATED LINKS</span></span>

[<span data-ttu-id="e8ccd-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e8ccd-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e8ccd-140">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="e8ccd-140">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="e8ccd-141">Újraindítás – AzVM</span><span class="sxs-lookup"><span data-stu-id="e8ccd-141">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="e8ccd-142">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="e8ccd-142">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="e8ccd-143">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="e8ccd-143">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="e8ccd-144">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e8ccd-144">Update-AzVM</span></span>](./Update-AzVM.md)


