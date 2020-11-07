---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: e343b9e16f793a760166736edcef6658bde34723
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842477"
---
# <span data-ttu-id="9f813-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="9f813-101">Start-AzVM</span></span>

## <span data-ttu-id="9f813-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f813-102">SYNOPSIS</span></span>
<span data-ttu-id="9f813-103">Azure virtuális gépet indít el.</span><span class="sxs-lookup"><span data-stu-id="9f813-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="9f813-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f813-104">SYNTAX</span></span>

### <span data-ttu-id="9f813-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f813-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f813-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9f813-106">IdParameterSetName</span></span>
```
Start-AzVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f813-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f813-107">DESCRIPTION</span></span>
<span data-ttu-id="9f813-108">A **Start-AzVM** parancsmag egy Azure virtuális gépet indít el.</span><span class="sxs-lookup"><span data-stu-id="9f813-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="9f813-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9f813-109">EXAMPLES</span></span>

### <span data-ttu-id="9f813-110">Példa 1: virtuális gép indítása</span><span class="sxs-lookup"><span data-stu-id="9f813-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="9f813-111">Ez a parancs elindítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9f813-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="9f813-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f813-112">PARAMETERS</span></span>

### <span data-ttu-id="9f813-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f813-113">-AsJob</span></span>
<span data-ttu-id="9f813-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="9f813-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9f813-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f813-115">-DefaultProfile</span></span>
<span data-ttu-id="9f813-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f813-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f813-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9f813-117">-Id</span></span>
<span data-ttu-id="9f813-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9f813-118">The resource group name.</span></span>

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

### <span data-ttu-id="9f813-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9f813-119">-Name</span></span>
<span data-ttu-id="9f813-120">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="9f813-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="9f813-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f813-121">-ResourceGroupName</span></span>
<span data-ttu-id="9f813-122">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f813-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9f813-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9f813-123">-Confirm</span></span>
<span data-ttu-id="9f813-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f813-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f813-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f813-125">-WhatIf</span></span>
<span data-ttu-id="9f813-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9f813-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f813-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f813-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f813-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f813-128">CommonParameters</span></span>
<span data-ttu-id="9f813-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f813-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f813-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f813-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f813-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f813-131">INPUTS</span></span>

### <span data-ttu-id="9f813-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="9f813-132">None</span></span>
<span data-ttu-id="9f813-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9f813-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9f813-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f813-134">OUTPUTS</span></span>

### <span data-ttu-id="9f813-135">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="9f813-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="9f813-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f813-136">NOTES</span></span>

## <span data-ttu-id="9f813-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f813-137">RELATED LINKS</span></span>

[<span data-ttu-id="9f813-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9f813-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9f813-139">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="9f813-139">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="9f813-140">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="9f813-140">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="9f813-141">Újraindítás – AzVM</span><span class="sxs-lookup"><span data-stu-id="9f813-141">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="9f813-142">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="9f813-142">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="9f813-143">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="9f813-143">Update-AzVM</span></span>](./Update-AzVM.md)


