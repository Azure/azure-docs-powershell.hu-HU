---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: 6938cf80f3fa6fb20252e1e4a212133ecd1c62a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500715"
---
# <span data-ttu-id="ee14b-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ee14b-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="ee14b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee14b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee14b-103">Erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ee14b-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee14b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee14b-104">SYNTAX</span></span>

### <span data-ttu-id="ee14b-105">A név alapján jeleníti meg az erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="ee14b-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="ee14b-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="ee14b-106">(Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee14b-107">Felsorolja az azonosító alapján az erőforráscsoport listáját.</span><span class="sxs-lookup"><span data-stu-id="ee14b-107">Lists the resource group based in the Id.</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee14b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee14b-108">DESCRIPTION</span></span>
<span data-ttu-id="ee14b-109">A **Remove-AzureRmResourceGroup** parancsmag egy Azure-erőforráscsoport és erőforrásai törlődnek az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="ee14b-109">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="ee14b-110">Ha törölni szeretne egy erőforrást, de elhagyja az erőforrás csoportját, használja az Remove-AzureRmResource parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ee14b-110">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="ee14b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ee14b-111">EXAMPLES</span></span>

### <span data-ttu-id="ee14b-112">1. példa: erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ee14b-112">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="ee14b-113">Ez a parancs eltávolítja a ContosoRG01 erőforráscsoportot az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="ee14b-113">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="ee14b-114">A parancsmag kéri a megerősítést, és a nincs kimenet értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ee14b-114">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="ee14b-115">2. példa: erőforráscsoportok eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="ee14b-115">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="ee14b-116">Ez a parancs az Get-AzureRmResourceGroup parancsmagot használja az erőforráscsoport ContosoRG01 beolvasásához, majd átadja a AzureRmResourceGroup a csővezeték **-** kezelő használatával.</span><span class="sxs-lookup"><span data-stu-id="ee14b-116">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="ee14b-117">A *részletes* általános paraméter információkat kap a műveletről, és az *erő* paraméter letiltja a megerősítési üzenetet.</span><span class="sxs-lookup"><span data-stu-id="ee14b-117">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="ee14b-118">3. példa: az összes erőforráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ee14b-118">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="ee14b-119">Ez a parancs a **Get-AzureRmResourceGroup** parancsmagot használja az összes erőforráscsoport beolvasására, majd átadja azokat a **AzureRmResourceGroup** a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="ee14b-119">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="ee14b-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee14b-120">PARAMETERS</span></span>

### <span data-ttu-id="ee14b-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ee14b-121">-ApiVersion</span></span>
<span data-ttu-id="ee14b-122">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee14b-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ee14b-123">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="ee14b-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ee14b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ee14b-124">-Force</span></span>
<span data-ttu-id="ee14b-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ee14b-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ee14b-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ee14b-126">-Id</span></span>
<span data-ttu-id="ee14b-127">Az eltávolítandó erőforráscsoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee14b-127">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="ee14b-128">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="ee14b-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee14b-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee14b-129">-Name</span></span>
<span data-ttu-id="ee14b-130">Az eltávolítandó erőforráscsoportok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee14b-130">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="ee14b-131">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="ee14b-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee14b-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="ee14b-132">-Pre</span></span>
<span data-ttu-id="ee14b-133">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ee14b-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ee14b-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee14b-134">-Confirm</span></span>
<span data-ttu-id="ee14b-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee14b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee14b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee14b-136">-WhatIf</span></span>
<span data-ttu-id="ee14b-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee14b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee14b-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee14b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee14b-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee14b-139">-DefaultProfile</span></span>
<span data-ttu-id="ee14b-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee14b-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee14b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee14b-141">CommonParameters</span></span>
<span data-ttu-id="ee14b-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee14b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee14b-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee14b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee14b-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee14b-144">INPUTS</span></span>

### <span data-ttu-id="ee14b-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="ee14b-145">None</span></span>

## <span data-ttu-id="ee14b-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee14b-146">OUTPUTS</span></span>

### <span data-ttu-id="ee14b-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="ee14b-147">None</span></span>

## <span data-ttu-id="ee14b-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee14b-148">NOTES</span></span>

## <span data-ttu-id="ee14b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee14b-149">RELATED LINKS</span></span>

[<span data-ttu-id="ee14b-150">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ee14b-150">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="ee14b-151">Új – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ee14b-151">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="ee14b-152">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ee14b-152">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


