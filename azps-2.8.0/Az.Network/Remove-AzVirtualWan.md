---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: d1ec777d6574aa34a6b19fa7cdc94d9c349dbc48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837067"
---
# <span data-ttu-id="cbdcb-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cbdcb-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="cbdcb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cbdcb-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdcb-103">Azure virtuális WAN-kapcsolat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="cbdcb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cbdcb-104">SYNTAX</span></span>

### <span data-ttu-id="cbdcb-105">ByVirtualWanName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cbdcb-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbdcb-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="cbdcb-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbdcb-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="cbdcb-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbdcb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cbdcb-108">DESCRIPTION</span></span>
<span data-ttu-id="cbdcb-109">Azure virtuális WAN-kapcsolat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="cbdcb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cbdcb-110">EXAMPLES</span></span>

### <span data-ttu-id="cbdcb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cbdcb-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="cbdcb-112">Ez a példa létrehoz egy virtuális WAN-csoportot egy erőforráscsoporthoz, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="cbdcb-113">Ha el szeretné tiltani a virtuális WAN-kapcsolat törlésekor megjelenő üzenetet, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="cbdcb-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="cbdcb-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="cbdcb-115">Ez a példa létrehoz egy virtuális WAN-csoportot egy erőforráscsoporthoz, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="cbdcb-116">Ez a Törlés az új AzVirtualWan által visszaadott virtuális WAN-objektum használatával történik.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="cbdcb-117">Ha el szeretné tiltani a virtuális WAN-kapcsolat törlésekor megjelenő üzenetet, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="cbdcb-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="cbdcb-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="cbdcb-119">Ez a példa létrehoz egy virtuális WAN-csoportot egy erőforráscsoporthoz, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="cbdcb-120">Ez a Törlés az új AzVirtualWan által visszaadott virtuális WAN-erőforrás-azonosító használatával történik.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="cbdcb-121">Ha el szeretné tiltani a virtuális WAN-kapcsolat törlésekor megjelenő üzenetet, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="cbdcb-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cbdcb-122">PARAMETERS</span></span>

### <span data-ttu-id="cbdcb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdcb-123">-DefaultProfile</span></span>
<span data-ttu-id="cbdcb-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbdcb-125">-Force</span><span class="sxs-lookup"><span data-stu-id="cbdcb-125">-Force</span></span>
<span data-ttu-id="cbdcb-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cbdcb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbdcb-127">-InputObject</span></span>
<span data-ttu-id="cbdcb-128">A törlendő virtuális WAN-objektum.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-128">The virtual wan object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbdcb-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cbdcb-129">-Name</span></span>
<span data-ttu-id="cbdcb-130">A virtuális WAN-név.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-130">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdcb-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbdcb-131">-PassThru</span></span>
<span data-ttu-id="cbdcb-132">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cbdcb-133">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cbdcb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbdcb-134">-ResourceGroupName</span></span>
<span data-ttu-id="cbdcb-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdcb-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbdcb-136">-ResourceId</span></span>
<span data-ttu-id="cbdcb-137">A virtuális WAN által törölni kívánt Azure Resource ID azonosító.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbdcb-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cbdcb-138">-Confirm</span></span>
<span data-ttu-id="cbdcb-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbdcb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbdcb-140">-WhatIf</span></span>
<span data-ttu-id="cbdcb-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbdcb-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cbdcb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbdcb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdcb-143">CommonParameters</span></span>
<span data-ttu-id="cbdcb-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cbdcb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdcb-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbdcb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdcb-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbdcb-146">INPUTS</span></span>

### <span data-ttu-id="cbdcb-147">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cbdcb-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="cbdcb-148">System. String</span><span class="sxs-lookup"><span data-stu-id="cbdcb-148">System.String</span></span>

## <span data-ttu-id="cbdcb-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbdcb-149">OUTPUTS</span></span>

### <span data-ttu-id="cbdcb-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cbdcb-150">System.Boolean</span></span>

## <span data-ttu-id="cbdcb-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cbdcb-151">NOTES</span></span>

## <span data-ttu-id="cbdcb-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbdcb-152">RELATED LINKS</span></span>

[<span data-ttu-id="cbdcb-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cbdcb-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="cbdcb-154">Új – AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cbdcb-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="cbdcb-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cbdcb-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
