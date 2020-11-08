---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194767"
---
# <span data-ttu-id="d11a5-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="d11a5-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="d11a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d11a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d11a5-103">Szabályok motor-konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d11a5-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="d11a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d11a5-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d11a5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d11a5-105">DESCRIPTION</span></span>
<span data-ttu-id="d11a5-106">A **Get-AzFrontDoorRulesEngine** parancsmag bizonyos szabályok motorjának konfigurációját adja meg, vagy beilleszti a szabályok motor-konfigurációját egy bejárati ajtóhoz.</span><span class="sxs-lookup"><span data-stu-id="d11a5-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="d11a5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d11a5-107">EXAMPLES</span></span>

### <span data-ttu-id="d11a5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d11a5-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="d11a5-109">Meghatározott szabályok beszerzése Engine Configuration.</span><span class="sxs-lookup"><span data-stu-id="d11a5-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="d11a5-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="d11a5-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="d11a5-111">Beolvassa a szabályok motor-konfigurációját egy bejárati ajtóban.</span><span class="sxs-lookup"><span data-stu-id="d11a5-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="d11a5-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="d11a5-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="d11a5-113">A nem létező szabályok motorjának beszerzése várható eredmény.</span><span class="sxs-lookup"><span data-stu-id="d11a5-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="d11a5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d11a5-114">PARAMETERS</span></span>

### <span data-ttu-id="d11a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11a5-115">-DefaultProfile</span></span>
<span data-ttu-id="d11a5-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d11a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d11a5-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="d11a5-117">-FrontDoorName</span></span>
<span data-ttu-id="d11a5-118">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="d11a5-118">Front Door name.</span></span>

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

### <span data-ttu-id="d11a5-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d11a5-119">-Name</span></span>
<span data-ttu-id="d11a5-120">A szabályok motorjának neve</span><span class="sxs-lookup"><span data-stu-id="d11a5-120">Rules engine name.</span></span>

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

### <span data-ttu-id="d11a5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d11a5-121">-ResourceGroupName</span></span>
<span data-ttu-id="d11a5-122">Az erőforráscsoport neve, amelybe az első ajtó jön létre.</span><span class="sxs-lookup"><span data-stu-id="d11a5-122">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="d11a5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11a5-123">CommonParameters</span></span>
<span data-ttu-id="d11a5-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d11a5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11a5-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d11a5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11a5-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d11a5-126">INPUTS</span></span>

### <span data-ttu-id="d11a5-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="d11a5-127">None</span></span>

## <span data-ttu-id="d11a5-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d11a5-128">OUTPUTS</span></span>

### <span data-ttu-id="d11a5-129">Microsoft. Azure. Command. FrontDoor. models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="d11a5-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="d11a5-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d11a5-130">NOTES</span></span>

## <span data-ttu-id="d11a5-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d11a5-131">RELATED LINKS</span></span>
