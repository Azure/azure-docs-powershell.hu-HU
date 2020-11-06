---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
ms.openlocfilehash: f0d6ab84e457894b3c1ff7309efc6914350a03e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500080"
---
# <span data-ttu-id="cc741-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cc741-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="cc741-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc741-102">SYNOPSIS</span></span>
<span data-ttu-id="cc741-103">Azure virtuális gép leállítása</span><span class="sxs-lookup"><span data-stu-id="cc741-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc741-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc741-104">SYNTAX</span></span>

### <span data-ttu-id="cc741-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc741-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc741-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="cc741-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc741-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc741-107">DESCRIPTION</span></span>
<span data-ttu-id="cc741-108">A **stop-AzureRmVM** parancsmag leállítja az Azure Virtual machinet.</span><span class="sxs-lookup"><span data-stu-id="cc741-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="cc741-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cc741-109">EXAMPLES</span></span>

### <span data-ttu-id="cc741-110">Példa 1: virtuális gép leállítása</span><span class="sxs-lookup"><span data-stu-id="cc741-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="cc741-111">Ez a parancs leállítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cc741-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="cc741-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc741-112">PARAMETERS</span></span>

### <span data-ttu-id="cc741-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc741-113">-DefaultProfile</span></span>
<span data-ttu-id="cc741-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc741-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc741-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cc741-115">-Force</span></span>
<span data-ttu-id="cc741-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="cc741-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc741-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="cc741-117">-Id</span></span>
<span data-ttu-id="cc741-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="cc741-118">The resource group name.</span></span>

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

### <span data-ttu-id="cc741-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc741-119">-Name</span></span>
<span data-ttu-id="cc741-120">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="cc741-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="cc741-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc741-121">-ResourceGroupName</span></span>
<span data-ttu-id="cc741-122">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc741-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cc741-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="cc741-123">-StayProvisioned</span></span>
<span data-ttu-id="cc741-124">A parancsmag leállítja az összes virtuális gépet a VMSS, de nem osztja fel őket.</span><span class="sxs-lookup"><span data-stu-id="cc741-124">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="cc741-125">A rendszer a leállított virtuális gépek számláját terheli.</span><span class="sxs-lookup"><span data-stu-id="cc741-125">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="cc741-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc741-126">-Confirm</span></span>
<span data-ttu-id="cc741-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc741-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc741-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc741-128">-WhatIf</span></span>
<span data-ttu-id="cc741-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc741-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc741-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc741-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc741-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc741-131">CommonParameters</span></span>
<span data-ttu-id="cc741-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc741-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc741-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc741-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc741-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc741-134">INPUTS</span></span>

## <span data-ttu-id="cc741-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc741-135">OUTPUTS</span></span>

## <span data-ttu-id="cc741-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc741-136">NOTES</span></span>

## <span data-ttu-id="cc741-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc741-137">RELATED LINKS</span></span>

[<span data-ttu-id="cc741-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cc741-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="cc741-139">Új – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cc741-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="cc741-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cc741-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="cc741-141">Újraindítás – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cc741-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="cc741-142">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cc741-142">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="cc741-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cc741-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


