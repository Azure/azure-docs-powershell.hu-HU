---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 449b10f851dbd4e2f2e804bab0772543d512c0c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505236"
---
# <span data-ttu-id="d221b-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d221b-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="d221b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d221b-102">SYNOPSIS</span></span>
<span data-ttu-id="d221b-103">Kognitív szolgáltatások fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d221b-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d221b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d221b-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d221b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d221b-105">DESCRIPTION</span></span>
<span data-ttu-id="d221b-106">A **New-AzureRmCognitiveServicesAccount** parancsmag a megadott típusú és SKU-hoz létrehoz egy kognitív szolgáltatásokat tartalmazó fiókot.</span><span class="sxs-lookup"><span data-stu-id="d221b-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="d221b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d221b-107">EXAMPLES</span></span>

### <span data-ttu-id="d221b-108">1:</span><span class="sxs-lookup"><span data-stu-id="d221b-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="d221b-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d221b-109">PARAMETERS</span></span>

### <span data-ttu-id="d221b-110">-Force</span><span class="sxs-lookup"><span data-stu-id="d221b-110">-Force</span></span>
<span data-ttu-id="d221b-111">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d221b-111">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d221b-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="d221b-112">-Location</span></span>
<span data-ttu-id="d221b-113">Azt a helyet adja meg, ahol létre szeretné hozni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="d221b-113">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="d221b-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d221b-114">-Name</span></span>
<span data-ttu-id="d221b-115">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d221b-115">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="d221b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d221b-116">-ResourceGroupName</span></span>
<span data-ttu-id="d221b-117">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez hozzá szeretné rendelni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="d221b-117">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="d221b-118">Az erőforráscsoportnek már léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="d221b-118">The resource group must already exist.</span></span>

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

### <span data-ttu-id="d221b-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d221b-119">-SkuName</span></span>
<span data-ttu-id="d221b-120">A fiókhoz tartozó SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="d221b-120">Specifies the SKU for the account.</span></span>
<span data-ttu-id="d221b-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d221b-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d221b-122">F0 (ingyenes Tier)</span><span class="sxs-lookup"><span data-stu-id="d221b-122">F0 (free tier)</span></span>
- <span data-ttu-id="d221b-123">S0</span><span class="sxs-lookup"><span data-stu-id="d221b-123">S0</span></span>
- <span data-ttu-id="d221b-124">S1</span><span class="sxs-lookup"><span data-stu-id="d221b-124">S1</span></span>
- <span data-ttu-id="d221b-125">S2</span><span class="sxs-lookup"><span data-stu-id="d221b-125">S2</span></span>
- <span data-ttu-id="d221b-126">S3</span><span class="sxs-lookup"><span data-stu-id="d221b-126">S3</span></span>
- <span data-ttu-id="d221b-127">S4</span><span class="sxs-lookup"><span data-stu-id="d221b-127">S4</span></span>

<span data-ttu-id="d221b-128">További információt a [kognitív szolgáltatás API](https://www.microsoft.com/cognitive-services/en-us/apis)-k című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="d221b-128">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="d221b-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="d221b-129">-Tag</span></span>
<span data-ttu-id="d221b-130">Egy címkét név/érték párokként ad meg.</span><span class="sxs-lookup"><span data-stu-id="d221b-130">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="d221b-131">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="d221b-131">-Type</span></span>
<span data-ttu-id="d221b-132">A létrehozandó fiók típusát adja meg. A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d221b-132">Specifies the type of account to create.The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d221b-133">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="d221b-133">ComputerVision</span></span>
- <span data-ttu-id="d221b-134">Érzelem</span><span class="sxs-lookup"><span data-stu-id="d221b-134">Emotion</span></span>
- <span data-ttu-id="d221b-135">Arc</span><span class="sxs-lookup"><span data-stu-id="d221b-135">Face</span></span>
- <span data-ttu-id="d221b-136">LUIS</span><span class="sxs-lookup"><span data-stu-id="d221b-136">LUIS</span></span>
- <span data-ttu-id="d221b-137">Javaslatok</span><span class="sxs-lookup"><span data-stu-id="d221b-137">Recommendations</span></span>
- <span data-ttu-id="d221b-138">Beszéd</span><span class="sxs-lookup"><span data-stu-id="d221b-138">Speech</span></span>
- <span data-ttu-id="d221b-139">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="d221b-139">TextAnalytics</span></span>
- <span data-ttu-id="d221b-140">WebLM</span><span class="sxs-lookup"><span data-stu-id="d221b-140">WebLM</span></span>

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

### <span data-ttu-id="d221b-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d221b-141">-Confirm</span></span>
<span data-ttu-id="d221b-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d221b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d221b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d221b-143">-WhatIf</span></span>
<span data-ttu-id="d221b-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d221b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d221b-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d221b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d221b-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d221b-146">-DefaultProfile</span></span>
<span data-ttu-id="d221b-147">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d221b-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d221b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d221b-148">CommonParameters</span></span>
<span data-ttu-id="d221b-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d221b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d221b-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d221b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d221b-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d221b-151">INPUTS</span></span>

## <span data-ttu-id="d221b-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d221b-152">OUTPUTS</span></span>

### <span data-ttu-id="d221b-153">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d221b-153">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="d221b-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d221b-154">NOTES</span></span>

## <span data-ttu-id="d221b-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d221b-155">RELATED LINKS</span></span>

[<span data-ttu-id="d221b-156">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d221b-156">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="d221b-157">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d221b-157">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="d221b-158">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d221b-158">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
