---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 18f492147e897b8061795434c309cc63729bec5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494470"
---
# <span data-ttu-id="f556c-101">Get-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f556c-101">Get-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="f556c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f556c-102">SYNOPSIS</span></span>
<span data-ttu-id="f556c-103">Megkapja a fiókot.</span><span class="sxs-lookup"><span data-stu-id="f556c-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f556c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f556c-104">SYNTAX</span></span>

### <span data-ttu-id="f556c-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f556c-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccount [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f556c-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f556c-106">AccountNameParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f556c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f556c-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f556c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f556c-108">DESCRIPTION</span></span>
<span data-ttu-id="f556c-109">A **Get-AzureRmLocationBasedServicesAccount** parancsmag egy kiépített helyeken nyugvó Services-fiókkal rendelkezik, amelyet az erőforráscsoport, a név vagy az erőforrás-azonosító alapján kap.</span><span class="sxs-lookup"><span data-stu-id="f556c-109">The **Get-AzureRmLocationBasedServicesAccount** cmdlet gets a provisioned Location Based Services account, either by resource group and name, or by resource id.</span></span>

<span data-ttu-id="f556c-110">Ezenkívül visszaállíthatja az összes fiók listáját a ResourceGroup, illetve az aktuális előfizetéshez tartozó összes hely-és szolgáltatási fiókot is.</span><span class="sxs-lookup"><span data-stu-id="f556c-110">Additionally, it can return a list of all accounts in the ResourceGroup, or all Location Based Services accounts for the current subscription.</span></span>

## <span data-ttu-id="f556c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f556c-111">EXAMPLES</span></span>

### <span data-ttu-id="f556c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f556c-112">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="f556c-113">Ha létezik, az erőforráscsoport MyResourceGroup a MyAccount nevű fiókot kapja.</span><span class="sxs-lookup"><span data-stu-id="f556c-113">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="f556c-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="f556c-114">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="f556c-115">Az erőforráscsoport MyResourceGroup minden hely-alapú szolgáltatási fiókot kap.</span><span class="sxs-lookup"><span data-stu-id="f556c-115">Gets all Location Based Services accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="f556c-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="f556c-116">Example 3</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="f556c-117">A jelenlegi előfizetésben minden hely-alapú szolgáltatási fiók beolvasása</span><span class="sxs-lookup"><span data-stu-id="f556c-117">Gets all Location Based Services accounts in the current subscription.</span></span>

### <span data-ttu-id="f556c-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="f556c-118">Example 4</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="f556c-119">Megkapja az erőforrás-azonosító által megadott hely-alapú szolgáltatások fiókját.</span><span class="sxs-lookup"><span data-stu-id="f556c-119">Gets the Location Based Services account specified by the Resource Id.</span></span>

## <span data-ttu-id="f556c-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f556c-120">PARAMETERS</span></span>

### <span data-ttu-id="f556c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f556c-121">-DefaultProfile</span></span>
<span data-ttu-id="f556c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f556c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f556c-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f556c-123">-Name</span></span>
<span data-ttu-id="f556c-124">A helyeken nyugvó szolgáltatások fiókjának neve.</span><span class="sxs-lookup"><span data-stu-id="f556c-124">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f556c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f556c-125">-ResourceGroupName</span></span>
<span data-ttu-id="f556c-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f556c-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f556c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f556c-127">-ResourceId</span></span>
<span data-ttu-id="f556c-128">A helyeken nyugvó Services-fiók ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f556c-128">Location Based Services Account ResourceId.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f556c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f556c-129">CommonParameters</span></span>
<span data-ttu-id="f556c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f556c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f556c-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f556c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f556c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f556c-132">INPUTS</span></span>

### <span data-ttu-id="f556c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f556c-133">System.String</span></span>

## <span data-ttu-id="f556c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f556c-134">OUTPUTS</span></span>

### <span data-ttu-id="f556c-135">Microsoft. Azure. Command. LocationBasedServices. models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f556c-135">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>
<span data-ttu-id="f556c-136">Ez a parancsmag egy **PSLocationBasedServicesAccount** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="f556c-136">This cmdlet returns a **PSLocationBasedServicesAccount** object.</span></span>
<span data-ttu-id="f556c-137">Módosíthatja ezt az objektumot, és a **set-AzureRmLocationBasedServices** használatával alkalmazhatja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="f556c-137">You can modify this object, and then apply changes by using **Set-AzureRmLocationBasedServices**.</span></span>

## <span data-ttu-id="f556c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f556c-138">NOTES</span></span>

## <span data-ttu-id="f556c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f556c-139">RELATED LINKS</span></span>
