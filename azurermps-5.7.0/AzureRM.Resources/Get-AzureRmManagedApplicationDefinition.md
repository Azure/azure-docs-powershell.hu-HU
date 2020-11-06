---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 9dec17ba09bf76ec7e8f3323b7cfd0557e08e525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501420"
---
# <span data-ttu-id="fd723-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="fd723-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="fd723-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd723-102">SYNOPSIS</span></span>
<span data-ttu-id="fd723-103">Felügyelt alkalmazás-definíciók beolvasása</span><span class="sxs-lookup"><span data-stu-id="fd723-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd723-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd723-104">SYNTAX</span></span>

### <span data-ttu-id="fd723-105">GetByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd723-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd723-106">GetById</span><span class="sxs-lookup"><span data-stu-id="fd723-106">GetById</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd723-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd723-107">DESCRIPTION</span></span>
<span data-ttu-id="fd723-108">A **Get-AzureRmManagedApplicationDefinition** parancsmag felügyelt alkalmazás-definíciókat kap</span><span class="sxs-lookup"><span data-stu-id="fd723-108">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="fd723-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fd723-109">EXAMPLES</span></span>

### <span data-ttu-id="fd723-110">Példa 1: az összes felügyelt alkalmazás definíciójának beolvasása egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="fd723-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="fd723-111">Ez a parancs a felügyelt alkalmazások definícióját a "MyRG" erőforráscsoport csoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fd723-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="fd723-112">2. példa: felügyelt alkalmazás definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="fd723-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="fd723-113">Ez a parancs beolvassa a felügyelt alkalmazás definícióját "myManagedAppDef" az erőforráscsoport "MyRG" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="fd723-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="fd723-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd723-114">PARAMETERS</span></span>

### <span data-ttu-id="fd723-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fd723-115">-ApiVersion</span></span>
<span data-ttu-id="fd723-116">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd723-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fd723-117">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fd723-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fd723-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd723-118">-DefaultProfile</span></span>
<span data-ttu-id="fd723-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd723-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd723-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="fd723-120">-Id</span></span>
<span data-ttu-id="fd723-121">A teljes mértékben minősített felügyelt alkalmazás-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="fd723-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="fd723-122">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="fd723-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd723-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd723-123">-Name</span></span>
<span data-ttu-id="fd723-124">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="fd723-124">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd723-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="fd723-125">-Pre</span></span>
<span data-ttu-id="fd723-126">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="fd723-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fd723-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd723-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd723-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd723-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd723-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd723-129">CommonParameters</span></span>
<span data-ttu-id="fd723-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd723-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd723-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd723-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd723-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd723-132">INPUTS</span></span>

### <span data-ttu-id="fd723-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fd723-133">System.String</span></span>

## <span data-ttu-id="fd723-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd723-134">OUTPUTS</span></span>

### <span data-ttu-id="fd723-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fd723-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fd723-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd723-136">NOTES</span></span>

## <span data-ttu-id="fd723-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd723-137">RELATED LINKS</span></span>
