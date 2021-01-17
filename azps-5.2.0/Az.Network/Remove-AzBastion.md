---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327456"
---
# <span data-ttu-id="c9c09-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="c9c09-101">Remove-AzBastion</span></span>

## <span data-ttu-id="c9c09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9c09-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c09-103">Eltávolít egy bastion erőforrást.</span><span class="sxs-lookup"><span data-stu-id="c9c09-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="c9c09-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c9c09-104">SYNTAX</span></span>

### <span data-ttu-id="c9c09-105">ByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9c09-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9c09-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c9c09-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9c09-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c9c09-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9c09-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c9c09-108">DESCRIPTION</span></span>
<span data-ttu-id="c9c09-109">Eltávolít egy bastion erőforrást. Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span><span class="sxs-lookup"><span data-stu-id="c9c09-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="c9c09-110">Example2 deletes the bastion using its object with pipeline.</span><span class="sxs-lookup"><span data-stu-id="c9c09-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="c9c09-111">Example3 deletes the bastion using its object.</span><span class="sxs-lookup"><span data-stu-id="c9c09-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="c9c09-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c9c09-112">EXAMPLES</span></span>

### <span data-ttu-id="c9c09-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="c9c09-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="c9c09-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c9c09-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="c9c09-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="c9c09-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="c9c09-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9c09-116">PARAMETERS</span></span>

### <span data-ttu-id="c9c09-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9c09-117">-Confirm</span></span>
<span data-ttu-id="c9c09-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c9c09-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9c09-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c09-119">-DefaultProfile</span></span>
<span data-ttu-id="c9c09-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9c09-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9c09-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c9c09-121">-Force</span></span>
<span data-ttu-id="c9c09-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9c09-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c9c09-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9c09-123">-InputObject</span></span>
<span data-ttu-id="c9c09-124">The Bastion object to bedeleted.</span><span class="sxs-lookup"><span data-stu-id="c9c09-124">The Bastion object to be deleted.</span></span>

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

### <span data-ttu-id="c9c09-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c9c09-125">-Name</span></span>
<span data-ttu-id="c9c09-126">A törölni szükséges bastion erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c9c09-126">The bastion resource name to be deleted.</span></span>

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

### <span data-ttu-id="c9c09-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9c09-127">-PassThru</span></span>
<span data-ttu-id="c9c09-128">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtanunk.</span><span class="sxs-lookup"><span data-stu-id="c9c09-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="c9c09-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9c09-129">-ResourceGroupName</span></span>
<span data-ttu-id="c9c09-130">Az erőforráscsoport neve, ahol a bástya létezik.</span><span class="sxs-lookup"><span data-stu-id="c9c09-130">The resource group name where bastion exists.</span></span>

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

### <span data-ttu-id="c9c09-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9c09-131">-ResourceId</span></span>
<span data-ttu-id="c9c09-132">A bazsalika azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="c9c09-132">The Azure resource ID for the Bastion to be deleted.</span></span>

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

### <span data-ttu-id="c9c09-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9c09-133">-WhatIf</span></span>
<span data-ttu-id="c9c09-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c9c09-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9c09-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9c09-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9c09-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c09-136">CommonParameters</span></span>
<span data-ttu-id="c9c09-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9c09-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c09-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9c09-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c09-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9c09-139">INPUTS</span></span>

### <span data-ttu-id="c9c09-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="c9c09-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="c9c09-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c9c09-141">System.String</span></span>

## <span data-ttu-id="c9c09-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9c09-142">OUTPUTS</span></span>

### <span data-ttu-id="c9c09-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c9c09-143">System.Boolean</span></span>

## <span data-ttu-id="c9c09-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c9c09-144">NOTES</span></span>

## <span data-ttu-id="c9c09-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9c09-145">RELATED LINKS</span></span>
[<span data-ttu-id="c9c09-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="c9c09-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="c9c09-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="c9c09-147">New-AzBastion</span></span>](./New-AzBastion.md)