---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: 35815afe33329ebfae92638f47176043bf6f5844
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667553"
---
# <span data-ttu-id="92f69-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="92f69-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="92f69-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92f69-102">SYNOPSIS</span></span>
<span data-ttu-id="92f69-103">Megkapja a fiókot.</span><span class="sxs-lookup"><span data-stu-id="92f69-103">Gets an account.</span></span>

## <span data-ttu-id="92f69-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92f69-104">SYNTAX</span></span>

### <span data-ttu-id="92f69-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="92f69-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92f69-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="92f69-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92f69-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="92f69-107">DESCRIPTION</span></span>
<span data-ttu-id="92f69-108">A **Get-AzCognitiveServicesAccount** parancsmag a kiépített kognitív szolgáltatások fiókját a *ResourceGroupName* paraméterrel megadott erőforráscsoport szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="92f69-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="92f69-109">Ha nem adja meg a *ResourceGroupName* paramétert, ez a parancsmag a jelenlegi előfizetéshez az összes kognitív szolgáltatási fiókot kapja.</span><span class="sxs-lookup"><span data-stu-id="92f69-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="92f69-110">Példák</span><span class="sxs-lookup"><span data-stu-id="92f69-110">EXAMPLES</span></span>

### <span data-ttu-id="92f69-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="92f69-111">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locati
on 'WestUS'

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

## <span data-ttu-id="92f69-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92f69-112">PARAMETERS</span></span>

### <span data-ttu-id="92f69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f69-113">-DefaultProfile</span></span>
<span data-ttu-id="92f69-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="92f69-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92f69-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="92f69-115">-Name</span></span>
<span data-ttu-id="92f69-116">A beszerzéshez a kognitív Services-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="92f69-116">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f69-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f69-117">-ResourceGroupName</span></span>
<span data-ttu-id="92f69-118">Annak a csoportnak a nevét adja meg, amelyre a kognitív Services-fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="92f69-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f69-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f69-119">CommonParameters</span></span>
<span data-ttu-id="92f69-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92f69-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f69-121">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="92f69-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f69-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92f69-122">INPUTS</span></span>

### <span data-ttu-id="92f69-123">System. String</span><span class="sxs-lookup"><span data-stu-id="92f69-123">System.String</span></span>

## <span data-ttu-id="92f69-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92f69-124">OUTPUTS</span></span>

### <span data-ttu-id="92f69-125">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="92f69-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="92f69-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92f69-126">NOTES</span></span>

## <span data-ttu-id="92f69-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92f69-127">RELATED LINKS</span></span>

[<span data-ttu-id="92f69-128">Új – AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="92f69-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="92f69-129">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="92f69-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="92f69-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="92f69-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


