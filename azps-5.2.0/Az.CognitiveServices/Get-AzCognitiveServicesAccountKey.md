---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331386"
---
# <span data-ttu-id="29976-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="29976-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="29976-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29976-102">SYNOPSIS</span></span>
<span data-ttu-id="29976-103">Egy fiók API-kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="29976-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="29976-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="29976-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29976-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="29976-105">DESCRIPTION</span></span>
<span data-ttu-id="29976-106">A **Get-AzCognitiveServicesAccountKey** parancsmag egy kiépített Kognitív Szolgáltatások-fiók API-kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="29976-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="29976-107">A kognitív szolgáltatások fiókja két API-kulccsal rendelkezik: Key1 és Key2.</span><span class="sxs-lookup"><span data-stu-id="29976-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="29976-108">A kulcsok lehetővé teszik a kognitív szolgáltatások fiók végpontjának interakcióját.</span><span class="sxs-lookup"><span data-stu-id="29976-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="29976-109">A New-AzCognitiveServicesAccountKey újragenerál egy kulcsot.</span><span class="sxs-lookup"><span data-stu-id="29976-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="29976-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="29976-110">EXAMPLES</span></span>

### <span data-ttu-id="29976-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="29976-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="29976-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29976-112">PARAMETERS</span></span>

### <span data-ttu-id="29976-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29976-113">-DefaultProfile</span></span>
<span data-ttu-id="29976-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="29976-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29976-115">-Name</span><span class="sxs-lookup"><span data-stu-id="29976-115">-Name</span></span>
<span data-ttu-id="29976-116">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29976-116">Specifies the name of the account.</span></span>
<span data-ttu-id="29976-117">Ez a parancsmag megkapja a fiók kulcsait.</span><span class="sxs-lookup"><span data-stu-id="29976-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="29976-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29976-118">-ResourceGroupName</span></span>
<span data-ttu-id="29976-119">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="29976-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="29976-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29976-120">CommonParameters</span></span>
<span data-ttu-id="29976-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29976-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29976-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29976-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29976-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29976-123">INPUTS</span></span>

### <span data-ttu-id="29976-124">System.String</span><span class="sxs-lookup"><span data-stu-id="29976-124">System.String</span></span>

## <span data-ttu-id="29976-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29976-125">OUTPUTS</span></span>

### <span data-ttu-id="29976-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="29976-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="29976-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="29976-127">NOTES</span></span>

## <span data-ttu-id="29976-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29976-128">RELATED LINKS</span></span>

[<span data-ttu-id="29976-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="29976-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


