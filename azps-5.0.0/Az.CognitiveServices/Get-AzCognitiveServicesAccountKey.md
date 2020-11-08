---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194125"
---
# <span data-ttu-id="9f332-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="9f332-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="9f332-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f332-102">SYNOPSIS</span></span>
<span data-ttu-id="9f332-103">A fiók API-kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="9f332-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="9f332-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f332-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f332-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f332-105">DESCRIPTION</span></span>
<span data-ttu-id="9f332-106">A **Get-AzCognitiveServicesAccountKey** parancsmag beilleszti az API-kulcsokat egy kiépített kognitív Services-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="9f332-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="9f332-107">A kognitív szolgáltatások fiók két API-kulcsból áll: Key1 és Azonosító2.</span><span class="sxs-lookup"><span data-stu-id="9f332-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="9f332-108">A billentyűk lehetővé teszik az interakciót a kognitív szolgáltatások fiókja végponttal.</span><span class="sxs-lookup"><span data-stu-id="9f332-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="9f332-109">A billentyűk újragenerálásához használja a New-AzCognitiveServicesAccountKey.</span><span class="sxs-lookup"><span data-stu-id="9f332-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="9f332-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9f332-110">EXAMPLES</span></span>

### <span data-ttu-id="9f332-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9f332-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="9f332-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f332-112">PARAMETERS</span></span>

### <span data-ttu-id="9f332-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f332-113">-DefaultProfile</span></span>
<span data-ttu-id="9f332-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9f332-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f332-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9f332-115">-Name</span></span>
<span data-ttu-id="9f332-116">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f332-116">Specifies the name of the account.</span></span>
<span data-ttu-id="9f332-117">Ez a parancsmag a fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9f332-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="9f332-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f332-118">-ResourceGroupName</span></span>
<span data-ttu-id="9f332-119">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="9f332-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="9f332-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f332-120">CommonParameters</span></span>
<span data-ttu-id="9f332-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f332-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f332-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9f332-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f332-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f332-123">INPUTS</span></span>

### <span data-ttu-id="9f332-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9f332-124">System.String</span></span>

## <span data-ttu-id="9f332-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f332-125">OUTPUTS</span></span>

### <span data-ttu-id="9f332-126">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9f332-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="9f332-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f332-127">NOTES</span></span>

## <span data-ttu-id="9f332-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f332-128">RELATED LINKS</span></span>

[<span data-ttu-id="9f332-129">Új – AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="9f332-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


