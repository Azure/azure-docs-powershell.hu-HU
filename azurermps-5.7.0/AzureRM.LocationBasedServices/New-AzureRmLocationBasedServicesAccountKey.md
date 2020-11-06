---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 7116cd4c5da2dd897af4e6540593a5e5458e4eda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495336"
---
# <span data-ttu-id="1ec56-101">New-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="1ec56-101">New-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="1ec56-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ec56-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec56-103">Visszahozza a fiók kulcsát.</span><span class="sxs-lookup"><span data-stu-id="1ec56-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ec56-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ec56-104">SYNTAX</span></span>

### <span data-ttu-id="1ec56-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ec56-105">NameParameterSet (Default)</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ec56-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ec56-106">InputObjectParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ec56-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ec56-107">ResourceIdParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ec56-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ec56-108">DESCRIPTION</span></span>
<span data-ttu-id="1ec56-109">A **New-AzureRmLocationBasedServicesAccountKey** parancsmag létrehoz egy API-kulcsot egy hely-alapú Services-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="1ec56-109">The **New-AzureRmLocationBasedServicesAccountKey** cmdlet regenerates an API key for a Location Based Services account.</span></span>

## <span data-ttu-id="1ec56-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1ec56-110">EXAMPLES</span></span>

### <span data-ttu-id="1ec56-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1ec56-111">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="1ec56-112">Újragenerálja az elsődleges API-kulcsot az erőforráscsoport MyResourceGroup tartozó MyAccount.</span><span class="sxs-lookup"><span data-stu-id="1ec56-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="1ec56-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="1ec56-113">Example 2</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="1ec56-114">A megadott hely alapú Services-fiók másodlagos API-kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="1ec56-114">Regenerates the Secondary API Key for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="1ec56-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ec56-115">PARAMETERS</span></span>

### <span data-ttu-id="1ec56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec56-116">-DefaultProfile</span></span>
<span data-ttu-id="1ec56-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ec56-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ec56-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ec56-118">-InputObject</span></span>
<span data-ttu-id="1ec56-119">A hely alapú szolgáltatások fiókja a [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="1ec56-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

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

### <span data-ttu-id="1ec56-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="1ec56-120">-KeyName</span></span>
<span data-ttu-id="1ec56-121">A helyeken nyugvó szolgáltatások fiók kulcsa.</span><span class="sxs-lookup"><span data-stu-id="1ec56-121">Location Based Services Account Key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec56-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ec56-122">-Name</span></span>
<span data-ttu-id="1ec56-123">A helyeken nyugvó szolgáltatások fiókjának neve.</span><span class="sxs-lookup"><span data-stu-id="1ec56-123">Location Based Services Account Name.</span></span>

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

### <span data-ttu-id="1ec56-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec56-124">-ResourceGroupName</span></span>
<span data-ttu-id="1ec56-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1ec56-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1ec56-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ec56-126">-ResourceId</span></span>
<span data-ttu-id="1ec56-127">A helyeken nyugvó Services-fiók ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1ec56-127">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="1ec56-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ec56-128">-Confirm</span></span>
<span data-ttu-id="1ec56-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ec56-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ec56-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ec56-130">-WhatIf</span></span>
<span data-ttu-id="1ec56-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ec56-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ec56-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ec56-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ec56-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec56-133">CommonParameters</span></span>
<span data-ttu-id="1ec56-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ec56-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec56-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ec56-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec56-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ec56-136">INPUTS</span></span>

### <span data-ttu-id="1ec56-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1ec56-137">System.String</span></span>
<span data-ttu-id="1ec56-138">Microsoft. Azure. Command. LocationBasedServices. NewAzureLocationBasedServicesAccountKeyCommand + KeyNameType</span><span class="sxs-lookup"><span data-stu-id="1ec56-138">Microsoft.Azure.Commands.LocationBasedServices.NewAzureLocationBasedServicesAccountKeyCommand+KeyNameType</span></span>

## <span data-ttu-id="1ec56-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ec56-139">OUTPUTS</span></span>

### <span data-ttu-id="1ec56-140">Microsoft. Azure. Management. LocationBasedServices. models. LocationBasedServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1ec56-140">Microsoft.Azure.Management.LocationBasedServices.Models.LocationBasedServicesAccountKeys</span></span>

## <span data-ttu-id="1ec56-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ec56-141">NOTES</span></span>

## <span data-ttu-id="1ec56-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ec56-142">RELATED LINKS</span></span>
