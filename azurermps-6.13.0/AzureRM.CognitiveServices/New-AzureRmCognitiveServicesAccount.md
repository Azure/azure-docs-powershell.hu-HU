---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41defe467244647f707bae16c653dfcbe99eaec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495161"
---
# <span data-ttu-id="76dd4-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76dd4-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="76dd4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76dd4-102">SYNOPSIS</span></span>
<span data-ttu-id="76dd4-103">Kognitív szolgáltatások fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="76dd4-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76dd4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76dd4-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76dd4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="76dd4-105">DESCRIPTION</span></span>
<span data-ttu-id="76dd4-106">A **New-AzureRmCognitiveServicesAccount** parancsmag a megadott típusú és SKU-hoz létrehoz egy kognitív szolgáltatásokat tartalmazó fiókot.</span><span class="sxs-lookup"><span data-stu-id="76dd4-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="76dd4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="76dd4-107">EXAMPLES</span></span>

### <span data-ttu-id="76dd4-108">1:</span><span class="sxs-lookup"><span data-stu-id="76dd4-108">1:</span></span>
```
PS C:\> New-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="76dd4-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76dd4-109">PARAMETERS</span></span>

### <span data-ttu-id="76dd4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76dd4-110">-DefaultProfile</span></span>
<span data-ttu-id="76dd4-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="76dd4-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dd4-112">-Force</span><span class="sxs-lookup"><span data-stu-id="76dd4-112">-Force</span></span>
<span data-ttu-id="76dd4-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="76dd4-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dd4-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="76dd4-114">-Location</span></span>
<span data-ttu-id="76dd4-115">Azt a helyet adja meg, ahol létre szeretné hozni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="76dd4-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76dd4-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76dd4-116">-Name</span></span>
<span data-ttu-id="76dd4-117">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76dd4-117">Specifies the name for the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76dd4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76dd4-118">-ResourceGroupName</span></span>
<span data-ttu-id="76dd4-119">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez hozzá szeretné rendelni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="76dd4-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="76dd4-120">Az erőforráscsoportnek már léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="76dd4-120">The resource group must already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76dd4-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="76dd4-121">-SkuName</span></span>
<span data-ttu-id="76dd4-122">A fiókhoz tartozó SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="76dd4-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="76dd4-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="76dd4-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="76dd4-124">F0 (ingyenes Tier)</span><span class="sxs-lookup"><span data-stu-id="76dd4-124">F0 (free tier)</span></span>
- <span data-ttu-id="76dd4-125">S0</span><span class="sxs-lookup"><span data-stu-id="76dd4-125">S0</span></span>
- <span data-ttu-id="76dd4-126">S1</span><span class="sxs-lookup"><span data-stu-id="76dd4-126">S1</span></span>
- <span data-ttu-id="76dd4-127">S2</span><span class="sxs-lookup"><span data-stu-id="76dd4-127">S2</span></span>
- <span data-ttu-id="76dd4-128">S3</span><span class="sxs-lookup"><span data-stu-id="76dd4-128">S3</span></span>
- <span data-ttu-id="76dd4-129">S4 további tudnivalókért olvassa el a [kognitív szolgáltatás API](https://www.microsoft.com/cognitive-services/en-us/apis)-k című témakört.</span><span class="sxs-lookup"><span data-stu-id="76dd4-129">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76dd4-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="76dd4-130">-Tag</span></span>
<span data-ttu-id="76dd4-131">Egy címkét név/érték párokként ad meg.</span><span class="sxs-lookup"><span data-stu-id="76dd4-131">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dd4-132">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="76dd4-132">-Type</span></span>
<span data-ttu-id="76dd4-133">A létrehozandó fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="76dd4-133">Specifies the type of account to create.</span></span> <span data-ttu-id="76dd4-134">Használja `Get-AzureRmCognitiveServicesAccountType` a parancsmagot a jelenlegi elfogadható értékek beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="76dd4-134">Use `Get-AzureRmCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76dd4-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="76dd4-135">-Confirm</span></span>
<span data-ttu-id="76dd4-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="76dd4-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dd4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76dd4-137">-WhatIf</span></span>
<span data-ttu-id="76dd4-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="76dd4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76dd4-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="76dd4-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dd4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76dd4-140">CommonParameters</span></span>
<span data-ttu-id="76dd4-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76dd4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76dd4-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76dd4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76dd4-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76dd4-143">INPUTS</span></span>

### <span data-ttu-id="76dd4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="76dd4-144">System.String</span></span>

## <span data-ttu-id="76dd4-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76dd4-145">OUTPUTS</span></span>

### <span data-ttu-id="76dd4-146">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76dd4-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="76dd4-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76dd4-147">NOTES</span></span>

## <span data-ttu-id="76dd4-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76dd4-148">RELATED LINKS</span></span>

[<span data-ttu-id="76dd4-149">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76dd4-149">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="76dd4-150">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76dd4-150">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="76dd4-151">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76dd4-151">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
