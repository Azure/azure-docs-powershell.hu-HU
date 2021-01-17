---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469813"
---
# <span data-ttu-id="5e17a-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="5e17a-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="5e17a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e17a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e17a-103">A Szabálymotor beállításainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="5e17a-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="5e17a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e17a-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e17a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e17a-105">DESCRIPTION</span></span>
<span data-ttu-id="5e17a-106">A **Get-AzFrontDoorRulesEngine** parancsmag egy adott szabálymotor-konfigurációt kap, vagy a bevezető ajtóhoz társított összes szabálymotor-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="5e17a-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="5e17a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e17a-107">EXAMPLES</span></span>

### <span data-ttu-id="5e17a-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="5e17a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="5e17a-109">Konkrét szabálymotor-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="5e17a-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="5e17a-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="5e17a-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="5e17a-111">Minden szabálymotor-konfigurációt be tud szerezni egy előtérbe.</span><span class="sxs-lookup"><span data-stu-id="5e17a-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="5e17a-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="5e17a-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="5e17a-113">Várt kimenet nem létező szabálymotor leküldkor.</span><span class="sxs-lookup"><span data-stu-id="5e17a-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="5e17a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e17a-114">PARAMETERS</span></span>

### <span data-ttu-id="5e17a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e17a-115">-DefaultProfile</span></span>
<span data-ttu-id="5e17a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e17a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e17a-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="5e17a-117">-FrontDoorName</span></span>
<span data-ttu-id="5e17a-118">Front Door name.</span><span class="sxs-lookup"><span data-stu-id="5e17a-118">Front Door name.</span></span>

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

### <span data-ttu-id="5e17a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5e17a-119">-Name</span></span>
<span data-ttu-id="5e17a-120">A szabálymotor neve.</span><span class="sxs-lookup"><span data-stu-id="5e17a-120">Rules engine name.</span></span>

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

### <span data-ttu-id="5e17a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e17a-121">-ResourceGroupName</span></span>
<span data-ttu-id="5e17a-122">Az erőforráscsoport neve, amelybe a front door nevet fogja létrehozni.</span><span class="sxs-lookup"><span data-stu-id="5e17a-122">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="5e17a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e17a-123">CommonParameters</span></span>
<span data-ttu-id="5e17a-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e17a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e17a-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e17a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e17a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e17a-126">INPUTS</span></span>

### <span data-ttu-id="5e17a-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="5e17a-127">None</span></span>

## <span data-ttu-id="5e17a-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e17a-128">OUTPUTS</span></span>

### <span data-ttu-id="5e17a-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="5e17a-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="5e17a-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e17a-130">NOTES</span></span>

## <span data-ttu-id="5e17a-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e17a-131">RELATED LINKS</span></span>
