---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 74c066cd59497603da4f953f35ed16e454e67155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672802"
---
# <span data-ttu-id="b7653-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b7653-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="b7653-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7653-102">SYNOPSIS</span></span>
<span data-ttu-id="b7653-103">Módosítja a fiókot.</span><span class="sxs-lookup"><span data-stu-id="b7653-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7653-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7653-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7653-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7653-105">DESCRIPTION</span></span>
<span data-ttu-id="b7653-106">A **set-AzureRmCognitiveServicesAccount** parancsmag a megadott kognitív Services-fiók SKU-ának vagy címkéjének módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="b7653-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="b7653-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b7653-107">EXAMPLES</span></span>

### <span data-ttu-id="b7653-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b7653-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="b7653-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7653-109">PARAMETERS</span></span>

### <span data-ttu-id="b7653-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7653-110">-DefaultProfile</span></span>
<span data-ttu-id="b7653-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b7653-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7653-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b7653-112">-Force</span></span>
<span data-ttu-id="b7653-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b7653-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b7653-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b7653-114">-Name</span></span>
<span data-ttu-id="b7653-115">A módosítani kívánt fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7653-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="b7653-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7653-116">-ResourceGroupName</span></span>
<span data-ttu-id="b7653-117">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b7653-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="b7653-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b7653-118">-SkuName</span></span>
<span data-ttu-id="b7653-119">A fiókhoz tartozó SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7653-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="b7653-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b7653-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7653-121">F0 (ingyenes Tier)</span><span class="sxs-lookup"><span data-stu-id="b7653-121">F0 (free tier)</span></span>
- <span data-ttu-id="b7653-122">S0</span><span class="sxs-lookup"><span data-stu-id="b7653-122">S0</span></span>
- <span data-ttu-id="b7653-123">S1</span><span class="sxs-lookup"><span data-stu-id="b7653-123">S1</span></span>
- <span data-ttu-id="b7653-124">S2</span><span class="sxs-lookup"><span data-stu-id="b7653-124">S2</span></span>
- <span data-ttu-id="b7653-125">S3</span><span class="sxs-lookup"><span data-stu-id="b7653-125">S3</span></span>
- <span data-ttu-id="b7653-126">S4</span><span class="sxs-lookup"><span data-stu-id="b7653-126">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7653-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="b7653-127">-Tag</span></span>
<span data-ttu-id="b7653-128">Egy címkét név/érték párokként ad meg.</span><span class="sxs-lookup"><span data-stu-id="b7653-128">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7653-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7653-129">-Confirm</span></span>
<span data-ttu-id="b7653-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7653-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7653-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7653-131">-WhatIf</span></span>
<span data-ttu-id="b7653-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b7653-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7653-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7653-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7653-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7653-134">CommonParameters</span></span>
<span data-ttu-id="b7653-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7653-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7653-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7653-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7653-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7653-137">INPUTS</span></span>

### <span data-ttu-id="b7653-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b7653-138">System.String</span></span>

### <span data-ttu-id="b7653-139">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="b7653-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="b7653-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7653-140">OUTPUTS</span></span>

### <span data-ttu-id="b7653-141">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b7653-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="b7653-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7653-142">NOTES</span></span>

## <span data-ttu-id="b7653-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7653-143">RELATED LINKS</span></span>

[<span data-ttu-id="b7653-144">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b7653-144">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b7653-145">Új – AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b7653-145">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b7653-146">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b7653-146">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
