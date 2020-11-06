---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: ce028e52d893372f4a668a278466d4cdc51655f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498843"
---
# <span data-ttu-id="f5574-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5574-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="f5574-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5574-102">SYNOPSIS</span></span>
<span data-ttu-id="f5574-103">Erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5574-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5574-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5574-104">SYNTAX</span></span>

### <span data-ttu-id="f5574-105">RemoveByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5574-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5574-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="f5574-106">RemoveByResourceGroupId</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5574-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5574-107">DESCRIPTION</span></span>
<span data-ttu-id="f5574-108">A **Remove-AzureRmResourceGroup** parancsmag egy Azure-erőforráscsoport és erőforrásai törlődnek az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="f5574-108">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="f5574-109">Ha törölni szeretne egy erőforrást, de elhagyja az erőforrás csoportját, használja az Remove-AzureRmResource parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f5574-109">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="f5574-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f5574-110">EXAMPLES</span></span>

### <span data-ttu-id="f5574-111">1. példa: erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5574-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="f5574-112">Ez a parancs eltávolítja a ContosoRG01 erőforráscsoportot az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="f5574-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="f5574-113">A parancsmag kéri a megerősítést, és a nincs kimenet értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f5574-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="f5574-114">2. példa: erőforráscsoportok eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="f5574-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="f5574-115">Ez a parancs az Get-AzureRmResourceGroup parancsmagot használja az erőforráscsoport ContosoRG01 beolvasásához, majd átadja a AzureRmResourceGroup a csővezeték **-** kezelő használatával.</span><span class="sxs-lookup"><span data-stu-id="f5574-115">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="f5574-116">A *részletes* általános paraméter információkat kap a műveletről, és az *erő* paraméter letiltja a megerősítési üzenetet.</span><span class="sxs-lookup"><span data-stu-id="f5574-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="f5574-117">3. példa: az összes erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5574-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="f5574-118">Ez a parancs a **Get-AzureRmResourceGroup** parancsmagot használja az összes erőforráscsoport beolvasására, majd átadja azokat a **AzureRmResourceGroup** a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="f5574-118">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="f5574-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5574-119">PARAMETERS</span></span>

### <span data-ttu-id="f5574-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f5574-120">-ApiVersion</span></span>
<span data-ttu-id="f5574-121">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5574-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f5574-122">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="f5574-122">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5574-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5574-123">-AsJob</span></span>
<span data-ttu-id="f5574-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f5574-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5574-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5574-125">-DefaultProfile</span></span>
<span data-ttu-id="f5574-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f5574-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5574-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f5574-127">-Force</span></span>
<span data-ttu-id="f5574-128">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f5574-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f5574-129">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f5574-129">-Id</span></span>
<span data-ttu-id="f5574-130">Az eltávolítandó erőforráscsoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5574-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="f5574-131">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="f5574-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5574-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5574-132">-Name</span></span>
<span data-ttu-id="f5574-133">Az eltávolítandó erőforráscsoportok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5574-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="f5574-134">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="f5574-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5574-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="f5574-135">-Pre</span></span>
<span data-ttu-id="f5574-136">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f5574-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f5574-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5574-137">-Confirm</span></span>
<span data-ttu-id="f5574-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5574-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5574-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5574-139">-WhatIf</span></span>
<span data-ttu-id="f5574-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5574-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5574-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5574-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5574-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5574-142">CommonParameters</span></span>
<span data-ttu-id="f5574-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5574-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5574-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5574-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5574-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5574-145">INPUTS</span></span>

### <span data-ttu-id="f5574-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="f5574-146">None</span></span>

## <span data-ttu-id="f5574-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5574-147">OUTPUTS</span></span>

### <span data-ttu-id="f5574-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="f5574-148">None</span></span>

## <span data-ttu-id="f5574-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5574-149">NOTES</span></span>

## <span data-ttu-id="f5574-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5574-150">RELATED LINKS</span></span>

[<span data-ttu-id="f5574-151">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5574-151">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="f5574-152">Új – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5574-152">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="f5574-153">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5574-153">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


