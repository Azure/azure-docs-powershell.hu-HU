---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: e6df93dee8599c6bae42cc9428b2a7691abf4740
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849526"
---
# <span data-ttu-id="534ee-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="534ee-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="534ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="534ee-102">SYNOPSIS</span></span>
<span data-ttu-id="534ee-103">Felügyelt alkalmazás-definíciók beolvasása</span><span class="sxs-lookup"><span data-stu-id="534ee-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="534ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="534ee-104">SYNTAX</span></span>

### <span data-ttu-id="534ee-105">GetByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="534ee-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="534ee-106">GetById</span><span class="sxs-lookup"><span data-stu-id="534ee-106">GetById</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="534ee-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="534ee-107">DESCRIPTION</span></span>
<span data-ttu-id="534ee-108">A **Get-AzureRmManagedApplicationDefinition** parancsmag felügyelt alkalmazás-definíciókat kap</span><span class="sxs-lookup"><span data-stu-id="534ee-108">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="534ee-109">Példák</span><span class="sxs-lookup"><span data-stu-id="534ee-109">EXAMPLES</span></span>

### <span data-ttu-id="534ee-110">Példa 1: az összes felügyelt alkalmazás definíciójának beolvasása egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="534ee-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="534ee-111">Ez a parancs a felügyelt alkalmazások definícióját a "MyRG" erőforráscsoport csoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="534ee-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="534ee-112">2. példa: felügyelt alkalmazás definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="534ee-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="534ee-113">Ez a parancs beolvassa a felügyelt alkalmazás definícióját "myManagedAppDef" az erőforráscsoport "MyRG" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="534ee-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="534ee-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="534ee-114">PARAMETERS</span></span>

### <span data-ttu-id="534ee-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="534ee-115">-ApiVersion</span></span>
<span data-ttu-id="534ee-116">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="534ee-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="534ee-117">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="534ee-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="534ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534ee-118">-DefaultProfile</span></span>
<span data-ttu-id="534ee-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="534ee-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="534ee-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="534ee-120">-Id</span></span>
<span data-ttu-id="534ee-121">A teljes mértékben minősített felügyelt alkalmazás-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="534ee-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="534ee-122">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="534ee-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="534ee-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="534ee-123">-Name</span></span>
<span data-ttu-id="534ee-124">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="534ee-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="534ee-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="534ee-125">-Pre</span></span>
<span data-ttu-id="534ee-126">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="534ee-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="534ee-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="534ee-127">-ResourceGroupName</span></span>
<span data-ttu-id="534ee-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="534ee-128">The resource group name.</span></span>

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

### <span data-ttu-id="534ee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534ee-129">CommonParameters</span></span>
<span data-ttu-id="534ee-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="534ee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534ee-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="534ee-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534ee-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="534ee-132">INPUTS</span></span>

### <span data-ttu-id="534ee-133">System. String</span><span class="sxs-lookup"><span data-stu-id="534ee-133">System.String</span></span>

## <span data-ttu-id="534ee-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="534ee-134">OUTPUTS</span></span>

### <span data-ttu-id="534ee-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="534ee-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="534ee-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="534ee-136">NOTES</span></span>

## <span data-ttu-id="534ee-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="534ee-137">RELATED LINKS</span></span>
