---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: e53e5311b4553dc3803a4a6d9ac31d6a2569bbc0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195545"
---
# <span data-ttu-id="675ed-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="675ed-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="675ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="675ed-102">SYNOPSIS</span></span>
<span data-ttu-id="675ed-103">Erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="675ed-103">Removes a resource group.</span></span>

## <span data-ttu-id="675ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="675ed-104">SYNTAX</span></span>

### <span data-ttu-id="675ed-105">RemoveByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="675ed-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="675ed-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="675ed-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="675ed-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="675ed-107">DESCRIPTION</span></span>
<span data-ttu-id="675ed-108">A **Remove-AzResourceGroup** parancsmag egy Azure-erőforráscsoport és erőforrásai törlődnek az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="675ed-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="675ed-109">Ha törölni szeretne egy erőforrást, de elhagyja az erőforrás csoportját, használja az Remove-AzResource parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="675ed-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="675ed-110">Példák</span><span class="sxs-lookup"><span data-stu-id="675ed-110">EXAMPLES</span></span>

### <span data-ttu-id="675ed-111">1. példa: erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="675ed-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="675ed-112">Ez a parancs eltávolítja a ContosoRG01 erőforráscsoportot az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="675ed-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="675ed-113">A parancsmag kéri a megerősítést, és a nincs kimenet értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="675ed-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="675ed-114">2. példa: erőforráscsoportok eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="675ed-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Force
```

<span data-ttu-id="675ed-115">Ez a parancs az Get-AzResourceGroup parancsmagot használja az erőforráscsoport ContosoRG01 beolvasásához, majd átadja a AzResourceGroup a csővezeték **-** kezelő használatával.</span><span class="sxs-lookup"><span data-stu-id="675ed-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span> <span data-ttu-id="675ed-116">Az *erő* paraméter letiltja a megerősítési üzenetet.</span><span class="sxs-lookup"><span data-stu-id="675ed-116">The *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="675ed-117">3. példa: az összes erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="675ed-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="675ed-118">Ez a parancs a **Get-AzResourceGroup** parancsmagot használja az összes erőforráscsoport beolvasására, majd átadja azokat a **AzResourceGroup** a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="675ed-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="675ed-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="675ed-119">PARAMETERS</span></span>

### <span data-ttu-id="675ed-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="675ed-120">-ApiVersion</span></span>
<span data-ttu-id="675ed-121">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="675ed-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="675ed-122">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="675ed-122">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="675ed-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="675ed-123">-AsJob</span></span>
<span data-ttu-id="675ed-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="675ed-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="675ed-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="675ed-125">-DefaultProfile</span></span>
<span data-ttu-id="675ed-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="675ed-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="675ed-127">-Force</span><span class="sxs-lookup"><span data-stu-id="675ed-127">-Force</span></span>
<span data-ttu-id="675ed-128">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="675ed-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="675ed-129">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="675ed-129">-Id</span></span>
<span data-ttu-id="675ed-130">Az eltávolítandó erőforráscsoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="675ed-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="675ed-131">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="675ed-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="675ed-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="675ed-132">-Name</span></span>
<span data-ttu-id="675ed-133">Az eltávolítandó erőforráscsoportok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="675ed-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="675ed-134">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="675ed-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="675ed-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="675ed-135">-Pre</span></span>
<span data-ttu-id="675ed-136">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="675ed-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="675ed-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="675ed-137">-Confirm</span></span>
<span data-ttu-id="675ed-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="675ed-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="675ed-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="675ed-139">-WhatIf</span></span>
<span data-ttu-id="675ed-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="675ed-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="675ed-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="675ed-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="675ed-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="675ed-142">CommonParameters</span></span>
<span data-ttu-id="675ed-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="675ed-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="675ed-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="675ed-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="675ed-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="675ed-145">INPUTS</span></span>

### <span data-ttu-id="675ed-146">System. String</span><span class="sxs-lookup"><span data-stu-id="675ed-146">System.String</span></span>

## <span data-ttu-id="675ed-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="675ed-147">OUTPUTS</span></span>

### <span data-ttu-id="675ed-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="675ed-148">System.Boolean</span></span>

## <span data-ttu-id="675ed-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="675ed-149">NOTES</span></span>

## <span data-ttu-id="675ed-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="675ed-150">RELATED LINKS</span></span>

[<span data-ttu-id="675ed-151">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="675ed-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="675ed-152">Új – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="675ed-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="675ed-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="675ed-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

