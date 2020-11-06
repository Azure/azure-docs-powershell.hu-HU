---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: c5bbefe1edc36d63dcac53ad85923da3f75d80e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500136"
---
# <span data-ttu-id="b1deb-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="b1deb-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="b1deb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1deb-102">SYNOPSIS</span></span>
<span data-ttu-id="b1deb-103">Felügyelt alkalmazás-definíciók beolvasása</span><span class="sxs-lookup"><span data-stu-id="b1deb-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1deb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1deb-104">SYNTAX</span></span>

### <span data-ttu-id="b1deb-105">GetByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b1deb-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1deb-106">GetById</span><span class="sxs-lookup"><span data-stu-id="b1deb-106">GetById</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1deb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1deb-107">DESCRIPTION</span></span>
<span data-ttu-id="b1deb-108">A **Get-AzureRmManagedApplicationDefinition** parancsmag felügyelt alkalmazás-definíciókat kap</span><span class="sxs-lookup"><span data-stu-id="b1deb-108">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="b1deb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b1deb-109">EXAMPLES</span></span>

### <span data-ttu-id="b1deb-110">Példa 1: az összes felügyelt alkalmazás definíciójának beolvasása egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="b1deb-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="b1deb-111">Ez a parancs a felügyelt alkalmazások definícióját a "MyRG" erőforráscsoport csoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b1deb-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="b1deb-112">2. példa: felügyelt alkalmazás definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="b1deb-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="b1deb-113">Ez a parancs beolvassa a felügyelt alkalmazás definícióját "myManagedAppDef" az erőforráscsoport "MyRG" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="b1deb-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="b1deb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1deb-114">PARAMETERS</span></span>

### <span data-ttu-id="b1deb-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b1deb-115">-ApiVersion</span></span>
<span data-ttu-id="b1deb-116">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1deb-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b1deb-117">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b1deb-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b1deb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1deb-118">-DefaultProfile</span></span>
<span data-ttu-id="b1deb-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1deb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1deb-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="b1deb-120">-Id</span></span>
<span data-ttu-id="b1deb-121">A teljes mértékben minősített felügyelt alkalmazás-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="b1deb-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="b1deb-122">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b1deb-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="b1deb-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b1deb-123">-Name</span></span>
<span data-ttu-id="b1deb-124">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="b1deb-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="b1deb-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="b1deb-125">-Pre</span></span>
<span data-ttu-id="b1deb-126">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b1deb-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b1deb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1deb-127">-ResourceGroupName</span></span>
<span data-ttu-id="b1deb-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b1deb-128">The resource group name.</span></span>

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

### <span data-ttu-id="b1deb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1deb-129">CommonParameters</span></span>
<span data-ttu-id="b1deb-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1deb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1deb-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1deb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1deb-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1deb-132">INPUTS</span></span>

### <span data-ttu-id="b1deb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b1deb-133">System.String</span></span>

## <span data-ttu-id="b1deb-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1deb-134">OUTPUTS</span></span>

### <span data-ttu-id="b1deb-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b1deb-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b1deb-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1deb-136">NOTES</span></span>

## <span data-ttu-id="b1deb-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1deb-137">RELATED LINKS</span></span>
