---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018155"
---
# <span data-ttu-id="abd42-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="abd42-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="abd42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abd42-102">SYNOPSIS</span></span>
<span data-ttu-id="abd42-103">A NetworkRule tulajdonság beszerzése a kognitív szolgáltatások fiókban</span><span class="sxs-lookup"><span data-stu-id="abd42-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="abd42-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abd42-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abd42-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="abd42-105">DESCRIPTION</span></span>
<span data-ttu-id="abd42-106">A **Get-AzCognitiveServicesAccountNetworkRuleSet** parancsmag a NetworkRule tulajdonságát kapja meg a kognitív Services-fiókban.</span><span class="sxs-lookup"><span data-stu-id="abd42-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="abd42-107">Példák</span><span class="sxs-lookup"><span data-stu-id="abd42-107">EXAMPLES</span></span>

### <span data-ttu-id="abd42-108">Példa 1: a NetworkRule tulajdonság beszerzése egy megadott kognitív szolgáltatási fiókból</span><span class="sxs-lookup"><span data-stu-id="abd42-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="abd42-109">Ez a parancs beolvassa a NetworkRule tulajdonságot egy megadott kognitív Services-fiókkal.</span><span class="sxs-lookup"><span data-stu-id="abd42-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="abd42-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abd42-110">PARAMETERS</span></span>

### <span data-ttu-id="abd42-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd42-111">-DefaultProfile</span></span>
<span data-ttu-id="abd42-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abd42-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abd42-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="abd42-113">-Name</span></span>
<span data-ttu-id="abd42-114">A kognitív szolgáltatások fiók neve.</span><span class="sxs-lookup"><span data-stu-id="abd42-114">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="abd42-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abd42-115">-ResourceGroupName</span></span>
<span data-ttu-id="abd42-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="abd42-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="abd42-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd42-117">CommonParameters</span></span>
<span data-ttu-id="abd42-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abd42-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd42-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="abd42-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd42-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abd42-120">INPUTS</span></span>

### <span data-ttu-id="abd42-121">System. String</span><span class="sxs-lookup"><span data-stu-id="abd42-121">System.String</span></span>

## <span data-ttu-id="abd42-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abd42-122">OUTPUTS</span></span>

### <span data-ttu-id="abd42-123">Microsoft. Azure. Command. Management. CognitiveServices. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="abd42-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="abd42-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abd42-124">NOTES</span></span>

## <span data-ttu-id="abd42-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abd42-125">RELATED LINKS</span></span>
