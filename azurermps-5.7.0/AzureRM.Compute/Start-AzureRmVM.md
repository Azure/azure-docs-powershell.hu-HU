---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 7b9e6aa5a9879e0f7abb281810d80a6900198ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672745"
---
# <span data-ttu-id="2ad30-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2ad30-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="2ad30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ad30-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad30-103">Azure virtuális gépet indít el.</span><span class="sxs-lookup"><span data-stu-id="2ad30-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ad30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ad30-104">SYNTAX</span></span>

### <span data-ttu-id="2ad30-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ad30-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ad30-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2ad30-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ad30-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ad30-107">DESCRIPTION</span></span>
<span data-ttu-id="2ad30-108">A **Start-AzureRmVM** parancsmag egy Azure virtuális gépet indít el.</span><span class="sxs-lookup"><span data-stu-id="2ad30-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="2ad30-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2ad30-109">EXAMPLES</span></span>

### <span data-ttu-id="2ad30-110">Példa 1: virtuális gép indítása</span><span class="sxs-lookup"><span data-stu-id="2ad30-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="2ad30-111">Ez a parancs elindítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2ad30-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="2ad30-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ad30-112">PARAMETERS</span></span>

### <span data-ttu-id="2ad30-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ad30-113">-AsJob</span></span>
<span data-ttu-id="2ad30-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="2ad30-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2ad30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad30-115">-DefaultProfile</span></span>
<span data-ttu-id="2ad30-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ad30-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ad30-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="2ad30-117">-Id</span></span>
<span data-ttu-id="2ad30-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ad30-118">The resource group name.</span></span>

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

### <span data-ttu-id="2ad30-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ad30-119">-Name</span></span>
<span data-ttu-id="2ad30-120">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="2ad30-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="2ad30-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad30-121">-ResourceGroupName</span></span>
<span data-ttu-id="2ad30-122">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ad30-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2ad30-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2ad30-123">-Confirm</span></span>
<span data-ttu-id="2ad30-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ad30-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ad30-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ad30-125">-WhatIf</span></span>
<span data-ttu-id="2ad30-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2ad30-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ad30-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ad30-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ad30-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad30-128">CommonParameters</span></span>
<span data-ttu-id="2ad30-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ad30-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad30-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ad30-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad30-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ad30-131">INPUTS</span></span>

### <span data-ttu-id="2ad30-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="2ad30-132">None</span></span>
<span data-ttu-id="2ad30-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2ad30-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2ad30-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ad30-134">OUTPUTS</span></span>

### <span data-ttu-id="2ad30-135">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="2ad30-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="2ad30-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ad30-136">NOTES</span></span>

## <span data-ttu-id="2ad30-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ad30-137">RELATED LINKS</span></span>

[<span data-ttu-id="2ad30-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2ad30-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="2ad30-139">Új – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2ad30-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="2ad30-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2ad30-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="2ad30-141">Újraindítás – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2ad30-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="2ad30-142">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2ad30-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="2ad30-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2ad30-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


