---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: 3f442cc975c6fdbb95d53153c2c80615bb8676a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362052"
---
# <span data-ttu-id="db21d-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db21d-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="db21d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db21d-102">SYNOPSIS</span></span>
<span data-ttu-id="db21d-103">Fiókot kap.</span><span class="sxs-lookup"><span data-stu-id="db21d-103">Gets an account.</span></span>

## <span data-ttu-id="db21d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db21d-104">SYNTAX</span></span>

### <span data-ttu-id="db21d-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="db21d-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db21d-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db21d-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db21d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db21d-107">DESCRIPTION</span></span>
<span data-ttu-id="db21d-108">A **Get-AzCognitiveServicesAccount** parancsmag a ResourceGroupName paraméterrel megadott erőforráscsoportban kapja meg a kiépített *Kognitív szolgáltatások-fiókokat.*</span><span class="sxs-lookup"><span data-stu-id="db21d-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="db21d-109">Ha nem adja meg az *ResourceGroupName* paramétert, ez a parancsmag az aktuális előfizetés összes kognitív szolgáltatásfiókját megkapja.</span><span class="sxs-lookup"><span data-stu-id="db21d-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="db21d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db21d-110">EXAMPLES</span></span>

### <span data-ttu-id="db21d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="db21d-111">Example 1</span></span>
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

## <span data-ttu-id="db21d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db21d-112">PARAMETERS</span></span>

### <span data-ttu-id="db21d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db21d-113">-DefaultProfile</span></span>
<span data-ttu-id="db21d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="db21d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db21d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="db21d-115">-Name</span></span>
<span data-ttu-id="db21d-116">A lekért Kognitív szolgáltatások fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db21d-116">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="db21d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db21d-117">-ResourceGroupName</span></span>
<span data-ttu-id="db21d-118">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a Kognitív szolgáltatások fiók van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="db21d-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="db21d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db21d-119">CommonParameters</span></span>
<span data-ttu-id="db21d-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db21d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db21d-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db21d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db21d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db21d-122">INPUTS</span></span>

### <span data-ttu-id="db21d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="db21d-123">System.String</span></span>

## <span data-ttu-id="db21d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db21d-124">OUTPUTS</span></span>

### <span data-ttu-id="db21d-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db21d-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="db21d-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db21d-126">NOTES</span></span>

## <span data-ttu-id="db21d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db21d-127">RELATED LINKS</span></span>

[<span data-ttu-id="db21d-128">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db21d-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="db21d-129">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db21d-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="db21d-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db21d-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


