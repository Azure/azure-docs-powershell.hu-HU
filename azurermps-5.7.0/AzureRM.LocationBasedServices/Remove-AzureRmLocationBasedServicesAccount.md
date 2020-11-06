---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/remove-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 0496fcdba082370654b3259f101987d1a78621fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500572"
---
# <span data-ttu-id="35822-101">Remove-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="35822-101">Remove-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="35822-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35822-102">SYNOPSIS</span></span>
<span data-ttu-id="35822-103">A helyeken nyugvó Services-fiók törlése</span><span class="sxs-lookup"><span data-stu-id="35822-103">Deletes a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35822-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35822-104">SYNTAX</span></span>

### <span data-ttu-id="35822-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="35822-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35822-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35822-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35822-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35822-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35822-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="35822-108">DESCRIPTION</span></span>
<span data-ttu-id="35822-109">A **Remove-AzureRmLocationBasedServicesAccount** parancsmag törli a megadott hely alapú Services-fiókot.</span><span class="sxs-lookup"><span data-stu-id="35822-109">The **Remove-AzureRmLocationBasedServicesAccount** cmdlet deletes the specified Location Based Services account.</span></span>

## <span data-ttu-id="35822-110">Példák</span><span class="sxs-lookup"><span data-stu-id="35822-110">EXAMPLES</span></span>

### <span data-ttu-id="35822-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="35822-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="35822-112">Törli a fiók MyAccount az erőforrás csoport MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="35822-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="35822-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="35822-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="35822-114">Törli a megadott helyeken nyugvó Services-fiókot.</span><span class="sxs-lookup"><span data-stu-id="35822-114">Deletes the specified Location Based Services Account.</span></span>

## <span data-ttu-id="35822-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35822-115">PARAMETERS</span></span>

### <span data-ttu-id="35822-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35822-116">-DefaultProfile</span></span>
<span data-ttu-id="35822-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35822-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35822-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35822-118">-InputObject</span></span>
<span data-ttu-id="35822-119">A hely alapú szolgáltatások fiókja a [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="35822-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35822-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="35822-120">-Name</span></span>
<span data-ttu-id="35822-121">A helyeken nyugvó szolgáltatások fiókjának neve.</span><span class="sxs-lookup"><span data-stu-id="35822-121">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35822-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35822-122">-ResourceGroupName</span></span>
<span data-ttu-id="35822-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="35822-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35822-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35822-124">-ResourceId</span></span>
<span data-ttu-id="35822-125">A helyeken nyugvó Services-fiók ResourceId.</span><span class="sxs-lookup"><span data-stu-id="35822-125">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="35822-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="35822-126">-Confirm</span></span>
<span data-ttu-id="35822-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="35822-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35822-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35822-128">-WhatIf</span></span>
<span data-ttu-id="35822-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="35822-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35822-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35822-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35822-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35822-131">CommonParameters</span></span>
<span data-ttu-id="35822-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35822-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35822-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35822-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35822-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35822-134">INPUTS</span></span>

### <span data-ttu-id="35822-135">System. String</span><span class="sxs-lookup"><span data-stu-id="35822-135">System.String</span></span>

## <span data-ttu-id="35822-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35822-136">OUTPUTS</span></span>

### <span data-ttu-id="35822-137">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="35822-137">System.Object</span></span>

## <span data-ttu-id="35822-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35822-138">NOTES</span></span>

## <span data-ttu-id="35822-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35822-139">RELATED LINKS</span></span>
