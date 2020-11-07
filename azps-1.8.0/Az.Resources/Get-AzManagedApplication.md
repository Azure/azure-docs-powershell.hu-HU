---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: 9c670973c9fcff3cd9038809cb955efc32edeee0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669444"
---
# <span data-ttu-id="3ffc0-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="3ffc0-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="3ffc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ffc0-102">SYNOPSIS</span></span>
<span data-ttu-id="3ffc0-103">Felügyelt alkalmazásokat kap</span><span class="sxs-lookup"><span data-stu-id="3ffc0-103">Gets managed applications</span></span>

## <span data-ttu-id="3ffc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ffc0-104">SYNTAX</span></span>

### <span data-ttu-id="3ffc0-105">GetBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ffc0-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ffc0-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3ffc0-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ffc0-107">GetById</span><span class="sxs-lookup"><span data-stu-id="3ffc0-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ffc0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ffc0-108">DESCRIPTION</span></span>
<span data-ttu-id="3ffc0-109">A **Get-AzManagedApplication** parancsmag felügyelt alkalmazásokat kap</span><span class="sxs-lookup"><span data-stu-id="3ffc0-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="3ffc0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3ffc0-110">EXAMPLES</span></span>

### <span data-ttu-id="3ffc0-111">Példa 1: az összes felügyelt alkalmazás beolvasása egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="3ffc0-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="3ffc0-112">A parancs a kezelt alkalmazásokat a "MyRG" erőforráscsoport alatt kapja.</span><span class="sxs-lookup"><span data-stu-id="3ffc0-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="3ffc0-113">2. példa: az összes felügyelt alkalmazás beolvasása</span><span class="sxs-lookup"><span data-stu-id="3ffc0-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="3ffc0-114">Ez a parancs beolvassa az összes felügyelt alkalmazást az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="3ffc0-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="3ffc0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ffc0-115">PARAMETERS</span></span>

### <span data-ttu-id="3ffc0-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3ffc0-116">-ApiVersion</span></span>
<span data-ttu-id="3ffc0-117">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ffc0-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3ffc0-118">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3ffc0-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3ffc0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ffc0-119">-DefaultProfile</span></span>
<span data-ttu-id="3ffc0-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ffc0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ffc0-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="3ffc0-121">-Id</span></span>
<span data-ttu-id="3ffc0-122">A teljes mértékben minősített felügyelt alkalmazásspecifikus azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="3ffc0-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="3ffc0-123">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="3ffc0-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffc0-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ffc0-124">-Name</span></span>
<span data-ttu-id="3ffc0-125">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="3ffc0-125">The managed application name.</span></span>

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

### <span data-ttu-id="3ffc0-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="3ffc0-126">-Pre</span></span>
<span data-ttu-id="3ffc0-127">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="3ffc0-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3ffc0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ffc0-128">-ResourceGroupName</span></span>
<span data-ttu-id="3ffc0-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3ffc0-129">The resource group name.</span></span>

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

### <span data-ttu-id="3ffc0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ffc0-130">CommonParameters</span></span>
<span data-ttu-id="3ffc0-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ffc0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ffc0-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ffc0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ffc0-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ffc0-133">INPUTS</span></span>

### <span data-ttu-id="3ffc0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3ffc0-134">System.String</span></span>

## <span data-ttu-id="3ffc0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ffc0-135">OUTPUTS</span></span>

### <span data-ttu-id="3ffc0-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3ffc0-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3ffc0-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ffc0-137">NOTES</span></span>

## <span data-ttu-id="3ffc0-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ffc0-138">RELATED LINKS</span></span>
