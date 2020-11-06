---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 1f528bb0a80f039b9a2be7cb4cb6e4c7fbc740c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504540"
---
# <span data-ttu-id="a2520-101">Get-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="a2520-101">Get-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="a2520-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2520-102">SYNOPSIS</span></span>
<span data-ttu-id="a2520-103">A fiók API-kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="a2520-103">Gets the API keys for an account.</span></span> <span data-ttu-id="a2520-104">Ezek a kulcsok az Azure Location based Services további hívásokban használt hitelesítési mechanizmusát jelentik.</span><span class="sxs-lookup"><span data-stu-id="a2520-104">These keys are the authentication mechanism used in subsequent calls to Azure Location Based Services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2520-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2520-105">SYNTAX</span></span>

### <span data-ttu-id="a2520-106">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2520-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2520-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2520-107">InputObjectParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2520-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2520-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2520-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2520-109">DESCRIPTION</span></span>
<span data-ttu-id="a2520-110">A **Get-AzureRmLocationBasedServicesAccountKey** parancsmag a kiépített helyekre épülő Services-fiók API kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a2520-110">The **Get-AzureRmLocationBasedServicesAccountKey** cmdlet gets the API keys for a provisioned Location Based Services account.</span></span>

<span data-ttu-id="a2520-111">A helyekre épülő szolgáltatási fiók két API-kulcsból áll: elsődleges és másodlagos.</span><span class="sxs-lookup"><span data-stu-id="a2520-111">A Location Based Services account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="a2520-112">A billentyűk lehetővé teszik az interakciót a hely-és szolgáltatási fiók végponttal.</span><span class="sxs-lookup"><span data-stu-id="a2520-112">The keys enable interaction with the Location Based Services account endpoint.</span></span>

<span data-ttu-id="a2520-113">A billentyűk újragenerálásához használja a [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) .</span><span class="sxs-lookup"><span data-stu-id="a2520-113">Use [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) to regenerate a key.</span></span>

## <span data-ttu-id="a2520-114">Példák</span><span class="sxs-lookup"><span data-stu-id="a2520-114">EXAMPLES</span></span>

### <span data-ttu-id="a2520-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a2520-115">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="a2520-116">A MyAccount nevű fiók kulcsait számítja ki az erőforráscsoport MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a2520-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="a2520-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="a2520-117">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="a2520-118">A megadott hely alapú szolgáltatások fiók kulcsait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a2520-118">Returns the keys for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="a2520-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2520-119">PARAMETERS</span></span>

### <span data-ttu-id="a2520-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2520-120">-DefaultProfile</span></span>
<span data-ttu-id="a2520-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2520-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2520-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2520-122">-InputObject</span></span>
<span data-ttu-id="a2520-123">A hely alapú szolgáltatások fiókja a [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="a2520-123">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

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

### <span data-ttu-id="a2520-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2520-124">-Name</span></span>
<span data-ttu-id="a2520-125">A helyeken nyugvó szolgáltatások fiókjának neve.</span><span class="sxs-lookup"><span data-stu-id="a2520-125">Location Based Services Account Name.</span></span>

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

### <span data-ttu-id="a2520-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2520-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2520-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a2520-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="a2520-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2520-128">-ResourceId</span></span>
<span data-ttu-id="a2520-129">A helyeken nyugvó Services-fiók ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a2520-129">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="a2520-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2520-130">CommonParameters</span></span>
<span data-ttu-id="a2520-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2520-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2520-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2520-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2520-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2520-133">INPUTS</span></span>

### <span data-ttu-id="a2520-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a2520-134">System.String</span></span>

## <span data-ttu-id="a2520-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2520-135">OUTPUTS</span></span>

### <span data-ttu-id="a2520-136">Microsoft. Azure. Command. LocationBasedServices. models. PSLocationBasedServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a2520-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccountKeys</span></span>

### <span data-ttu-id="a2520-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2520-137">CommonParameters</span></span>
<span data-ttu-id="a2520-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2520-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2520-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2520-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2520-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2520-140">NOTES</span></span>

## <span data-ttu-id="a2520-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2520-141">RELATED LINKS</span></span>
