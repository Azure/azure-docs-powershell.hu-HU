---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: 7ea94e2e7e4c3e54d67beef367dffee001e94652
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835221"
---
# <span data-ttu-id="c4561-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c4561-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="c4561-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4561-102">SYNOPSIS</span></span>
<span data-ttu-id="c4561-103">Megkapja a fiókot.</span><span class="sxs-lookup"><span data-stu-id="c4561-103">Gets the account.</span></span>

## <span data-ttu-id="c4561-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4561-104">SYNTAX</span></span>

### <span data-ttu-id="c4561-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4561-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4561-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4561-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4561-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4561-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4561-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4561-108">DESCRIPTION</span></span>
<span data-ttu-id="c4561-109">A Get-AzMapsAccount parancsmag létrehoz egy kiépített Azure Maps-fiókot az erőforráscsoport, név vagy erőforrás-azonosító alapján. Emellett a ResourceGroup minden fiókját, illetve az összes Azure Maps-fiókot is visszaállíthatja az aktuális előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="c4561-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="c4561-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c4561-110">EXAMPLES</span></span>

### <span data-ttu-id="c4561-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c4561-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="c4561-112">Ha létezik, az erőforráscsoport MyResourceGroup a MyAccount nevű fiókot kapja.</span><span class="sxs-lookup"><span data-stu-id="c4561-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="c4561-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c4561-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="c4561-114">Az összes Azure Maps-fiók beolvasása az erőforráscsoport MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c4561-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="c4561-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="c4561-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="c4561-116">Az összes Azure Maps-fiók beolvasása az aktuális előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="c4561-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="c4561-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="c4561-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="c4561-118">Megkapja az erőforrás-azonosító által megadott térképek-fiókot.</span><span class="sxs-lookup"><span data-stu-id="c4561-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="c4561-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4561-119">PARAMETERS</span></span>

### <span data-ttu-id="c4561-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4561-120">-DefaultProfile</span></span>
<span data-ttu-id="c4561-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4561-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4561-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4561-122">-Name</span></span>
<span data-ttu-id="c4561-123">A fiók nevének megfeleltetése</span><span class="sxs-lookup"><span data-stu-id="c4561-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4561-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4561-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4561-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c4561-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4561-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4561-126">-ResourceId</span></span>
<span data-ttu-id="c4561-127">Térképek fiók ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c4561-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4561-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4561-128">CommonParameters</span></span>
<span data-ttu-id="c4561-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4561-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4561-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4561-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4561-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4561-131">INPUTS</span></span>

### <span data-ttu-id="c4561-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c4561-132">System.String</span></span>

## <span data-ttu-id="c4561-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4561-133">OUTPUTS</span></span>

### <span data-ttu-id="c4561-134">Microsoft. Azure. commands. maps. models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c4561-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="c4561-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4561-135">NOTES</span></span>

## <span data-ttu-id="c4561-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4561-136">RELATED LINKS</span></span>
