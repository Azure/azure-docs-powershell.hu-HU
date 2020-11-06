---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: b0e47d95d8ede448b37ef62e0b9deb7283d293c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492845"
---
# <span data-ttu-id="10d27-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="10d27-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="10d27-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10d27-102">SYNOPSIS</span></span>
<span data-ttu-id="10d27-103">A fiók API-kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="10d27-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10d27-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10d27-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10d27-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="10d27-105">DESCRIPTION</span></span>
<span data-ttu-id="10d27-106">A **Get-AzureRmCognitiveServicesAccountKey** parancsmag beilleszti az API-kulcsokat egy kiépített kognitív Services-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="10d27-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="10d27-107">A kognitív szolgáltatások fiók két API-kulcsból áll: Key1 és Azonosító2.</span><span class="sxs-lookup"><span data-stu-id="10d27-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="10d27-108">A billentyűk lehetővé teszik az interakciót a kognitív szolgáltatások fiókja végponttal.</span><span class="sxs-lookup"><span data-stu-id="10d27-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="10d27-109">A billentyűk újragenerálásához használja a New-AzureRmCognitiveServicesAccountKey.</span><span class="sxs-lookup"><span data-stu-id="10d27-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="10d27-110">Példák</span><span class="sxs-lookup"><span data-stu-id="10d27-110">EXAMPLES</span></span>

### <span data-ttu-id="10d27-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="10d27-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="10d27-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10d27-112">PARAMETERS</span></span>

### <span data-ttu-id="10d27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d27-113">-DefaultProfile</span></span>
<span data-ttu-id="10d27-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="10d27-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10d27-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="10d27-115">-Name</span></span>
<span data-ttu-id="10d27-116">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10d27-116">Specifies the name of the account.</span></span>
<span data-ttu-id="10d27-117">Ez a parancsmag a fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="10d27-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="10d27-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10d27-118">-ResourceGroupName</span></span>
<span data-ttu-id="10d27-119">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="10d27-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="10d27-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d27-120">CommonParameters</span></span>
<span data-ttu-id="10d27-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10d27-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d27-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10d27-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d27-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10d27-123">INPUTS</span></span>

### <span data-ttu-id="10d27-124">System. String</span><span class="sxs-lookup"><span data-stu-id="10d27-124">System.String</span></span>

## <span data-ttu-id="10d27-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10d27-125">OUTPUTS</span></span>

### <span data-ttu-id="10d27-126">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="10d27-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="10d27-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10d27-127">NOTES</span></span>

## <span data-ttu-id="10d27-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10d27-128">RELATED LINKS</span></span>

[<span data-ttu-id="10d27-129">Új – AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="10d27-129">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


