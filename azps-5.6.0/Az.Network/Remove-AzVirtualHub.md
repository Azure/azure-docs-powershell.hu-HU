---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 7a5724346f1b94af0dbc07df16f9cdab5f798523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006117"
---
# <span data-ttu-id="55845-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="55845-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="55845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55845-102">SYNOPSIS</span></span>
<span data-ttu-id="55845-103">Eltávolít egy Azure VirtualHub-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="55845-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="55845-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="55845-104">SYNTAX</span></span>

### <span data-ttu-id="55845-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55845-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55845-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="55845-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55845-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="55845-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55845-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="55845-108">DESCRIPTION</span></span>
<span data-ttu-id="55845-109">Eltávolít egy Azure VirtualHub-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="55845-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="55845-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="55845-110">EXAMPLES</span></span>

### <span data-ttu-id="55845-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="55845-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="55845-112">A fentiekkel létrehoz egy "testRG" erőforráscsoportot, egy virtuális WAN-t és egy virtuális központot az Azure-ban az adott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="55845-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="55845-113">A virtuális központ a "10.0.1.0/24" címterületet fogja rendelkezésre álló helyen.</span><span class="sxs-lookup"><span data-stu-id="55845-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="55845-114">Ezután törli a virtuális központot annak ResourceGroupName és ResourceName tulajdonságával.</span><span class="sxs-lookup"><span data-stu-id="55845-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="55845-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="55845-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="55845-116">A fentiekkel létrehoz egy "testRG" erőforráscsoportot, egy virtuális WAN-t és egy virtuális központot az Azure-ban az adott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="55845-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="55845-117">A virtuális központ a "10.0.1.0/24" címterületet fogja rendelkezésre álló helyen.</span><span class="sxs-lookup"><span data-stu-id="55845-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="55845-118">Ezután egy bemeneti objektum használatával törli a virtuális központot.</span><span class="sxs-lookup"><span data-stu-id="55845-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="55845-119">A bemeneti objektum PSVirtualHub típusú.</span><span class="sxs-lookup"><span data-stu-id="55845-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="55845-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="55845-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="55845-121">A fentiekkel létrehoz egy "testRG" erőforráscsoportot, egy virtuális WAN-t és egy virtuális központot az Azure-ban az adott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="55845-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="55845-122">A virtuális központ a "10.0.1.0/24" címterületet fogja rendelkezésre álló helyen.</span><span class="sxs-lookup"><span data-stu-id="55845-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="55845-123">Ezután powershell-piping használatával törli a virtuális központot a Get-AzVirtualHub kimenetét használva.</span><span class="sxs-lookup"><span data-stu-id="55845-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="55845-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55845-124">PARAMETERS</span></span>

### <span data-ttu-id="55845-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55845-125">-AsJob</span></span>
<span data-ttu-id="55845-126">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="55845-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55845-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55845-127">-DefaultProfile</span></span>
<span data-ttu-id="55845-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55845-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55845-129">-Force</span><span class="sxs-lookup"><span data-stu-id="55845-129">-Force</span></span>
<span data-ttu-id="55845-130">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="55845-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="55845-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55845-131">-InputObject</span></span>
<span data-ttu-id="55845-132">A módosítva lévő virtuális központi objektum.</span><span class="sxs-lookup"><span data-stu-id="55845-132">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55845-133">-Name</span><span class="sxs-lookup"><span data-stu-id="55845-133">-Name</span></span>
<span data-ttu-id="55845-134">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="55845-134">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55845-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55845-135">-PassThru</span></span>
<span data-ttu-id="55845-136">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="55845-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="55845-137">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="55845-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55845-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55845-138">-ResourceGroupName</span></span>
<span data-ttu-id="55845-139">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="55845-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55845-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55845-140">-ResourceId</span></span>
<span data-ttu-id="55845-141">A módosítani szükséges virtuális központ erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="55845-141">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55845-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55845-142">-Confirm</span></span>
<span data-ttu-id="55845-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="55845-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55845-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55845-144">-WhatIf</span></span>
<span data-ttu-id="55845-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="55845-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55845-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55845-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55845-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55845-147">CommonParameters</span></span>
<span data-ttu-id="55845-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55845-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55845-149">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55845-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55845-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55845-150">INPUTS</span></span>

### <span data-ttu-id="55845-151">System.String</span><span class="sxs-lookup"><span data-stu-id="55845-151">System.String</span></span>

### <span data-ttu-id="55845-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="55845-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="55845-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55845-153">OUTPUTS</span></span>

### <span data-ttu-id="55845-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="55845-154">System.Boolean</span></span>

## <span data-ttu-id="55845-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="55845-155">NOTES</span></span>

## <span data-ttu-id="55845-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55845-156">RELATED LINKS</span></span>

[<span data-ttu-id="55845-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="55845-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="55845-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="55845-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="55845-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="55845-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
