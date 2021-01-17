---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385207"
---
# <span data-ttu-id="c3911-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3911-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="c3911-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3911-102">SYNOPSIS</span></span>
<span data-ttu-id="c3911-103">Eltávolít egy Azure Virtual WAN-t.</span><span class="sxs-lookup"><span data-stu-id="c3911-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="c3911-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3911-104">SYNTAX</span></span>

### <span data-ttu-id="c3911-105">ByVirtualWanName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3911-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3911-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c3911-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3911-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c3911-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3911-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3911-108">DESCRIPTION</span></span>
<span data-ttu-id="c3911-109">Eltávolít egy Azure Virtual WAN-t.</span><span class="sxs-lookup"><span data-stu-id="c3911-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="c3911-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3911-110">EXAMPLES</span></span>

### <span data-ttu-id="c3911-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c3911-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="c3911-112">Ebben a példában egy virtuális WAN-t hoz létre egy erőforráscsoportban, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="c3911-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c3911-113">A virtuális WAN törlésekor megjelenő üzenet elrejtését a -Force jelölővel használhatja.</span><span class="sxs-lookup"><span data-stu-id="c3911-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="c3911-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c3911-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="c3911-115">Ebben a példában egy virtuális WAN-t hoz létre egy erőforráscsoportban, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="c3911-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c3911-116">Ez a törlés a New-AzVirtualWan által visszaadott virtuális wan objektum használatával történik.</span><span class="sxs-lookup"><span data-stu-id="c3911-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="c3911-117">A virtuális WAN törlésekor megjelenő üzenet elrejtését a -Force jelölővel használhatja.</span><span class="sxs-lookup"><span data-stu-id="c3911-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="c3911-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="c3911-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="c3911-119">Ebben a példában egy virtuális WAN-t hoz létre egy erőforráscsoportban, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="c3911-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c3911-120">Ez a törlés a New-AzVirtualWan által visszaadott virtuális wan erőforrás-azonosító használatával történik.</span><span class="sxs-lookup"><span data-stu-id="c3911-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="c3911-121">A virtuális WAN törlésekor megjelenő üzenet elrejtését a -Force jelölővel használhatja.</span><span class="sxs-lookup"><span data-stu-id="c3911-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="c3911-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3911-122">PARAMETERS</span></span>

### <span data-ttu-id="c3911-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3911-123">-DefaultProfile</span></span>
<span data-ttu-id="c3911-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3911-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3911-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c3911-125">-Force</span></span>
<span data-ttu-id="c3911-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3911-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c3911-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3911-127">-InputObject</span></span>
<span data-ttu-id="c3911-128">A virtuális wan objektum, amit törölni kell.</span><span class="sxs-lookup"><span data-stu-id="c3911-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="c3911-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c3911-129">-Name</span></span>
<span data-ttu-id="c3911-130">A virtuális wan név.</span><span class="sxs-lookup"><span data-stu-id="c3911-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="c3911-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3911-131">-PassThru</span></span>
<span data-ttu-id="c3911-132">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="c3911-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c3911-133">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c3911-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c3911-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3911-134">-ResourceGroupName</span></span>
<span data-ttu-id="c3911-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c3911-135">The resource group name.</span></span>

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

### <span data-ttu-id="c3911-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3911-136">-ResourceId</span></span>
<span data-ttu-id="c3911-137">A virtuális hálózat Azure-erőforrásazonosítóját törölni kell.</span><span class="sxs-lookup"><span data-stu-id="c3911-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="c3911-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3911-138">-Confirm</span></span>
<span data-ttu-id="c3911-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c3911-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3911-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3911-140">-WhatIf</span></span>
<span data-ttu-id="c3911-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c3911-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3911-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3911-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3911-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3911-143">CommonParameters</span></span>
<span data-ttu-id="c3911-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3911-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3911-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3911-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3911-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3911-146">INPUTS</span></span>

### <span data-ttu-id="c3911-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3911-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="c3911-148">System.String</span><span class="sxs-lookup"><span data-stu-id="c3911-148">System.String</span></span>

## <span data-ttu-id="c3911-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3911-149">OUTPUTS</span></span>

### <span data-ttu-id="c3911-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c3911-150">System.Boolean</span></span>

## <span data-ttu-id="c3911-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3911-151">NOTES</span></span>

## <span data-ttu-id="c3911-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3911-152">RELATED LINKS</span></span>

[<span data-ttu-id="c3911-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3911-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="c3911-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3911-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="c3911-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3911-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
