---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186775"
---
# <span data-ttu-id="6370d-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="6370d-101">Start-AzVM</span></span>

## <span data-ttu-id="6370d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6370d-102">SYNOPSIS</span></span>
<span data-ttu-id="6370d-103">Azure virtuális gépet indít el.</span><span class="sxs-lookup"><span data-stu-id="6370d-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="6370d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6370d-104">SYNTAX</span></span>

### <span data-ttu-id="6370d-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6370d-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6370d-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6370d-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6370d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6370d-107">DESCRIPTION</span></span>
<span data-ttu-id="6370d-108">A **Start-AzVM** parancsmag egy Azure virtuális gépet indít el.</span><span class="sxs-lookup"><span data-stu-id="6370d-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="6370d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6370d-109">EXAMPLES</span></span>

### <span data-ttu-id="6370d-110">Példa 1: virtuális gép indítása</span><span class="sxs-lookup"><span data-stu-id="6370d-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="6370d-111">Ez a parancs elindítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6370d-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="6370d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6370d-112">PARAMETERS</span></span>

### <span data-ttu-id="6370d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6370d-113">-AsJob</span></span>
<span data-ttu-id="6370d-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="6370d-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6370d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6370d-115">-DefaultProfile</span></span>
<span data-ttu-id="6370d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6370d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6370d-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="6370d-117">-Id</span></span>
<span data-ttu-id="6370d-118">A virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6370d-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="6370d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6370d-119">-Name</span></span>
<span data-ttu-id="6370d-120">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="6370d-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="6370d-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="6370d-121">-NoWait</span></span>
<span data-ttu-id="6370d-122">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="6370d-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="6370d-123">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="6370d-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="6370d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6370d-124">-ResourceGroupName</span></span>
<span data-ttu-id="6370d-125">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6370d-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6370d-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6370d-126">-Confirm</span></span>
<span data-ttu-id="6370d-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6370d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6370d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6370d-128">-WhatIf</span></span>
<span data-ttu-id="6370d-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6370d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6370d-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6370d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6370d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6370d-131">CommonParameters</span></span>
<span data-ttu-id="6370d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6370d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6370d-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6370d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6370d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6370d-134">INPUTS</span></span>

### <span data-ttu-id="6370d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6370d-135">System.String</span></span>

## <span data-ttu-id="6370d-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6370d-136">OUTPUTS</span></span>

### <span data-ttu-id="6370d-137">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="6370d-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="6370d-138">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6370d-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6370d-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6370d-139">NOTES</span></span>

## <span data-ttu-id="6370d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6370d-140">RELATED LINKS</span></span>

[<span data-ttu-id="6370d-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="6370d-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="6370d-142">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="6370d-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="6370d-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="6370d-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="6370d-144">Újraindítás – AzVM</span><span class="sxs-lookup"><span data-stu-id="6370d-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="6370d-145">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="6370d-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="6370d-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6370d-146">Update-AzVM</span></span>](./Update-AzVM.md)

