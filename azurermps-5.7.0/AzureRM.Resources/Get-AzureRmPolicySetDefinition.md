---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 694f2ef459b50648e934e4ea0e434fe218d4b1f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501412"
---
# <span data-ttu-id="f96a7-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f96a7-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="f96a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f96a7-102">SYNOPSIS</span></span>
<span data-ttu-id="f96a7-103">Kapja meg a házirend-definíciókat.</span><span class="sxs-lookup"><span data-stu-id="f96a7-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f96a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f96a7-104">SYNTAX</span></span>

### <span data-ttu-id="f96a7-105">GetBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f96a7-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f96a7-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f96a7-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f96a7-107">GetById</span><span class="sxs-lookup"><span data-stu-id="f96a7-107">GetById</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f96a7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f96a7-108">DESCRIPTION</span></span>
<span data-ttu-id="f96a7-109">A **Get-AzureRmPolicySetDefinition** parancsmag az összes házirend-készlet definícióját, illetve egy bizonyos, név vagy azonosító által meghatározott házirend-definíciót tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="f96a7-109">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="f96a7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f96a7-110">EXAMPLES</span></span>

### <span data-ttu-id="f96a7-111">Példa 1: az összes házirend-készlet definíciójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="f96a7-111">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="f96a7-112">Ez a parancs beilleszti az összes házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="f96a7-112">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="f96a7-113">2. példa: a házirend-definíció beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="f96a7-113">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="f96a7-114">Ez a parancs a VMPolicyDefinition nevű házirend-definíciós definíciót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f96a7-114">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="f96a7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f96a7-115">PARAMETERS</span></span>

### <span data-ttu-id="f96a7-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f96a7-116">-ApiVersion</span></span>
<span data-ttu-id="f96a7-117">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f96a7-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f96a7-118">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f96a7-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f96a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f96a7-119">-DefaultProfile</span></span>
<span data-ttu-id="f96a7-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f96a7-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f96a7-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f96a7-121">-Id</span></span>
<span data-ttu-id="f96a7-122">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetést is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="f96a7-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="f96a7-123">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="f96a7-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f96a7-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f96a7-124">-Name</span></span>
<span data-ttu-id="f96a7-125">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="f96a7-125">The policy set definition name.</span></span>

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

### <span data-ttu-id="f96a7-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="f96a7-126">-Pre</span></span>
<span data-ttu-id="f96a7-127">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f96a7-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f96a7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f96a7-128">CommonParameters</span></span>
<span data-ttu-id="f96a7-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f96a7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f96a7-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f96a7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f96a7-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f96a7-131">INPUTS</span></span>

### <span data-ttu-id="f96a7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f96a7-132">System.String</span></span>

## <span data-ttu-id="f96a7-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f96a7-133">OUTPUTS</span></span>

### <span data-ttu-id="f96a7-134">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f96a7-134">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f96a7-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f96a7-135">NOTES</span></span>

## <span data-ttu-id="f96a7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f96a7-136">RELATED LINKS</span></span>
