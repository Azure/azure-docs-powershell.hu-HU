---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 3ab2ab4778b7fdb12334db416c953a7c373c63b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185430"
---
# <span data-ttu-id="434b1-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="434b1-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="434b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="434b1-102">SYNOPSIS</span></span>
<span data-ttu-id="434b1-103">Megkapja azt a helyet, ahol az adott operációs rendszerhez tartozó és a csomag típusa függvény alkalmazás elérhető.</span><span class="sxs-lookup"><span data-stu-id="434b1-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="434b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="434b1-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="434b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="434b1-105">DESCRIPTION</span></span>
<span data-ttu-id="434b1-106">Megkapja azt a helyet, ahol az adott operációs rendszerhez tartozó és a csomag típusa függvény alkalmazás elérhető.</span><span class="sxs-lookup"><span data-stu-id="434b1-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="434b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="434b1-107">EXAMPLES</span></span>

### <span data-ttu-id="434b1-108">Példa 1: a Windowshoz elérhető prémium helyek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="434b1-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="434b1-109">Ha nincs megadva paraméter, akkor a PlanType a "Prémium" és a OSType "Windows" értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="434b1-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
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

<span data-ttu-id="434b1-110">Ez a parancs azokat a helyeket kapja meg, ahol a prémium verzió elérhető a Windowsban.</span><span class="sxs-lookup"><span data-stu-id="434b1-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="434b1-111">2. példa: a prémium verzióhoz elérhető helyek beszerzése a Linuxban.</span><span class="sxs-lookup"><span data-stu-id="434b1-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
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

<span data-ttu-id="434b1-112">Ez a parancs azokat a helyeket kapja meg, ahol a prémium verzió Linuxra elérhető.</span><span class="sxs-lookup"><span data-stu-id="434b1-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="434b1-113">3. példa: a Windowshoz elérhető felhasználás helyének beszerzése.</span><span class="sxs-lookup"><span data-stu-id="434b1-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
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

<span data-ttu-id="434b1-114">Ez a parancs azokat a helyeket adja meg, ahol a Windows a felhasználás elérhető.</span><span class="sxs-lookup"><span data-stu-id="434b1-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="434b1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="434b1-115">PARAMETERS</span></span>

### <span data-ttu-id="434b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434b1-116">-DefaultProfile</span></span>
<span data-ttu-id="434b1-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="434b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="434b1-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="434b1-118">-OSType</span></span>
<span data-ttu-id="434b1-119">A szolgáltatási terv operációs rendszer típusa.</span><span class="sxs-lookup"><span data-stu-id="434b1-119">The OS type for the service plan.</span></span>

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

### <span data-ttu-id="434b1-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="434b1-120">-PlanType</span></span>
<span data-ttu-id="434b1-121">A terv típusa.</span><span class="sxs-lookup"><span data-stu-id="434b1-121">The plan type.</span></span>
<span data-ttu-id="434b1-122">Érvényes bemenetek: fogyasztás vagy prémium</span><span class="sxs-lookup"><span data-stu-id="434b1-122">Valid inputs: Consumption or Premium</span></span>

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

### <span data-ttu-id="434b1-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="434b1-123">-SubscriptionId</span></span>
<span data-ttu-id="434b1-124">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="434b1-124">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="434b1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434b1-125">CommonParameters</span></span>
<span data-ttu-id="434b1-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="434b1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434b1-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="434b1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434b1-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="434b1-128">INPUTS</span></span>

## <span data-ttu-id="434b1-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="434b1-129">OUTPUTS</span></span>

### <span data-ttu-id="434b1-130">Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="434b1-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="434b1-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="434b1-131">NOTES</span></span>

<span data-ttu-id="434b1-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="434b1-132">ALIASES</span></span>

## <span data-ttu-id="434b1-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="434b1-133">RELATED LINKS</span></span>

