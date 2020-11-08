---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: 499b2c68dbebdcc16e816c5ce5e76f9b671139f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182695"
---
# <span data-ttu-id="15b73-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="15b73-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="15b73-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15b73-102">SYNOPSIS</span></span>
<span data-ttu-id="15b73-103">Felügyelt alkalmazás-definíciók beolvasása</span><span class="sxs-lookup"><span data-stu-id="15b73-103">Gets managed application definitions</span></span>

## <span data-ttu-id="15b73-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15b73-104">SYNTAX</span></span>

### <span data-ttu-id="15b73-105">GetByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15b73-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15b73-106">GetById</span><span class="sxs-lookup"><span data-stu-id="15b73-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15b73-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="15b73-107">DESCRIPTION</span></span>
<span data-ttu-id="15b73-108">A **Get-AzManagedApplicationDefinition** parancsmag felügyelt alkalmazás-definíciókat kap</span><span class="sxs-lookup"><span data-stu-id="15b73-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="15b73-109">Példák</span><span class="sxs-lookup"><span data-stu-id="15b73-109">EXAMPLES</span></span>

### <span data-ttu-id="15b73-110">Példa 1: az összes felügyelt alkalmazás definíciójának beolvasása egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="15b73-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="15b73-111">Ez a parancs a felügyelt alkalmazások definícióját a "MyRG" erőforráscsoport csoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="15b73-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="15b73-112">2. példa: felügyelt alkalmazás definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="15b73-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="15b73-113">Ez a parancs beolvassa a felügyelt alkalmazás definícióját "myManagedAppDef" az erőforráscsoport "MyRG" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="15b73-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="15b73-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15b73-114">PARAMETERS</span></span>

### <span data-ttu-id="15b73-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="15b73-115">-ApiVersion</span></span>
<span data-ttu-id="15b73-116">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="15b73-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="15b73-117">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="15b73-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="15b73-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b73-118">-DefaultProfile</span></span>
<span data-ttu-id="15b73-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15b73-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15b73-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="15b73-120">-Id</span></span>
<span data-ttu-id="15b73-121">A teljes mértékben minősített felügyelt alkalmazás-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="15b73-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="15b73-122">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="15b73-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b73-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="15b73-123">-Name</span></span>
<span data-ttu-id="15b73-124">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="15b73-124">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b73-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="15b73-125">-Pre</span></span>
<span data-ttu-id="15b73-126">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="15b73-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="15b73-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15b73-127">-ResourceGroupName</span></span>
<span data-ttu-id="15b73-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="15b73-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b73-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b73-129">CommonParameters</span></span>
<span data-ttu-id="15b73-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15b73-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b73-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="15b73-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b73-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15b73-132">INPUTS</span></span>

### <span data-ttu-id="15b73-133">System. String</span><span class="sxs-lookup"><span data-stu-id="15b73-133">System.String</span></span>

## <span data-ttu-id="15b73-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15b73-134">OUTPUTS</span></span>

### <span data-ttu-id="15b73-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="15b73-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="15b73-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15b73-136">NOTES</span></span>

## <span data-ttu-id="15b73-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15b73-137">RELATED LINKS</span></span>
