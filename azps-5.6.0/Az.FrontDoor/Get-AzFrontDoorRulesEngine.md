---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 62ef80d7af7ce9b9a10a7a18b38fbf5c6f1db562
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940450"
---
# <span data-ttu-id="e96f3-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="e96f3-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="e96f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e96f3-102">SYNOPSIS</span></span>
<span data-ttu-id="e96f3-103">A Szabálymotor beállításainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="e96f3-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="e96f3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e96f3-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e96f3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e96f3-105">DESCRIPTION</span></span>
<span data-ttu-id="e96f3-106">A **Get-AzFrontDoorRulesEngine** parancsmag egy adott szabálymotor-konfigurációt kap, vagy a bevezető ajtóhoz társított összes szabálymotor-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="e96f3-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="e96f3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e96f3-107">EXAMPLES</span></span>

### <span data-ttu-id="e96f3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e96f3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="e96f3-109">Konkrét szabálymotor-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="e96f3-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="e96f3-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="e96f3-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="e96f3-111">Minden szabálymotor-konfigurációt be tud szerezni egy előtérbe.</span><span class="sxs-lookup"><span data-stu-id="e96f3-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="e96f3-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="e96f3-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="e96f3-113">Várt kimenet nem létező szabálymotor leküldkor.</span><span class="sxs-lookup"><span data-stu-id="e96f3-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="e96f3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e96f3-114">PARAMETERS</span></span>

### <span data-ttu-id="e96f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e96f3-115">-DefaultProfile</span></span>
<span data-ttu-id="e96f3-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e96f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e96f3-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="e96f3-117">-FrontDoorName</span></span>
<span data-ttu-id="e96f3-118">Front Door name.</span><span class="sxs-lookup"><span data-stu-id="e96f3-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96f3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e96f3-119">-Name</span></span>
<span data-ttu-id="e96f3-120">A szabálymotor neve.</span><span class="sxs-lookup"><span data-stu-id="e96f3-120">Rules engine name.</span></span>

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

### <span data-ttu-id="e96f3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e96f3-121">-ResourceGroupName</span></span>
<span data-ttu-id="e96f3-122">Az erőforráscsoport neve, amelyből a front door lesz létrehozva.</span><span class="sxs-lookup"><span data-stu-id="e96f3-122">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96f3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e96f3-123">CommonParameters</span></span>
<span data-ttu-id="e96f3-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e96f3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e96f3-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e96f3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e96f3-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e96f3-126">INPUTS</span></span>

### <span data-ttu-id="e96f3-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="e96f3-127">None</span></span>

## <span data-ttu-id="e96f3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e96f3-128">OUTPUTS</span></span>

### <span data-ttu-id="e96f3-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="e96f3-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="e96f3-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e96f3-130">NOTES</span></span>

## <span data-ttu-id="e96f3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e96f3-131">RELATED LINKS</span></span>
