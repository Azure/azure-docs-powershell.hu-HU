---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: 232f8de58bb6026a2932631ac2f9e3ed77c71b91
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843233"
---
# <span data-ttu-id="24822-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24822-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="24822-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24822-102">SYNOPSIS</span></span>
<span data-ttu-id="24822-103">Erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="24822-103">Removes a resource group.</span></span>

## <span data-ttu-id="24822-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24822-104">SYNTAX</span></span>

### <span data-ttu-id="24822-105">RemoveByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24822-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24822-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="24822-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup [-Id] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24822-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="24822-107">DESCRIPTION</span></span>
<span data-ttu-id="24822-108">A **Remove-AzResourceGroup** parancsmag egy Azure-erőforráscsoport és erőforrásai törlődnek az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="24822-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="24822-109">Ha törölni szeretne egy erőforrást, de elhagyja az erőforrás csoportját, használja az Remove-AzResource parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="24822-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="24822-110">Példák</span><span class="sxs-lookup"><span data-stu-id="24822-110">EXAMPLES</span></span>

### <span data-ttu-id="24822-111">1. példa: erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="24822-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="24822-112">Ez a parancs eltávolítja a ContosoRG01 erőforráscsoportot az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="24822-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="24822-113">A parancsmag kéri a megerősítést, és a nincs kimenet értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="24822-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="24822-114">2. példa: erőforráscsoportok eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="24822-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Verbose -Force
```

<span data-ttu-id="24822-115">Ez a parancs az Get-AzResourceGroup parancsmagot használja az erőforráscsoport ContosoRG01 beolvasásához, majd átadja a AzResourceGroup a csővezeték **-** kezelő használatával.</span><span class="sxs-lookup"><span data-stu-id="24822-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="24822-116">A *részletes* általános paraméter információkat kap a műveletről, és az *erő* paraméter letiltja a megerősítési üzenetet.</span><span class="sxs-lookup"><span data-stu-id="24822-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="24822-117">3. példa: az összes erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="24822-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="24822-118">Ez a parancs a **Get-AzResourceGroup** parancsmagot használja az összes erőforráscsoport beolvasására, majd átadja azokat a **AzResourceGroup** a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="24822-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="24822-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24822-119">PARAMETERS</span></span>

### <span data-ttu-id="24822-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="24822-120">-ApiVersion</span></span>
<span data-ttu-id="24822-121">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="24822-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="24822-122">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="24822-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="24822-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24822-123">-AsJob</span></span>
<span data-ttu-id="24822-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="24822-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24822-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24822-125">-DefaultProfile</span></span>
<span data-ttu-id="24822-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="24822-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24822-127">-Force</span><span class="sxs-lookup"><span data-stu-id="24822-127">-Force</span></span>
<span data-ttu-id="24822-128">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="24822-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="24822-129">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="24822-129">-Id</span></span>
<span data-ttu-id="24822-130">Az eltávolítandó erőforráscsoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="24822-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="24822-131">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="24822-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24822-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24822-132">-Name</span></span>
<span data-ttu-id="24822-133">Az eltávolítandó erőforráscsoportok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="24822-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="24822-134">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="24822-134">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="24822-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="24822-135">-Pre</span></span>
<span data-ttu-id="24822-136">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="24822-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="24822-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24822-137">-Confirm</span></span>
<span data-ttu-id="24822-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24822-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24822-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24822-139">-WhatIf</span></span>
<span data-ttu-id="24822-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24822-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24822-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24822-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24822-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24822-142">CommonParameters</span></span>
<span data-ttu-id="24822-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24822-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24822-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24822-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24822-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24822-145">INPUTS</span></span>

## <span data-ttu-id="24822-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24822-146">OUTPUTS</span></span>

## <span data-ttu-id="24822-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24822-147">NOTES</span></span>

## <span data-ttu-id="24822-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24822-148">RELATED LINKS</span></span>

[<span data-ttu-id="24822-149">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24822-149">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="24822-150">Új – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24822-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="24822-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24822-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


