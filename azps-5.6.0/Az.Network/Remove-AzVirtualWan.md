---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: ae05b4afd18bb1cdb55c8c1b748068f1f6c5191f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922754"
---
# <span data-ttu-id="0a912-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0a912-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="0a912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a912-102">SYNOPSIS</span></span>
<span data-ttu-id="0a912-103">Eltávolít egy Azure Virtual WAN-t.</span><span class="sxs-lookup"><span data-stu-id="0a912-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="0a912-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a912-104">SYNTAX</span></span>

### <span data-ttu-id="0a912-105">ByVirtualWanName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a912-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a912-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="0a912-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a912-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="0a912-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a912-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a912-108">DESCRIPTION</span></span>
<span data-ttu-id="0a912-109">Eltávolít egy Azure Virtual WAN-t.</span><span class="sxs-lookup"><span data-stu-id="0a912-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="0a912-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a912-110">EXAMPLES</span></span>

### <span data-ttu-id="0a912-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="0a912-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="0a912-112">Ebben a példában egy virtuális WAN-t hoz létre egy erőforráscsoportban, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="0a912-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="0a912-113">A virtuális WAN törlésekor megjelenő üzenet elrejtését a -Force jelölővel használhatja.</span><span class="sxs-lookup"><span data-stu-id="0a912-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="0a912-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="0a912-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="0a912-115">Ebben a példában egy virtuális WAN-t hoz létre egy erőforráscsoportban, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="0a912-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="0a912-116">Ez a törlés a New-AzVirtualWan által visszaadott virtuális wan objektum használatával történik.</span><span class="sxs-lookup"><span data-stu-id="0a912-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="0a912-117">A virtuális WAN törlésekor megjelenő üzenet elrejtését a -Force jelölővel használhatja.</span><span class="sxs-lookup"><span data-stu-id="0a912-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="0a912-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="0a912-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="0a912-119">Ebben a példában egy virtuális WAN-t hoz létre egy erőforráscsoportban, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="0a912-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="0a912-120">Ez a törlés a New-AzVirtualWan által visszaadott virtuális wan erőforrás-azonosító használatával történik.</span><span class="sxs-lookup"><span data-stu-id="0a912-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="0a912-121">A virtuális WAN törlésekor megjelenő üzenet elrejtését a -Force jelölővel használhatja.</span><span class="sxs-lookup"><span data-stu-id="0a912-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="0a912-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a912-122">PARAMETERS</span></span>

### <span data-ttu-id="0a912-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a912-123">-DefaultProfile</span></span>
<span data-ttu-id="0a912-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a912-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a912-125">-Force</span><span class="sxs-lookup"><span data-stu-id="0a912-125">-Force</span></span>
<span data-ttu-id="0a912-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0a912-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0a912-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a912-127">-InputObject</span></span>
<span data-ttu-id="0a912-128">A virtuális wan objektum, amit törölni kell.</span><span class="sxs-lookup"><span data-stu-id="0a912-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="0a912-129">-Name</span><span class="sxs-lookup"><span data-stu-id="0a912-129">-Name</span></span>
<span data-ttu-id="0a912-130">A virtuális wan név.</span><span class="sxs-lookup"><span data-stu-id="0a912-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="0a912-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a912-131">-PassThru</span></span>
<span data-ttu-id="0a912-132">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="0a912-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0a912-133">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0a912-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0a912-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a912-134">-ResourceGroupName</span></span>
<span data-ttu-id="0a912-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0a912-135">The resource group name.</span></span>

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

### <span data-ttu-id="0a912-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a912-136">-ResourceId</span></span>
<span data-ttu-id="0a912-137">A virtuális hálózat Azure-erőforrásazonosítóját törölni kell.</span><span class="sxs-lookup"><span data-stu-id="0a912-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="0a912-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a912-138">-Confirm</span></span>
<span data-ttu-id="0a912-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0a912-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a912-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a912-140">-WhatIf</span></span>
<span data-ttu-id="0a912-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0a912-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a912-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a912-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a912-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a912-143">CommonParameters</span></span>
<span data-ttu-id="0a912-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a912-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a912-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a912-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a912-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a912-146">INPUTS</span></span>

### <span data-ttu-id="0a912-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0a912-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="0a912-148">System.String</span><span class="sxs-lookup"><span data-stu-id="0a912-148">System.String</span></span>

## <span data-ttu-id="0a912-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a912-149">OUTPUTS</span></span>

### <span data-ttu-id="0a912-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0a912-150">System.Boolean</span></span>

## <span data-ttu-id="0a912-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a912-151">NOTES</span></span>

## <span data-ttu-id="0a912-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a912-152">RELATED LINKS</span></span>

[<span data-ttu-id="0a912-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0a912-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="0a912-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0a912-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="0a912-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0a912-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
