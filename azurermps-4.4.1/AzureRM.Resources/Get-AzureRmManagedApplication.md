---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 953a810585550ec8895fc9306f78633beb4846a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493375"
---
# <span data-ttu-id="84142-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="84142-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="84142-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84142-102">SYNOPSIS</span></span>
<span data-ttu-id="84142-103">Felügyelt alkalmazásokat kap</span><span class="sxs-lookup"><span data-stu-id="84142-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84142-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84142-104">SYNTAX</span></span>

### <span data-ttu-id="84142-105">A listában az összes felügyelt alkalmazás paraméter van beállítva.</span><span class="sxs-lookup"><span data-stu-id="84142-105">The list all managed applications parameter set.</span></span> <span data-ttu-id="84142-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="84142-106">(Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84142-107">A felügyelt alkalmazásnév paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="84142-107">The managed application name parameter set.</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84142-108">A felügyelt alkalmazásspecifikus azonosító paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="84142-108">The managed application Id parameter set.</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84142-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="84142-109">DESCRIPTION</span></span>
<span data-ttu-id="84142-110">A **Get-AzureRmManagedApplication** parancsmag felügyelt alkalmazásokat kap</span><span class="sxs-lookup"><span data-stu-id="84142-110">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="84142-111">Példák</span><span class="sxs-lookup"><span data-stu-id="84142-111">EXAMPLES</span></span>

### <span data-ttu-id="84142-112">Példa 1: az összes felügyelt alkalmazás beolvasása egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="84142-112">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="84142-113">A parancs a kezelt alkalmazásokat a "MyRG" erőforráscsoport alatt kapja.</span><span class="sxs-lookup"><span data-stu-id="84142-113">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="84142-114">2. példa: az összes felügyelt alkalmazás beolvasása</span><span class="sxs-lookup"><span data-stu-id="84142-114">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="84142-115">Ez a parancs beolvassa az összes felügyelt alkalmazást az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="84142-115">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="84142-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84142-116">PARAMETERS</span></span>

### <span data-ttu-id="84142-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="84142-117">-ApiVersion</span></span>
<span data-ttu-id="84142-118">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="84142-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="84142-119">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="84142-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="84142-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84142-120">-DefaultProfile</span></span>
<span data-ttu-id="84142-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84142-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84142-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="84142-122">-Id</span></span>
<span data-ttu-id="84142-123">A teljes mértékben minősített felügyelt alkalmazásspecifikus azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="84142-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="84142-124">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="84142-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84142-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="84142-125">-Name</span></span>
<span data-ttu-id="84142-126">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="84142-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84142-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="84142-127">-Pre</span></span>
<span data-ttu-id="84142-128">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="84142-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="84142-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84142-129">-ResourceGroupName</span></span>
<span data-ttu-id="84142-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="84142-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84142-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84142-131">CommonParameters</span></span>
<span data-ttu-id="84142-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84142-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84142-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84142-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84142-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84142-134">INPUTS</span></span>

### <span data-ttu-id="84142-135">System. String</span><span class="sxs-lookup"><span data-stu-id="84142-135">System.String</span></span>

## <span data-ttu-id="84142-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84142-136">OUTPUTS</span></span>

### <span data-ttu-id="84142-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="84142-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="84142-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84142-138">NOTES</span></span>

## <span data-ttu-id="84142-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84142-139">RELATED LINKS</span></span>

