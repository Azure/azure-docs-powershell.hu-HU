---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2544531d9a988daaea314fc2088609df77b719b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671387"
---
# <span data-ttu-id="c39d7-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c39d7-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="c39d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c39d7-102">SYNOPSIS</span></span>
<span data-ttu-id="c39d7-103">Módosítja a fiókot.</span><span class="sxs-lookup"><span data-stu-id="c39d7-103">Modifies an account.</span></span>

## <span data-ttu-id="c39d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c39d7-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c39d7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c39d7-105">DESCRIPTION</span></span>
<span data-ttu-id="c39d7-106">A **set-AzCognitiveServicesAccount** parancsmag a megadott kognitív Services-fiók SKU-ának vagy címkéjének módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="c39d7-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="c39d7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c39d7-107">EXAMPLES</span></span>

### <span data-ttu-id="c39d7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c39d7-108">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


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

## <span data-ttu-id="c39d7-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c39d7-109">PARAMETERS</span></span>

### <span data-ttu-id="c39d7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c39d7-110">-DefaultProfile</span></span>
<span data-ttu-id="c39d7-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c39d7-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c39d7-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c39d7-112">-Force</span></span>
<span data-ttu-id="c39d7-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c39d7-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c39d7-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c39d7-114">-Name</span></span>
<span data-ttu-id="c39d7-115">A módosítani kívánt fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39d7-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="c39d7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c39d7-116">-ResourceGroupName</span></span>
<span data-ttu-id="c39d7-117">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="c39d7-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="c39d7-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c39d7-118">-SkuName</span></span>
<span data-ttu-id="c39d7-119">A fiókhoz tartozó SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39d7-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="c39d7-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c39d7-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c39d7-121">F0 (ingyenes Tier)</span><span class="sxs-lookup"><span data-stu-id="c39d7-121">F0 (free tier)</span></span>
- <span data-ttu-id="c39d7-122">S0</span><span class="sxs-lookup"><span data-stu-id="c39d7-122">S0</span></span>
- <span data-ttu-id="c39d7-123">S1</span><span class="sxs-lookup"><span data-stu-id="c39d7-123">S1</span></span>
- <span data-ttu-id="c39d7-124">S2</span><span class="sxs-lookup"><span data-stu-id="c39d7-124">S2</span></span>
- <span data-ttu-id="c39d7-125">S3</span><span class="sxs-lookup"><span data-stu-id="c39d7-125">S3</span></span>
- <span data-ttu-id="c39d7-126">S4</span><span class="sxs-lookup"><span data-stu-id="c39d7-126">S4</span></span>

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

### <span data-ttu-id="c39d7-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="c39d7-127">-Tag</span></span>
<span data-ttu-id="c39d7-128">Egy címkét név/érték párokként ad meg.</span><span class="sxs-lookup"><span data-stu-id="c39d7-128">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="c39d7-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c39d7-129">-Confirm</span></span>
<span data-ttu-id="c39d7-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c39d7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c39d7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c39d7-131">-WhatIf</span></span>
<span data-ttu-id="c39d7-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c39d7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c39d7-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c39d7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c39d7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39d7-134">CommonParameters</span></span>
<span data-ttu-id="c39d7-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c39d7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c39d7-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c39d7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39d7-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c39d7-137">INPUTS</span></span>

### <span data-ttu-id="c39d7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c39d7-138">System.String</span></span>

### <span data-ttu-id="c39d7-139">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="c39d7-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="c39d7-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c39d7-140">OUTPUTS</span></span>

### <span data-ttu-id="c39d7-141">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c39d7-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="c39d7-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c39d7-142">NOTES</span></span>

## <span data-ttu-id="c39d7-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c39d7-143">RELATED LINKS</span></span>

[<span data-ttu-id="c39d7-144">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c39d7-144">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c39d7-145">Új – AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c39d7-145">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c39d7-146">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c39d7-146">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
