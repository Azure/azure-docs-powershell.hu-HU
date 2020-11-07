---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 1c1d4ad776ed3db2cb3b5adfb490902a7de12f42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672168"
---
# <span data-ttu-id="7391a-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7391a-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="7391a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7391a-102">SYNOPSIS</span></span>
<span data-ttu-id="7391a-103">Kognitív szolgáltatások fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7391a-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7391a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7391a-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7391a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7391a-105">DESCRIPTION</span></span>
<span data-ttu-id="7391a-106">A **New-AzureRmCognitiveServicesAccount** parancsmag a megadott típusú és SKU-hoz létrehoz egy kognitív szolgáltatásokat tartalmazó fiókot.</span><span class="sxs-lookup"><span data-stu-id="7391a-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="7391a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7391a-107">EXAMPLES</span></span>

### <span data-ttu-id="7391a-108">1:</span><span class="sxs-lookup"><span data-stu-id="7391a-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="7391a-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7391a-109">PARAMETERS</span></span>

### <span data-ttu-id="7391a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7391a-110">-DefaultProfile</span></span>
<span data-ttu-id="7391a-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7391a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7391a-112">-Force</span><span class="sxs-lookup"><span data-stu-id="7391a-112">-Force</span></span>
<span data-ttu-id="7391a-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7391a-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7391a-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="7391a-114">-Location</span></span>
<span data-ttu-id="7391a-115">Azt a helyet adja meg, ahol létre szeretné hozni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="7391a-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7391a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7391a-116">-Name</span></span>
<span data-ttu-id="7391a-117">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7391a-117">Specifies the name for the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7391a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7391a-118">-ResourceGroupName</span></span>
<span data-ttu-id="7391a-119">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez hozzá szeretné rendelni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="7391a-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="7391a-120">Az erőforráscsoportnek már léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="7391a-120">The resource group must already exist.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7391a-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7391a-121">-SkuName</span></span>
<span data-ttu-id="7391a-122">A fiókhoz tartozó SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="7391a-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="7391a-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7391a-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7391a-124">F0 (ingyenes Tier)</span><span class="sxs-lookup"><span data-stu-id="7391a-124">F0 (free tier)</span></span>
- <span data-ttu-id="7391a-125">S0</span><span class="sxs-lookup"><span data-stu-id="7391a-125">S0</span></span>
- <span data-ttu-id="7391a-126">S1</span><span class="sxs-lookup"><span data-stu-id="7391a-126">S1</span></span>
- <span data-ttu-id="7391a-127">S2</span><span class="sxs-lookup"><span data-stu-id="7391a-127">S2</span></span>
- <span data-ttu-id="7391a-128">S3</span><span class="sxs-lookup"><span data-stu-id="7391a-128">S3</span></span>
- <span data-ttu-id="7391a-129">S4</span><span class="sxs-lookup"><span data-stu-id="7391a-129">S4</span></span>

<span data-ttu-id="7391a-130">További információt a [kognitív szolgáltatás API](https://www.microsoft.com/cognitive-services/en-us/apis)-k című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="7391a-130">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7391a-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="7391a-131">-Tag</span></span>
<span data-ttu-id="7391a-132">Egy címkét név/érték párokként ad meg.</span><span class="sxs-lookup"><span data-stu-id="7391a-132">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7391a-133">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="7391a-133">-Type</span></span>
<span data-ttu-id="7391a-134">A létrehozandó fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7391a-134">Specifies the type of account to create.</span></span> <span data-ttu-id="7391a-135">A paraméter jelenlegi elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7391a-135">Current acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7391a-136">Bing. autojavasolna. v7</span><span class="sxs-lookup"><span data-stu-id="7391a-136">Bing.Autosuggest.v7</span></span>
- <span data-ttu-id="7391a-137">Bing. CustomSearch</span><span class="sxs-lookup"><span data-stu-id="7391a-137">Bing.CustomSearch</span></span>
- <span data-ttu-id="7391a-138">Bing. Search. v7</span><span class="sxs-lookup"><span data-stu-id="7391a-138">Bing.Search.v7</span></span>
- <span data-ttu-id="7391a-139">Bing. Speech (beszédfelismerés)</span><span class="sxs-lookup"><span data-stu-id="7391a-139">Bing.Speech</span></span>
- <span data-ttu-id="7391a-140">Bing. helyesírás. v7</span><span class="sxs-lookup"><span data-stu-id="7391a-140">Bing.SpellCheck.v7</span></span>
- <span data-ttu-id="7391a-141">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="7391a-141">ComputerVision</span></span>
- <span data-ttu-id="7391a-142">ContentModerator</span><span class="sxs-lookup"><span data-stu-id="7391a-142">ContentModerator</span></span>
- <span data-ttu-id="7391a-143">CustomSpeech</span><span class="sxs-lookup"><span data-stu-id="7391a-143">CustomSpeech</span></span>
- <span data-ttu-id="7391a-144">CustomVision. előrejelzés</span><span class="sxs-lookup"><span data-stu-id="7391a-144">CustomVision.Prediction</span></span>
- <span data-ttu-id="7391a-145">CustomVision. oktatás</span><span class="sxs-lookup"><span data-stu-id="7391a-145">CustomVision.Training</span></span>
- <span data-ttu-id="7391a-146">Érzelem</span><span class="sxs-lookup"><span data-stu-id="7391a-146">Emotion</span></span>
- <span data-ttu-id="7391a-147">Arc</span><span class="sxs-lookup"><span data-stu-id="7391a-147">Face</span></span>
- <span data-ttu-id="7391a-148">LUIS</span><span class="sxs-lookup"><span data-stu-id="7391a-148">LUIS</span></span>
- <span data-ttu-id="7391a-149">QnAMaker</span><span class="sxs-lookup"><span data-stu-id="7391a-149">QnAMaker</span></span>
- <span data-ttu-id="7391a-150">SpeakerRecognition</span><span class="sxs-lookup"><span data-stu-id="7391a-150">SpeakerRecognition</span></span>
- <span data-ttu-id="7391a-151">SpeechTranslation</span><span class="sxs-lookup"><span data-stu-id="7391a-151">SpeechTranslation</span></span>
- <span data-ttu-id="7391a-152">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="7391a-152">TextAnalytics</span></span>
- <span data-ttu-id="7391a-153">TextTranslation</span><span class="sxs-lookup"><span data-stu-id="7391a-153">TextTranslation</span></span>
- <span data-ttu-id="7391a-154">WebLM</span><span class="sxs-lookup"><span data-stu-id="7391a-154">WebLM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7391a-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7391a-155">-Confirm</span></span>
<span data-ttu-id="7391a-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7391a-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7391a-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7391a-157">-WhatIf</span></span>
<span data-ttu-id="7391a-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7391a-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7391a-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7391a-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7391a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7391a-160">CommonParameters</span></span>
<span data-ttu-id="7391a-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7391a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7391a-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7391a-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7391a-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7391a-163">INPUTS</span></span>

### <span data-ttu-id="7391a-164">Nincs</span><span class="sxs-lookup"><span data-stu-id="7391a-164">None</span></span>
<span data-ttu-id="7391a-165">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7391a-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7391a-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7391a-166">OUTPUTS</span></span>

### <span data-ttu-id="7391a-167">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7391a-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="7391a-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7391a-168">NOTES</span></span>

## <span data-ttu-id="7391a-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7391a-169">RELATED LINKS</span></span>

[<span data-ttu-id="7391a-170">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7391a-170">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="7391a-171">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7391a-171">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="7391a-172">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7391a-172">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
