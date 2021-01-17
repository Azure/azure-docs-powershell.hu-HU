---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: d14d591ffdc0e20934a0cf758407dc2b4e6e152c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466482"
---
# <span data-ttu-id="74e6a-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="74e6a-101">Move-AzResource</span></span>

## <span data-ttu-id="74e6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="74e6a-103">Áthelyez egy erőforrást egy másik erőforráscsoportba vagy -előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="74e6a-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="74e6a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="74e6a-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74e6a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="74e6a-105">DESCRIPTION</span></span>
<span data-ttu-id="74e6a-106">A **Move-AzResource** parancsmag áthelyezi a meglévő erőforrásokat egy másik erőforráscsoportba.</span><span class="sxs-lookup"><span data-stu-id="74e6a-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="74e6a-107">Az erőforráscsoport másik előfizetésben is lehet.</span><span class="sxs-lookup"><span data-stu-id="74e6a-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="74e6a-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="74e6a-108">EXAMPLES</span></span>

### <span data-ttu-id="74e6a-109">1. példa: Erőforrás áthelyezése erőforráscsoportba</span><span class="sxs-lookup"><span data-stu-id="74e6a-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="74e6a-110">Az első parancs egy ContosoStorageAccount nevű erőforrást kap a Get-AzResource parancsmag használatával, majd az erőforrást a $Resource változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="74e6a-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="74e6a-111">A második parancs áthelyezi az erőforrást az Erőforráscsoport14 nevű erőforráscsoportba.</span><span class="sxs-lookup"><span data-stu-id="74e6a-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="74e6a-112">A parancs azonosítja az áthelyezni  szükséges erőforrást a $Resource.</span><span class="sxs-lookup"><span data-stu-id="74e6a-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="74e6a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74e6a-113">PARAMETERS</span></span>

### <span data-ttu-id="74e6a-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="74e6a-114">-ApiVersion</span></span>
<span data-ttu-id="74e6a-115">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="74e6a-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="74e6a-116">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="74e6a-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="74e6a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74e6a-117">-DefaultProfile</span></span>
<span data-ttu-id="74e6a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="74e6a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74e6a-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74e6a-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="74e6a-120">Annak az erőforráscsoportnak a nevét adja meg, amelybe ez a parancsmag áthelyezi az erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="74e6a-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e6a-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74e6a-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="74e6a-122">Annak az előfizetésnek az azonosítója, amelybe ez a parancsmag áthelyezi az erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="74e6a-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e6a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="74e6a-123">-Force</span></span>
<span data-ttu-id="74e6a-124">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="74e6a-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="74e6a-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="74e6a-125">-Pre</span></span>
<span data-ttu-id="74e6a-126">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="74e6a-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="74e6a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74e6a-127">-ResourceId</span></span>
<span data-ttu-id="74e6a-128">A parancsmag által áthelyezett erőforrások egy tömbje.</span><span class="sxs-lookup"><span data-stu-id="74e6a-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74e6a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74e6a-129">-Confirm</span></span>
<span data-ttu-id="74e6a-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="74e6a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74e6a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74e6a-131">-WhatIf</span></span>
<span data-ttu-id="74e6a-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="74e6a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74e6a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74e6a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74e6a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e6a-134">CommonParameters</span></span>
<span data-ttu-id="74e6a-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74e6a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e6a-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74e6a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e6a-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74e6a-137">INPUTS</span></span>

### <span data-ttu-id="74e6a-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="74e6a-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="74e6a-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="74e6a-139">System.String[]</span></span>

## <span data-ttu-id="74e6a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74e6a-140">OUTPUTS</span></span>

### <span data-ttu-id="74e6a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74e6a-141">System.Boolean</span></span>

## <span data-ttu-id="74e6a-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="74e6a-142">NOTES</span></span>

## <span data-ttu-id="74e6a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74e6a-143">RELATED LINKS</span></span>

[<span data-ttu-id="74e6a-144">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="74e6a-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="74e6a-145">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="74e6a-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="74e6a-146">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="74e6a-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="74e6a-147">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="74e6a-147">Set-AzResource</span></span>](./Set-AzResource.md)


