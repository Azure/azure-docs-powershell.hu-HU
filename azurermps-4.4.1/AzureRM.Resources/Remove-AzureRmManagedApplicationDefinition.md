---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 2e951452789d57d6d5e126fca80713ef7fd2c584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503212"
---
# <span data-ttu-id="3598b-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="3598b-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="3598b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3598b-102">SYNOPSIS</span></span>
<span data-ttu-id="3598b-103">Felügyelt alkalmazás definíciójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3598b-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3598b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3598b-104">SYNTAX</span></span>

### <span data-ttu-id="3598b-105">A Managed Application Definition Name paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="3598b-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="3598b-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="3598b-106">(Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3598b-107">A felügyelt alkalmazás-definíciós azonosító paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="3598b-107">The managed application definition Id parameter set.</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3598b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3598b-108">DESCRIPTION</span></span>
<span data-ttu-id="3598b-109">A **Remove-AzureRmManagedApplicationDefinition** parancsmag eltávolít egy felügyelt alkalmazás-definíciót</span><span class="sxs-lookup"><span data-stu-id="3598b-109">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="3598b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3598b-110">EXAMPLES</span></span>

### <span data-ttu-id="3598b-111">Példa 1: a felügyelt alkalmazás definíciójának eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="3598b-111">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="3598b-112">Az első parancs az Get-AzureRmManagedApplicationDefinition parancsmag használatával megkapja a myAppDef nevű felügyelt alkalmazás definícióját.</span><span class="sxs-lookup"><span data-stu-id="3598b-112">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="3598b-113">A parancs a $ApplicationDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3598b-113">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="3598b-114">A második parancs eltávolítja a felügyelt alkalmazás definícióját, amelyet az $ApplicationDefinition **ResourceId** tulajdonsága határoz meg.</span><span class="sxs-lookup"><span data-stu-id="3598b-114">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="3598b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3598b-115">PARAMETERS</span></span>

### <span data-ttu-id="3598b-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3598b-116">-ApiVersion</span></span>
<span data-ttu-id="3598b-117">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3598b-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3598b-118">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3598b-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3598b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3598b-119">-DefaultProfile</span></span>
<span data-ttu-id="3598b-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3598b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3598b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3598b-121">-Force</span></span>
<span data-ttu-id="3598b-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3598b-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3598b-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="3598b-123">-Id</span></span>
<span data-ttu-id="3598b-124">A teljes mértékben minősített felügyelt alkalmazás-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="3598b-124">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="3598b-125">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="3598b-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3598b-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3598b-126">-Name</span></span>
<span data-ttu-id="3598b-127">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="3598b-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3598b-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="3598b-128">-Pre</span></span>
<span data-ttu-id="3598b-129">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="3598b-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3598b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3598b-130">-ResourceGroupName</span></span>
<span data-ttu-id="3598b-131">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3598b-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3598b-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3598b-132">-Confirm</span></span>
<span data-ttu-id="3598b-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3598b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3598b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3598b-134">-WhatIf</span></span>
<span data-ttu-id="3598b-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3598b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3598b-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3598b-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3598b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3598b-137">CommonParameters</span></span>
<span data-ttu-id="3598b-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3598b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3598b-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3598b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3598b-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3598b-140">INPUTS</span></span>

### <span data-ttu-id="3598b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3598b-141">System.String</span></span>

## <span data-ttu-id="3598b-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3598b-142">OUTPUTS</span></span>

### <span data-ttu-id="3598b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3598b-143">System.Boolean</span></span>

## <span data-ttu-id="3598b-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3598b-144">NOTES</span></span>

## <span data-ttu-id="3598b-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3598b-145">RELATED LINKS</span></span>

