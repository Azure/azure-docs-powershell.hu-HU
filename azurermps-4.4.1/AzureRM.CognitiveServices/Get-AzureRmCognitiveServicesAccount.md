---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: c4419707c9c536a21e5fdc8aa39326b02e21937c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497835"
---
# <span data-ttu-id="501d1-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="501d1-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="501d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="501d1-102">SYNOPSIS</span></span>
<span data-ttu-id="501d1-103">Megkapja a fiókot.</span><span class="sxs-lookup"><span data-stu-id="501d1-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="501d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="501d1-104">SYNTAX</span></span>

### <span data-ttu-id="501d1-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="501d1-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="501d1-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="501d1-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="501d1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="501d1-107">DESCRIPTION</span></span>
<span data-ttu-id="501d1-108">A **Get-AzureRmCognitiveServicesAccount** parancsmag a kiépített kognitív szolgáltatások fiókját a *ResoureGroupName* paraméterrel megadott erőforráscsoport szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="501d1-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>

<span data-ttu-id="501d1-109">Ha nem adja meg a *ResoureGroupName* paramétert, ez a parancsmag a jelenlegi előfizetéshez az összes kognitív szolgáltatási fiókot kapja.</span><span class="sxs-lookup"><span data-stu-id="501d1-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="501d1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="501d1-110">EXAMPLES</span></span>

## <span data-ttu-id="501d1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="501d1-111">PARAMETERS</span></span>

### <span data-ttu-id="501d1-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="501d1-112">-Name</span></span>
<span data-ttu-id="501d1-113">A beszerzéshez a kognitív Services-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="501d1-113">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="501d1-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="501d1-114">-ResourceGroupName</span></span>
<span data-ttu-id="501d1-115">Annak a csoportnak a nevét adja meg, amelyre a kognitív Services-fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="501d1-115">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="501d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="501d1-116">-DefaultProfile</span></span>
<span data-ttu-id="501d1-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="501d1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="501d1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="501d1-118">CommonParameters</span></span>
<span data-ttu-id="501d1-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="501d1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="501d1-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="501d1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="501d1-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="501d1-121">INPUTS</span></span>

## <span data-ttu-id="501d1-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="501d1-122">OUTPUTS</span></span>

### <span data-ttu-id="501d1-123">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="501d1-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="501d1-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="501d1-124">NOTES</span></span>

## <span data-ttu-id="501d1-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="501d1-125">RELATED LINKS</span></span>

[<span data-ttu-id="501d1-126">Új – AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="501d1-126">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="501d1-127">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="501d1-127">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="501d1-128">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="501d1-128">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


