---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 3479a3d720554f0c062e2410d0c4b838f655909a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679715"
---
# <span data-ttu-id="f7a74-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="f7a74-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="f7a74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7a74-102">SYNOPSIS</span></span>
<span data-ttu-id="f7a74-103">Felügyelt alkalmazás definíciójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f7a74-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7a74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7a74-104">SYNTAX</span></span>

### <span data-ttu-id="f7a74-105">RemoveByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7a74-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7a74-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="f7a74-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7a74-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7a74-107">DESCRIPTION</span></span>
<span data-ttu-id="f7a74-108">A **Remove-AzureRmManagedApplicationDefinition** parancsmag eltávolít egy felügyelt alkalmazás-definíciót</span><span class="sxs-lookup"><span data-stu-id="f7a74-108">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="f7a74-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f7a74-109">EXAMPLES</span></span>

### <span data-ttu-id="f7a74-110">Példa 1: a felügyelt alkalmazás definíciójának eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="f7a74-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="f7a74-111">Az első parancs az Get-AzureRmManagedApplicationDefinition parancsmag használatával megkapja a myAppDef nevű felügyelt alkalmazás definícióját.</span><span class="sxs-lookup"><span data-stu-id="f7a74-111">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="f7a74-112">A parancs a $ApplicationDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f7a74-112">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="f7a74-113">A második parancs eltávolítja a felügyelt alkalmazás definícióját, amelyet az $ApplicationDefinition **ResourceId** tulajdonsága határoz meg.</span><span class="sxs-lookup"><span data-stu-id="f7a74-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="f7a74-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7a74-114">PARAMETERS</span></span>

### <span data-ttu-id="f7a74-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f7a74-115">-ApiVersion</span></span>
<span data-ttu-id="f7a74-116">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7a74-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f7a74-117">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f7a74-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f7a74-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7a74-118">-DefaultProfile</span></span>
<span data-ttu-id="f7a74-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7a74-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7a74-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f7a74-120">-Force</span></span>
<span data-ttu-id="f7a74-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7a74-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f7a74-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f7a74-122">-Id</span></span>
<span data-ttu-id="f7a74-123">A teljes mértékben minősített felügyelt alkalmazás-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="f7a74-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="f7a74-124">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="f7a74-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7a74-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f7a74-125">-Name</span></span>
<span data-ttu-id="f7a74-126">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="f7a74-126">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7a74-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="f7a74-127">-Pre</span></span>
<span data-ttu-id="f7a74-128">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f7a74-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f7a74-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7a74-129">-ResourceGroupName</span></span>
<span data-ttu-id="f7a74-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f7a74-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7a74-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f7a74-131">-Confirm</span></span>
<span data-ttu-id="f7a74-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7a74-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7a74-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7a74-133">-WhatIf</span></span>
<span data-ttu-id="f7a74-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f7a74-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7a74-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7a74-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7a74-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7a74-136">CommonParameters</span></span>
<span data-ttu-id="f7a74-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7a74-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7a74-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7a74-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7a74-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7a74-139">INPUTS</span></span>

### <span data-ttu-id="f7a74-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f7a74-140">System.String</span></span>

## <span data-ttu-id="f7a74-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7a74-141">OUTPUTS</span></span>

### <span data-ttu-id="f7a74-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7a74-142">System.Boolean</span></span>

## <span data-ttu-id="f7a74-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7a74-143">NOTES</span></span>

## <span data-ttu-id="f7a74-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7a74-144">RELATED LINKS</span></span>
