---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 4cdf61c8a5afca78f1701314476d9eacb862cdfb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844402"
---
# <span data-ttu-id="56443-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="56443-101">Remove-AzVM</span></span>

## <span data-ttu-id="56443-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56443-102">SYNOPSIS</span></span>
<span data-ttu-id="56443-103">Eltávolítja a virtuális gépet az Azureról.</span><span class="sxs-lookup"><span data-stu-id="56443-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="56443-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56443-104">SYNTAX</span></span>

### <span data-ttu-id="56443-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="56443-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56443-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="56443-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56443-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="56443-107">DESCRIPTION</span></span>
<span data-ttu-id="56443-108">A **Remove-AzVM** parancsmag eltávolítja a virtuális gépet az azureról.</span><span class="sxs-lookup"><span data-stu-id="56443-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="56443-109">Példák</span><span class="sxs-lookup"><span data-stu-id="56443-109">EXAMPLES</span></span>

### <span data-ttu-id="56443-110">Példa 1: virtuális gép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="56443-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="56443-111">Ez a parancs eltávolítja a VirtualMachine07 nevű virtuális gépet az erőforrás csoport ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="56443-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="56443-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56443-112">PARAMETERS</span></span>

### <span data-ttu-id="56443-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56443-113">-AsJob</span></span>
<span data-ttu-id="56443-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="56443-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="56443-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56443-115">-DefaultProfile</span></span>
<span data-ttu-id="56443-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56443-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56443-117">-Force</span><span class="sxs-lookup"><span data-stu-id="56443-117">-Force</span></span>
<span data-ttu-id="56443-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="56443-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="56443-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="56443-119">-Id</span></span>
<span data-ttu-id="56443-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="56443-120">The resource group name.</span></span>

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

### <span data-ttu-id="56443-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="56443-121">-Name</span></span>
<span data-ttu-id="56443-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="56443-122">The resource name.</span></span>

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

### <span data-ttu-id="56443-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56443-123">-ResourceGroupName</span></span>
<span data-ttu-id="56443-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="56443-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="56443-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="56443-125">-Confirm</span></span>
<span data-ttu-id="56443-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="56443-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56443-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56443-127">-WhatIf</span></span>
<span data-ttu-id="56443-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="56443-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="56443-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="56443-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56443-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56443-130">CommonParameters</span></span>
<span data-ttu-id="56443-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56443-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56443-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56443-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56443-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56443-133">INPUTS</span></span>

### <span data-ttu-id="56443-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="56443-134">None</span></span>
<span data-ttu-id="56443-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="56443-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56443-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56443-136">OUTPUTS</span></span>

### <span data-ttu-id="56443-137">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="56443-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="56443-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56443-138">NOTES</span></span>

## <span data-ttu-id="56443-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56443-139">RELATED LINKS</span></span>

[<span data-ttu-id="56443-140">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="56443-140">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="56443-141">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="56443-141">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="56443-142">Újraindítás – AzVM</span><span class="sxs-lookup"><span data-stu-id="56443-142">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="56443-143">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="56443-143">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="56443-144">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="56443-144">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="56443-145">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="56443-145">Update-AzVM</span></span>](./Update-AzVM.md)


