---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 116cffabc942572db48d6f86b469a954bccbc1c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188100"
---
# <span data-ttu-id="e9e3f-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e9e3f-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="e9e3f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e3f-103">Azure VirtualHub-erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="e9e3f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9e3f-104">SYNTAX</span></span>

### <span data-ttu-id="e9e3f-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9e3f-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e3f-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e9e3f-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e3f-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e9e3f-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9e3f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9e3f-108">DESCRIPTION</span></span>
<span data-ttu-id="e9e3f-109">Azure VirtualHub-erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="e9e3f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e9e3f-110">EXAMPLES</span></span>

### <span data-ttu-id="e9e3f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e9e3f-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="e9e3f-112">A fenti létrehoz egy erőforráscsoport "testRG", egy virtuális WAN és egy virtuális hub a West US-ben az Azure-beli erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e9e3f-113">A virtuális hub a "10.0.1.0/24" címterületet fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="e9e3f-114">Ezt követően törli a virtuális hubot a ResourceGroupName és a ResourceName segítségével.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="e9e3f-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="e9e3f-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="e9e3f-116">A fenti létrehoz egy erőforráscsoport "testRG", egy virtuális WAN és egy virtuális hub a West US-ben az Azure-beli erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e9e3f-117">A virtuális hub a "10.0.1.0/24" címterületet fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="e9e3f-118">Ezután a virtuális hubot egy bemeneti objektummal törli.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="e9e3f-119">A beviteli objektum PSVirtualHub típusú.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="e9e3f-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="e9e3f-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="e9e3f-121">A fenti létrehoz egy erőforráscsoport "testRG", egy virtuális WAN és egy virtuális hub a West US-ben az Azure-beli erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e9e3f-122">A virtuális hub a "10.0.1.0/24" címterületet fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="e9e3f-123">Ezt követően törli a virtuális hubot a Get-AzVirtualHub kimenete segítségével PowerShell-csövekkel.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="e9e3f-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9e3f-124">PARAMETERS</span></span>

### <span data-ttu-id="e9e3f-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9e3f-125">-AsJob</span></span>
<span data-ttu-id="e9e3f-126">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e9e3f-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9e3f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e3f-127">-DefaultProfile</span></span>
<span data-ttu-id="e9e3f-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9e3f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e9e3f-129">-Force</span></span>
<span data-ttu-id="e9e3f-130">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e9e3f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9e3f-131">-InputObject</span></span>
<span data-ttu-id="e9e3f-132">A módosítani kívánt virtuális hub-objektum.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-132">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="e9e3f-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e9e3f-133">-Name</span></span>
<span data-ttu-id="e9e3f-134">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-134">The resource name.</span></span>

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

### <span data-ttu-id="e9e3f-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9e3f-135">-PassThru</span></span>
<span data-ttu-id="e9e3f-136">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e9e3f-137">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e9e3f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9e3f-138">-ResourceGroupName</span></span>
<span data-ttu-id="e9e3f-139">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-139">The resource group name.</span></span>

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

### <span data-ttu-id="e9e3f-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9e3f-140">-ResourceId</span></span>
<span data-ttu-id="e9e3f-141">A módosítani kívánt virtuális hub erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-141">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="e9e3f-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e9e3f-142">-Confirm</span></span>
<span data-ttu-id="e9e3f-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9e3f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9e3f-144">-WhatIf</span></span>
<span data-ttu-id="e9e3f-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9e3f-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e9e3f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9e3f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e3f-147">CommonParameters</span></span>
<span data-ttu-id="e9e3f-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9e3f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e3f-149">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9e3f-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e3f-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9e3f-150">INPUTS</span></span>

### <span data-ttu-id="e9e3f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="e9e3f-151">System.String</span></span>

### <span data-ttu-id="e9e3f-152">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e9e3f-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e9e3f-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9e3f-153">OUTPUTS</span></span>

### <span data-ttu-id="e9e3f-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9e3f-154">System.Boolean</span></span>

## <span data-ttu-id="e9e3f-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9e3f-155">NOTES</span></span>

## <span data-ttu-id="e9e3f-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9e3f-156">RELATED LINKS</span></span>

[<span data-ttu-id="e9e3f-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e9e3f-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="e9e3f-158">Új – AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e9e3f-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="e9e3f-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e9e3f-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
