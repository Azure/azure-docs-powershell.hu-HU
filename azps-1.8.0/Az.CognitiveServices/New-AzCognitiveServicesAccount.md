---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 7e5253951ec3c74850584aaac9818a6a7c8f2737
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671389"
---
# <span data-ttu-id="8ef69-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8ef69-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="8ef69-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ef69-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef69-103">Kognitív szolgáltatások fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8ef69-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="8ef69-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ef69-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ef69-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ef69-105">DESCRIPTION</span></span>
<span data-ttu-id="8ef69-106">A **New-AzCognitiveServicesAccount** parancsmag a megadott típusú és SKU-hoz létrehoz egy kognitív szolgáltatásokat tartalmazó fiókot.</span><span class="sxs-lookup"><span data-stu-id="8ef69-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="8ef69-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8ef69-107">EXAMPLES</span></span>

### <span data-ttu-id="8ef69-108">1:</span><span class="sxs-lookup"><span data-stu-id="8ef69-108">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
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

## <span data-ttu-id="8ef69-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ef69-109">PARAMETERS</span></span>

### <span data-ttu-id="8ef69-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="8ef69-110">-CustomSubdomainName</span></span>
<span data-ttu-id="8ef69-111">A kognitív szolgáltatások fiók altartományának neve.</span><span class="sxs-lookup"><span data-stu-id="8ef69-111">Cognitive Services Account Subdomain Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ef69-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ef69-112">-DefaultProfile</span></span>
<span data-ttu-id="8ef69-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8ef69-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ef69-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8ef69-114">-Force</span></span>
<span data-ttu-id="8ef69-115">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8ef69-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8ef69-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="8ef69-116">-Location</span></span>
<span data-ttu-id="8ef69-117">Azt a helyet adja meg, ahol létre szeretné hozni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="8ef69-117">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="8ef69-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8ef69-118">-Name</span></span>
<span data-ttu-id="8ef69-119">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ef69-119">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="8ef69-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ef69-120">-ResourceGroupName</span></span>
<span data-ttu-id="8ef69-121">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez hozzá szeretné rendelni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="8ef69-121">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="8ef69-122">Az erőforráscsoportnek már léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="8ef69-122">The resource group must already exist.</span></span>

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

### <span data-ttu-id="8ef69-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8ef69-123">-SkuName</span></span>
<span data-ttu-id="8ef69-124">A fiókhoz tartozó SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ef69-124">Specifies the SKU for the account.</span></span>
<span data-ttu-id="8ef69-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8ef69-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8ef69-126">F0 (ingyenes Tier)</span><span class="sxs-lookup"><span data-stu-id="8ef69-126">F0 (free tier)</span></span>
- <span data-ttu-id="8ef69-127">S0</span><span class="sxs-lookup"><span data-stu-id="8ef69-127">S0</span></span>
- <span data-ttu-id="8ef69-128">S1</span><span class="sxs-lookup"><span data-stu-id="8ef69-128">S1</span></span>
- <span data-ttu-id="8ef69-129">S2</span><span class="sxs-lookup"><span data-stu-id="8ef69-129">S2</span></span>
- <span data-ttu-id="8ef69-130">S3</span><span class="sxs-lookup"><span data-stu-id="8ef69-130">S3</span></span>
- <span data-ttu-id="8ef69-131">S4 további tudnivalókért olvassa el a [kognitív szolgáltatás API](https://www.microsoft.com/cognitive-services/en-us/apis)-k című témakört.</span><span class="sxs-lookup"><span data-stu-id="8ef69-131">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="8ef69-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="8ef69-132">-Tag</span></span>
<span data-ttu-id="8ef69-133">Egy címkét név/érték párokként ad meg.</span><span class="sxs-lookup"><span data-stu-id="8ef69-133">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="8ef69-134">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="8ef69-134">-Type</span></span>
<span data-ttu-id="8ef69-135">A létrehozandó fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ef69-135">Specifies the type of account to create.</span></span> <span data-ttu-id="8ef69-136">Használja `Get-AzCognitiveServicesAccountType` a parancsmagot a jelenlegi elfogadható értékek beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="8ef69-136">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="8ef69-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8ef69-137">-Confirm</span></span>
<span data-ttu-id="8ef69-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8ef69-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ef69-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ef69-139">-WhatIf</span></span>
<span data-ttu-id="8ef69-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8ef69-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ef69-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ef69-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ef69-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef69-142">CommonParameters</span></span>
<span data-ttu-id="8ef69-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ef69-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef69-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ef69-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef69-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ef69-145">INPUTS</span></span>

### <span data-ttu-id="8ef69-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8ef69-146">System.String</span></span>

## <span data-ttu-id="8ef69-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ef69-147">OUTPUTS</span></span>

### <span data-ttu-id="8ef69-148">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8ef69-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="8ef69-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ef69-149">NOTES</span></span>

## <span data-ttu-id="8ef69-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ef69-150">RELATED LINKS</span></span>

[<span data-ttu-id="8ef69-151">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8ef69-151">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8ef69-152">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8ef69-152">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8ef69-153">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8ef69-153">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
