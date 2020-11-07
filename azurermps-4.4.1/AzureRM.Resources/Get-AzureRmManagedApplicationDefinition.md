---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: ef724c4d2e9771243058471c3ce2aebc944d2bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672412"
---
# <span data-ttu-id="7e83f-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="7e83f-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="7e83f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e83f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e83f-103">Felügyelt alkalmazás-definíciók beolvasása</span><span class="sxs-lookup"><span data-stu-id="7e83f-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e83f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e83f-104">SYNTAX</span></span>

### <span data-ttu-id="7e83f-105">A Managed Application Definition Name paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="7e83f-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="7e83f-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="7e83f-106">(Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e83f-107">A felügyelt alkalmazás-definíciós azonosító paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="7e83f-107">The managed application definition Id parameter set.</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e83f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e83f-108">DESCRIPTION</span></span>
<span data-ttu-id="7e83f-109">A **Get-AzureRmManagedApplicationDefinition** parancsmag felügyelt alkalmazás-definíciókat kap</span><span class="sxs-lookup"><span data-stu-id="7e83f-109">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="7e83f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7e83f-110">EXAMPLES</span></span>

### <span data-ttu-id="7e83f-111">Példa 1: az összes felügyelt alkalmazás definíciójának beolvasása egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="7e83f-111">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="7e83f-112">Ez a parancs a felügyelt alkalmazások definícióját a "MyRG" erőforráscsoport csoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7e83f-112">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="7e83f-113">2. példa: felügyelt alkalmazás definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="7e83f-113">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="7e83f-114">Ez a parancs beolvassa a felügyelt alkalmazás definícióját "myManagedAppDef" az erőforráscsoport "MyRG" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="7e83f-114">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="7e83f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e83f-115">PARAMETERS</span></span>

### <span data-ttu-id="7e83f-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7e83f-116">-ApiVersion</span></span>
<span data-ttu-id="7e83f-117">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e83f-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7e83f-118">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="7e83f-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="7e83f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e83f-119">-DefaultProfile</span></span>
<span data-ttu-id="7e83f-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e83f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e83f-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="7e83f-121">-Id</span></span>
<span data-ttu-id="7e83f-122">A teljes mértékben minősített felügyelt alkalmazás-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="7e83f-122">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="7e83f-123">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="7e83f-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e83f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7e83f-124">-Name</span></span>
<span data-ttu-id="7e83f-125">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="7e83f-125">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e83f-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="7e83f-126">-Pre</span></span>
<span data-ttu-id="7e83f-127">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="7e83f-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7e83f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e83f-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e83f-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7e83f-129">The resource group name.</span></span>

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

### <span data-ttu-id="7e83f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e83f-130">CommonParameters</span></span>
<span data-ttu-id="7e83f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e83f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e83f-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e83f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e83f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e83f-133">INPUTS</span></span>

### <span data-ttu-id="7e83f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7e83f-134">System.String</span></span>

## <span data-ttu-id="7e83f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e83f-135">OUTPUTS</span></span>

### <span data-ttu-id="7e83f-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7e83f-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7e83f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e83f-137">NOTES</span></span>

## <span data-ttu-id="7e83f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e83f-138">RELATED LINKS</span></span>

