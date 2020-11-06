---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVM.md
ms.openlocfilehash: bbfbf2a8a0cace2580dbd929a81bfec8a120cfe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492843"
---
# <span data-ttu-id="cd24a-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd24a-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="cd24a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd24a-102">SYNOPSIS</span></span>
<span data-ttu-id="cd24a-103">Eltávolítja a virtuális gépet az Azureról.</span><span class="sxs-lookup"><span data-stu-id="cd24a-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd24a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd24a-104">SYNTAX</span></span>

### <span data-ttu-id="cd24a-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd24a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd24a-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="cd24a-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd24a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd24a-107">DESCRIPTION</span></span>
<span data-ttu-id="cd24a-108">A **Remove-AzureRmVM** parancsmag eltávolítja a virtuális gépet az azureról.</span><span class="sxs-lookup"><span data-stu-id="cd24a-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="cd24a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cd24a-109">EXAMPLES</span></span>

### <span data-ttu-id="cd24a-110">Példa 1: virtuális gép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cd24a-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="cd24a-111">Ez a parancs eltávolítja a VirtualMachine07 nevű virtuális gépet az erőforrás csoport ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cd24a-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="cd24a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd24a-112">PARAMETERS</span></span>

### <span data-ttu-id="cd24a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd24a-113">-AsJob</span></span>
<span data-ttu-id="cd24a-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="cd24a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cd24a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd24a-115">-DefaultProfile</span></span>
<span data-ttu-id="cd24a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd24a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd24a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cd24a-117">-Force</span></span>
<span data-ttu-id="cd24a-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="cd24a-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd24a-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="cd24a-119">-Id</span></span>
<span data-ttu-id="cd24a-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="cd24a-120">The resource group name.</span></span>

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

### <span data-ttu-id="cd24a-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cd24a-121">-Name</span></span>
<span data-ttu-id="cd24a-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cd24a-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd24a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd24a-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd24a-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd24a-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cd24a-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd24a-125">-Confirm</span></span>
<span data-ttu-id="cd24a-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd24a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd24a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd24a-127">-WhatIf</span></span>
<span data-ttu-id="cd24a-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cd24a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd24a-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd24a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd24a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd24a-130">CommonParameters</span></span>
<span data-ttu-id="cd24a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd24a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd24a-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd24a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd24a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd24a-133">INPUTS</span></span>

### <span data-ttu-id="cd24a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cd24a-134">System.String</span></span>

## <span data-ttu-id="cd24a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd24a-135">OUTPUTS</span></span>

### <span data-ttu-id="cd24a-136">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="cd24a-136">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="cd24a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd24a-137">NOTES</span></span>

## <span data-ttu-id="cd24a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd24a-138">RELATED LINKS</span></span>

[<span data-ttu-id="cd24a-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd24a-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="cd24a-140">Új – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd24a-140">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="cd24a-141">Újraindítás – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd24a-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="cd24a-142">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd24a-142">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="cd24a-143">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd24a-143">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="cd24a-144">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd24a-144">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


