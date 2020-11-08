---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184102"
---
# <span data-ttu-id="4ce76-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="4ce76-101">Remove-AzBastion</span></span>

## <span data-ttu-id="4ce76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ce76-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce76-103">Egy bástya-erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="4ce76-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="4ce76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ce76-104">SYNTAX</span></span>

### <span data-ttu-id="4ce76-105">ByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ce76-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ce76-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ce76-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ce76-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce76-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ce76-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ce76-108">DESCRIPTION</span></span>
<span data-ttu-id="4ce76-109">Egy bástya-erőforrás eltávolítása. Example1: a bástya törlése a ResourceGroupName és a ResourceName használatával.</span><span class="sxs-lookup"><span data-stu-id="4ce76-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="4ce76-110">A pelda2 törli a bástya objektumát a pipeline használatával.</span><span class="sxs-lookup"><span data-stu-id="4ce76-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="4ce76-111">A Example3 a bástya objektummal történő törlésével törli a bástya-t.</span><span class="sxs-lookup"><span data-stu-id="4ce76-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="4ce76-112">Példák</span><span class="sxs-lookup"><span data-stu-id="4ce76-112">EXAMPLES</span></span>

### <span data-ttu-id="4ce76-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4ce76-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="4ce76-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="4ce76-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="4ce76-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="4ce76-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="4ce76-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ce76-116">PARAMETERS</span></span>

### <span data-ttu-id="4ce76-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4ce76-117">-Confirm</span></span>
<span data-ttu-id="4ce76-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ce76-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce76-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce76-119">-DefaultProfile</span></span>
<span data-ttu-id="4ce76-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ce76-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ce76-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4ce76-121">-Force</span></span>
<span data-ttu-id="4ce76-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ce76-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4ce76-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ce76-123">-InputObject</span></span>
<span data-ttu-id="4ce76-124">A törölni kívánt Bastion-objektum.</span><span class="sxs-lookup"><span data-stu-id="4ce76-124">The Bastion object to be deleted.</span></span>

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

### <span data-ttu-id="4ce76-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ce76-125">-Name</span></span>
<span data-ttu-id="4ce76-126">A kitörölni kívánt bástya-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4ce76-126">The bastion resource name to be deleted.</span></span>

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

### <span data-ttu-id="4ce76-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ce76-127">-PassThru</span></span>
<span data-ttu-id="4ce76-128">Egy olyan objektumot ad eredményül, amely azt az elemet jeleníti meg, amelyen a művelet végre van hajtva.</span><span class="sxs-lookup"><span data-stu-id="4ce76-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="4ce76-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce76-129">-ResourceGroupName</span></span>
<span data-ttu-id="4ce76-130">Az erőforráscsoport neve, ahol a bástya létezik.</span><span class="sxs-lookup"><span data-stu-id="4ce76-130">The resource group name where bastion exists.</span></span>

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

### <span data-ttu-id="4ce76-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce76-131">-ResourceId</span></span>
<span data-ttu-id="4ce76-132">A törlendő bástya Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="4ce76-132">The Azure resource ID for the Bastion to be deleted.</span></span>

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

### <span data-ttu-id="4ce76-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce76-133">-WhatIf</span></span>
<span data-ttu-id="4ce76-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4ce76-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ce76-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ce76-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce76-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce76-136">CommonParameters</span></span>
<span data-ttu-id="4ce76-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ce76-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce76-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4ce76-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce76-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ce76-139">INPUTS</span></span>

### <span data-ttu-id="4ce76-140">Microsoft. Azure. commands. Network. models. PSBastion</span><span class="sxs-lookup"><span data-stu-id="4ce76-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="4ce76-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4ce76-141">System.String</span></span>

## <span data-ttu-id="4ce76-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ce76-142">OUTPUTS</span></span>

### <span data-ttu-id="4ce76-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ce76-143">System.Boolean</span></span>

## <span data-ttu-id="4ce76-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ce76-144">NOTES</span></span>

## <span data-ttu-id="4ce76-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ce76-145">RELATED LINKS</span></span>
[<span data-ttu-id="4ce76-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="4ce76-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="4ce76-147">Új – AzBastion</span><span class="sxs-lookup"><span data-stu-id="4ce76-147">New-AzBastion</span></span>](./New-AzBastion.md)