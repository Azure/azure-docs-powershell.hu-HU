---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 84e24bdcd69a3100e3030e6d1947240494aea8e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671215"
---
# <span data-ttu-id="30247-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="30247-101">Start-AzVM</span></span>

## <span data-ttu-id="30247-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30247-102">SYNOPSIS</span></span>
<span data-ttu-id="30247-103">Azure virtuális gépet indít el.</span><span class="sxs-lookup"><span data-stu-id="30247-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="30247-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30247-104">SYNTAX</span></span>

### <span data-ttu-id="30247-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30247-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30247-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="30247-106">IdParameterSetName</span></span>
```
Start-AzVM [[-Name] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30247-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="30247-107">DESCRIPTION</span></span>
<span data-ttu-id="30247-108">A **Start-AzVM** parancsmag egy Azure virtuális gépet indít el.</span><span class="sxs-lookup"><span data-stu-id="30247-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="30247-109">Példák</span><span class="sxs-lookup"><span data-stu-id="30247-109">EXAMPLES</span></span>

### <span data-ttu-id="30247-110">Példa 1: virtuális gép indítása</span><span class="sxs-lookup"><span data-stu-id="30247-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="30247-111">Ez a parancs elindítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="30247-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="30247-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30247-112">PARAMETERS</span></span>

### <span data-ttu-id="30247-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30247-113">-AsJob</span></span>
<span data-ttu-id="30247-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="30247-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="30247-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30247-115">-DefaultProfile</span></span>
<span data-ttu-id="30247-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30247-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30247-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="30247-117">-Id</span></span>
<span data-ttu-id="30247-118">A virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="30247-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="30247-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="30247-119">-Name</span></span>
<span data-ttu-id="30247-120">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="30247-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30247-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30247-121">-ResourceGroupName</span></span>
<span data-ttu-id="30247-122">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="30247-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="30247-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="30247-123">-Confirm</span></span>
<span data-ttu-id="30247-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="30247-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30247-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30247-125">-WhatIf</span></span>
<span data-ttu-id="30247-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="30247-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30247-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30247-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30247-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30247-128">CommonParameters</span></span>
<span data-ttu-id="30247-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30247-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30247-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30247-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30247-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30247-131">INPUTS</span></span>

### <span data-ttu-id="30247-132">System. String</span><span class="sxs-lookup"><span data-stu-id="30247-132">System.String</span></span>

## <span data-ttu-id="30247-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30247-133">OUTPUTS</span></span>

### <span data-ttu-id="30247-134">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="30247-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="30247-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30247-135">NOTES</span></span>

## <span data-ttu-id="30247-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30247-136">RELATED LINKS</span></span>

[<span data-ttu-id="30247-137">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="30247-137">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="30247-138">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="30247-138">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="30247-139">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="30247-139">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="30247-140">Újraindítás – AzVM</span><span class="sxs-lookup"><span data-stu-id="30247-140">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="30247-141">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="30247-141">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="30247-142">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="30247-142">Update-AzVM</span></span>](./Update-AzVM.md)


