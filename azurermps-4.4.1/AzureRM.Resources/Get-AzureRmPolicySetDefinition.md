---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 5fba45e50076952a0a2e11e2e5541ab9546d3bc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500772"
---
# <span data-ttu-id="2edc9-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="2edc9-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="2edc9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2edc9-102">SYNOPSIS</span></span>
<span data-ttu-id="2edc9-103">Kapja meg a házirend-definíciókat.</span><span class="sxs-lookup"><span data-stu-id="2edc9-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2edc9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2edc9-104">SYNTAX</span></span>

### <span data-ttu-id="2edc9-105">Az összes házirend-készlet definíciós paraméterének beállítása.</span><span class="sxs-lookup"><span data-stu-id="2edc9-105">The list all policy set definitions parameter set.</span></span> <span data-ttu-id="2edc9-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="2edc9-106">(Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2edc9-107">A Policy set definition Name paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="2edc9-107">The policy set definition name parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2edc9-108">A házirend-definíciós azonosító paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="2edc9-108">The policy set definition Id parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2edc9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2edc9-109">DESCRIPTION</span></span>
<span data-ttu-id="2edc9-110">A **Get-AzureRmPolicySetDefinition** parancsmag az összes házirend-készlet definícióját, illetve egy bizonyos, név vagy azonosító által meghatározott házirend-definíciót tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2edc9-110">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="2edc9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2edc9-111">EXAMPLES</span></span>

### <span data-ttu-id="2edc9-112">Példa 1: az összes házirend-készlet definíciójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="2edc9-112">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="2edc9-113">Ez a parancs beilleszti az összes házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="2edc9-113">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="2edc9-114">2. példa: a házirend-definíció beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="2edc9-114">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="2edc9-115">Ez a parancs a VMPolicyDefinition nevű házirend-definíciós definíciót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2edc9-115">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="2edc9-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2edc9-116">PARAMETERS</span></span>

### <span data-ttu-id="2edc9-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2edc9-117">-ApiVersion</span></span>
<span data-ttu-id="2edc9-118">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2edc9-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2edc9-119">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2edc9-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2edc9-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="2edc9-120">-Id</span></span>
<span data-ttu-id="2edc9-121">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetést is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="2edc9-121">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="2edc9-122">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="2edc9-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2edc9-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2edc9-123">-Name</span></span>
<span data-ttu-id="2edc9-124">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="2edc9-124">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2edc9-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="2edc9-125">-Pre</span></span>
<span data-ttu-id="2edc9-126">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2edc9-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2edc9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2edc9-127">-DefaultProfile</span></span>
<span data-ttu-id="2edc9-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2edc9-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2edc9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2edc9-129">CommonParameters</span></span>
<span data-ttu-id="2edc9-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2edc9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2edc9-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2edc9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2edc9-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2edc9-132">INPUTS</span></span>

### <span data-ttu-id="2edc9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2edc9-133">System.String</span></span>

## <span data-ttu-id="2edc9-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2edc9-134">OUTPUTS</span></span>

### <span data-ttu-id="2edc9-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2edc9-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2edc9-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2edc9-136">NOTES</span></span>

## <span data-ttu-id="2edc9-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2edc9-137">RELATED LINKS</span></span>

