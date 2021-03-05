---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 60a61af31b5a7986779b19b893d4c02d0039ae49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007110"
---
# <span data-ttu-id="73bc6-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="73bc6-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="73bc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="73bc6-103">Kognitív szolgáltatások fiók NetworkRule tulajdonságának be szereznie</span><span class="sxs-lookup"><span data-stu-id="73bc6-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="73bc6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="73bc6-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73bc6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="73bc6-105">DESCRIPTION</span></span>
<span data-ttu-id="73bc6-106">A **Get-AzCognitiveServicesAccountNetworkRuleSet** parancsmag egy Kognitív szolgáltatások-fiók NetworkRule tulajdonságát kapja meg</span><span class="sxs-lookup"><span data-stu-id="73bc6-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="73bc6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="73bc6-107">EXAMPLES</span></span>

### <span data-ttu-id="73bc6-108">1. példa: Adott Kognitív Szolgáltatások-fiók NetworkRule tulajdonságának be szereznie</span><span class="sxs-lookup"><span data-stu-id="73bc6-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="73bc6-109">Ez a parancs egy adott Kognitív szolgáltatások-fiók NetworkRule tulajdonságát kapja meg</span><span class="sxs-lookup"><span data-stu-id="73bc6-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="73bc6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73bc6-110">PARAMETERS</span></span>

### <span data-ttu-id="73bc6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73bc6-111">-DefaultProfile</span></span>
<span data-ttu-id="73bc6-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73bc6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73bc6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="73bc6-113">-Name</span></span>
<span data-ttu-id="73bc6-114">Kognitív szolgáltatások fiókneve.</span><span class="sxs-lookup"><span data-stu-id="73bc6-114">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="73bc6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73bc6-115">-ResourceGroupName</span></span>
<span data-ttu-id="73bc6-116">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="73bc6-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="73bc6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bc6-117">CommonParameters</span></span>
<span data-ttu-id="73bc6-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73bc6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bc6-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73bc6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bc6-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73bc6-120">INPUTS</span></span>

### <span data-ttu-id="73bc6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="73bc6-121">System.String</span></span>

## <span data-ttu-id="73bc6-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73bc6-122">OUTPUTS</span></span>

### <span data-ttu-id="73bc6-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="73bc6-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="73bc6-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="73bc6-124">NOTES</span></span>

## <span data-ttu-id="73bc6-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73bc6-125">RELATED LINKS</span></span>
