---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202584"
---
# <span data-ttu-id="301e6-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="301e6-101">Remove-AzBastion</span></span>

## <span data-ttu-id="301e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="301e6-102">SYNOPSIS</span></span>
<span data-ttu-id="301e6-103">Eltávolít egy bastion erőforrást.</span><span class="sxs-lookup"><span data-stu-id="301e6-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="301e6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="301e6-104">SYNTAX</span></span>

### <span data-ttu-id="301e6-105">ByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="301e6-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="301e6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="301e6-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="301e6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="301e6-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="301e6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="301e6-108">DESCRIPTION</span></span>
<span data-ttu-id="301e6-109">Eltávolít egy bastion erőforrást. Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span><span class="sxs-lookup"><span data-stu-id="301e6-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="301e6-110">Example2 deletes the bastion using its object with pipeline.</span><span class="sxs-lookup"><span data-stu-id="301e6-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="301e6-111">Example3 deletes the bastion using its object.</span><span class="sxs-lookup"><span data-stu-id="301e6-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="301e6-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="301e6-112">EXAMPLES</span></span>

### <span data-ttu-id="301e6-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="301e6-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="301e6-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="301e6-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="301e6-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="301e6-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="301e6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="301e6-116">PARAMETERS</span></span>

### <span data-ttu-id="301e6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="301e6-117">-Confirm</span></span>
<span data-ttu-id="301e6-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="301e6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="301e6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301e6-119">-DefaultProfile</span></span>
<span data-ttu-id="301e6-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="301e6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="301e6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="301e6-121">-Force</span></span>
<span data-ttu-id="301e6-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="301e6-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="301e6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="301e6-123">-InputObject</span></span>
<span data-ttu-id="301e6-124">The Bastion object to bedeleted.</span><span class="sxs-lookup"><span data-stu-id="301e6-124">The Bastion object to be deleted.</span></span>

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

### <span data-ttu-id="301e6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="301e6-125">-Name</span></span>
<span data-ttu-id="301e6-126">A törölni szükséges erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="301e6-126">The bastion resource name to be deleted.</span></span>

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

### <span data-ttu-id="301e6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="301e6-127">-PassThru</span></span>
<span data-ttu-id="301e6-128">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtotta.</span><span class="sxs-lookup"><span data-stu-id="301e6-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="301e6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301e6-129">-ResourceGroupName</span></span>
<span data-ttu-id="301e6-130">Az erőforráscsoport neve, ahol a bástya létezik.</span><span class="sxs-lookup"><span data-stu-id="301e6-130">The resource group name where bastion exists.</span></span>

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

### <span data-ttu-id="301e6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="301e6-131">-ResourceId</span></span>
<span data-ttu-id="301e6-132">A bazsalika azure-erőforrásazonosítója, amely törlődik.</span><span class="sxs-lookup"><span data-stu-id="301e6-132">The Azure resource ID for the Bastion to be deleted.</span></span>

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

### <span data-ttu-id="301e6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="301e6-133">-WhatIf</span></span>
<span data-ttu-id="301e6-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="301e6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="301e6-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="301e6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="301e6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301e6-136">CommonParameters</span></span>
<span data-ttu-id="301e6-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="301e6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301e6-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="301e6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301e6-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="301e6-139">INPUTS</span></span>

### <span data-ttu-id="301e6-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="301e6-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="301e6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="301e6-141">System.String</span></span>

## <span data-ttu-id="301e6-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="301e6-142">OUTPUTS</span></span>

### <span data-ttu-id="301e6-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="301e6-143">System.Boolean</span></span>

## <span data-ttu-id="301e6-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="301e6-144">NOTES</span></span>

## <span data-ttu-id="301e6-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="301e6-145">RELATED LINKS</span></span>
[<span data-ttu-id="301e6-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="301e6-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="301e6-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="301e6-147">New-AzBastion</span></span>](./New-AzBastion.md)