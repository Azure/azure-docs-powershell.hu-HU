---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 57d136691d6ca0ac9bcd85f205d70cf267437b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667533"
---
# <span data-ttu-id="7f5fe-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7f5fe-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="7f5fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f5fe-102">SYNOPSIS</span></span>
<span data-ttu-id="7f5fe-103">Módosítja a fiókot.</span><span class="sxs-lookup"><span data-stu-id="7f5fe-103">Modifies an account.</span></span>

## <span data-ttu-id="7f5fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f5fe-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f5fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f5fe-105">DESCRIPTION</span></span>
<span data-ttu-id="7f5fe-106">A **set-AzCognitiveServicesAccount** parancsmag a megadott kognitív Services-fiók SKU-ának vagy címkéjének módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="7f5fe-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="7f5fe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7f5fe-107">EXAMPLES</span></span>

### <span data-ttu-id="7f5fe-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7f5fe-108">Example 1</span></span>
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

## <span data-ttu-id="7f5fe-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f5fe-109">PARAMETERS</span></span>

### <span data-ttu-id="7f5fe-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="7f5fe-110">-CustomSubdomainName</span></span>
<span data-ttu-id="7f5fe-111">A kognitív szolgáltatások fiók altartományának neve.</span><span class="sxs-lookup"><span data-stu-id="7f5fe-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="7f5fe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f5fe-112">-DefaultProfile</span></span>
<span data-ttu-id="7f5fe-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7f5fe-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f5fe-114">-Force</span><span class="sxs-lookup"><span data-stu-id="7f5fe-114">-Force</span></span>
<span data-ttu-id="7f5fe-115">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7f5fe-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f5fe-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7f5fe-116">-Name</span></span>
<span data-ttu-id="7f5fe-117">A módosítani kívánt fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f5fe-117">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="7f5fe-118">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f5fe-118">-NetworkRuleSet</span></span>
<span data-ttu-id="7f5fe-119">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazát, valamint a hálózati tulajdonságok értékének beállítását, például az olyan kérelmek kezelését ismerteti, amelyek nem felelnek meg a megadott szabályoknak</span><span class="sxs-lookup"><span data-stu-id="7f5fe-119">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f5fe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f5fe-120">-ResourceGroupName</span></span>
<span data-ttu-id="7f5fe-121">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="7f5fe-121">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="7f5fe-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7f5fe-122">-SkuName</span></span>
<span data-ttu-id="7f5fe-123">A fiókhoz tartozó SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f5fe-123">Specifies the SKU for the account.</span></span>
<span data-ttu-id="7f5fe-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7f5fe-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f5fe-125">F0 (ingyenes Tier)</span><span class="sxs-lookup"><span data-stu-id="7f5fe-125">F0 (free tier)</span></span>
- <span data-ttu-id="7f5fe-126">S0</span><span class="sxs-lookup"><span data-stu-id="7f5fe-126">S0</span></span>
- <span data-ttu-id="7f5fe-127">S1</span><span class="sxs-lookup"><span data-stu-id="7f5fe-127">S1</span></span>
- <span data-ttu-id="7f5fe-128">S2</span><span class="sxs-lookup"><span data-stu-id="7f5fe-128">S2</span></span>
- <span data-ttu-id="7f5fe-129">S3</span><span class="sxs-lookup"><span data-stu-id="7f5fe-129">S3</span></span>
- <span data-ttu-id="7f5fe-130">S4</span><span class="sxs-lookup"><span data-stu-id="7f5fe-130">S4</span></span>

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

### <span data-ttu-id="7f5fe-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="7f5fe-131">-Tag</span></span>
<span data-ttu-id="7f5fe-132">Egy címkét név/érték párokként ad meg.</span><span class="sxs-lookup"><span data-stu-id="7f5fe-132">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="7f5fe-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7f5fe-133">-Confirm</span></span>
<span data-ttu-id="7f5fe-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7f5fe-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f5fe-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f5fe-135">-WhatIf</span></span>
<span data-ttu-id="7f5fe-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7f5fe-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f5fe-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f5fe-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f5fe-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f5fe-138">CommonParameters</span></span>
<span data-ttu-id="7f5fe-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f5fe-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f5fe-140">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7f5fe-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f5fe-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f5fe-141">INPUTS</span></span>

### <span data-ttu-id="7f5fe-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7f5fe-142">System.String</span></span>

### <span data-ttu-id="7f5fe-143">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="7f5fe-143">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="7f5fe-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f5fe-144">OUTPUTS</span></span>

### <span data-ttu-id="7f5fe-145">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7f5fe-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="7f5fe-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f5fe-146">NOTES</span></span>

## <span data-ttu-id="7f5fe-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f5fe-147">RELATED LINKS</span></span>

[<span data-ttu-id="7f5fe-148">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7f5fe-148">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="7f5fe-149">Új – AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7f5fe-149">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="7f5fe-150">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7f5fe-150">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
