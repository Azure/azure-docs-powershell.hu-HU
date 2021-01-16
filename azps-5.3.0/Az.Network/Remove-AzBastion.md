---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385291"
---
# <span data-ttu-id="d41fa-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="d41fa-101">Remove-AzBastion</span></span>

## <span data-ttu-id="d41fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d41fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d41fa-103">Eltávolít egy bastion erőforrást.</span><span class="sxs-lookup"><span data-stu-id="d41fa-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="d41fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d41fa-104">SYNTAX</span></span>

### <span data-ttu-id="d41fa-105">ByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d41fa-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d41fa-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d41fa-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d41fa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d41fa-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d41fa-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d41fa-108">DESCRIPTION</span></span>
<span data-ttu-id="d41fa-109">Eltávolít egy bastion erőforrást. Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span><span class="sxs-lookup"><span data-stu-id="d41fa-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="d41fa-110">Example2 deletes the bastion using its object with pipeline.</span><span class="sxs-lookup"><span data-stu-id="d41fa-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="d41fa-111">Example3 deletes the bastion using its object.</span><span class="sxs-lookup"><span data-stu-id="d41fa-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="d41fa-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d41fa-112">EXAMPLES</span></span>

### <span data-ttu-id="d41fa-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="d41fa-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="d41fa-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="d41fa-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="d41fa-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="d41fa-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="d41fa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d41fa-116">PARAMETERS</span></span>

### <span data-ttu-id="d41fa-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d41fa-117">-Confirm</span></span>
<span data-ttu-id="d41fa-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d41fa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d41fa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d41fa-119">-DefaultProfile</span></span>
<span data-ttu-id="d41fa-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d41fa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d41fa-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d41fa-121">-Force</span></span>
<span data-ttu-id="d41fa-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d41fa-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d41fa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d41fa-123">-InputObject</span></span>
<span data-ttu-id="d41fa-124">The Bastion object to bedeleted.</span><span class="sxs-lookup"><span data-stu-id="d41fa-124">The Bastion object to be deleted.</span></span>

```yaml
Type: PSBastion
Parameter Sets: ByInputObject
Aliases: Bastion, BastionObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d41fa-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d41fa-125">-Name</span></span>
<span data-ttu-id="d41fa-126">A törölni szükséges erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d41fa-126">The bastion resource name to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d41fa-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d41fa-127">-PassThru</span></span>
<span data-ttu-id="d41fa-128">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtanunk.</span><span class="sxs-lookup"><span data-stu-id="d41fa-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="d41fa-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d41fa-129">-ResourceGroupName</span></span>
<span data-ttu-id="d41fa-130">Az erőforráscsoport neve, ahol a bástya létezik.</span><span class="sxs-lookup"><span data-stu-id="d41fa-130">The resource group name where bastion exists.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d41fa-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d41fa-131">-ResourceId</span></span>
<span data-ttu-id="d41fa-132">A bazsalika azure-erőforrásazonosítója, amely törlődik.</span><span class="sxs-lookup"><span data-stu-id="d41fa-132">The Azure resource ID for the Bastion to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: BastionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d41fa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d41fa-133">-WhatIf</span></span>
<span data-ttu-id="d41fa-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d41fa-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d41fa-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d41fa-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d41fa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d41fa-136">CommonParameters</span></span>
<span data-ttu-id="d41fa-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d41fa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d41fa-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d41fa-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d41fa-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d41fa-139">INPUTS</span></span>

### <span data-ttu-id="d41fa-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="d41fa-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="d41fa-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d41fa-141">System.String</span></span>

## <span data-ttu-id="d41fa-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d41fa-142">OUTPUTS</span></span>

### <span data-ttu-id="d41fa-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d41fa-143">System.Boolean</span></span>

## <span data-ttu-id="d41fa-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d41fa-144">NOTES</span></span>

## <span data-ttu-id="d41fa-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d41fa-145">RELATED LINKS</span></span>
[<span data-ttu-id="d41fa-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="d41fa-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="d41fa-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="d41fa-147">New-AzBastion</span></span>](./New-AzBastion.md)