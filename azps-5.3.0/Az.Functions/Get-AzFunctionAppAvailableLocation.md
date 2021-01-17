---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 3ab2ab4778b7fdb12334db416c953a7c373c63b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469745"
---
# <span data-ttu-id="3ffd0-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="3ffd0-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="3ffd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ffd0-102">SYNOPSIS</span></span>
<span data-ttu-id="3ffd0-103">Itt érhetők el az adott operációs rendszerhez és tervtípushoz használható függvényalkalmazások.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="3ffd0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3ffd0-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3ffd0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3ffd0-105">DESCRIPTION</span></span>
<span data-ttu-id="3ffd0-106">Itt érhetők el az adott operációs rendszerhez és tervtípushoz használható függvényalkalmazások.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="3ffd0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3ffd0-107">EXAMPLES</span></span>

### <span data-ttu-id="3ffd0-108">1. példa: Szerezze be, hogy hol érhető el a Prémium verzió a Windowshoz.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="3ffd0-109">Ha nincs megadva paraméter, a PlanType a "Premium" értéket, az OSType pedig a "Windows" értéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
West India
South India
Canada Central
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
Germany West Central
Norway East
```

<span data-ttu-id="3ffd0-110">Ezzel a paranccsal azok a helyek érhetők el, ahol a Prémium verzió elérhető a Windowshoz.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="3ffd0-111">2. példa: Szerezze be a linuxos prémium verziós helyeket.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Premium -OSType Linux

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
West India
Canada Central
West Central US
West US 2
UK West
UK South
Central US EUAP
Korea Central
France Central
Norway East
```

<span data-ttu-id="3ffd0-112">Ez a parancs beveszi azt a helyet, ahol a Linux prémium verzió elérhető.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="3ffd0-113">3. példa: Szerezze be a Helyek, ahol a Felhasználás elérhető a Windowshoz.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Consumption -OSType Windows

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
Central India
West India
South India
Canada Central
Canada East
West Central US
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
South Africa North
Switzerland North
Germany West Central
```

<span data-ttu-id="3ffd0-114">Ez a parancs beveszi azt a helyet, ahol a Felhasználás elérhető a Windowshoz.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="3ffd0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ffd0-115">PARAMETERS</span></span>

### <span data-ttu-id="3ffd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ffd0-116">-DefaultProfile</span></span>
<span data-ttu-id="3ffd0-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd0-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="3ffd0-118">-OSType</span></span>
<span data-ttu-id="3ffd0-119">A szolgáltatás csomag operációs rendszertípusa.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-119">The OS type for the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd0-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="3ffd0-120">-PlanType</span></span>
<span data-ttu-id="3ffd0-121">A terv típusa.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-121">The plan type.</span></span>
<span data-ttu-id="3ffd0-122">Érvényes bemenetek: Felhasználás vagy Prémium</span><span class="sxs-lookup"><span data-stu-id="3ffd0-122">Valid inputs: Consumption or Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd0-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ffd0-123">-SubscriptionId</span></span>
<span data-ttu-id="3ffd0-124">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-124">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ffd0-125">CommonParameters</span></span>
<span data-ttu-id="3ffd0-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ffd0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ffd0-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ffd0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ffd0-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ffd0-128">INPUTS</span></span>

## <span data-ttu-id="3ffd0-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ffd0-129">OUTPUTS</span></span>

### <span data-ttu-id="3ffd0-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="3ffd0-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="3ffd0-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3ffd0-131">NOTES</span></span>

<span data-ttu-id="3ffd0-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3ffd0-132">ALIASES</span></span>

## <span data-ttu-id="3ffd0-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ffd0-133">RELATED LINKS</span></span>

