---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a182bed0e93492521e3ac46d5f0ed3e2d705394c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505228"
---
# <span data-ttu-id="ad4ee-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ad4ee-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="ad4ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4ee-103">A kognitív Services-fiók törlése</span><span class="sxs-lookup"><span data-stu-id="ad4ee-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad4ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad4ee-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad4ee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad4ee-105">DESCRIPTION</span></span>
<span data-ttu-id="ad4ee-106">A **Remove-AzureRmCognitiveServicesAccount** parancsmag törli a megadott kognitív Services-fiókot.</span><span class="sxs-lookup"><span data-stu-id="ad4ee-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="ad4ee-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ad4ee-107">EXAMPLES</span></span>

## <span data-ttu-id="ad4ee-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad4ee-108">PARAMETERS</span></span>

### <span data-ttu-id="ad4ee-109">-Force</span><span class="sxs-lookup"><span data-stu-id="ad4ee-109">-Force</span></span>
<span data-ttu-id="ad4ee-110">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ad4ee-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad4ee-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad4ee-111">-Name</span></span>
<span data-ttu-id="ad4ee-112">A törlendő fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad4ee-112">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="ad4ee-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad4ee-113">-ResourceGroupName</span></span>
<span data-ttu-id="ad4ee-114">Annak a csoportnak a nevét adja meg, amelyre a kognitív Services-fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="ad4ee-114">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="ad4ee-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad4ee-115">-Confirm</span></span>
<span data-ttu-id="ad4ee-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad4ee-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad4ee-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad4ee-117">-WhatIf</span></span>
<span data-ttu-id="ad4ee-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad4ee-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad4ee-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad4ee-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad4ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4ee-120">-DefaultProfile</span></span>
<span data-ttu-id="ad4ee-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad4ee-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad4ee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4ee-122">CommonParameters</span></span>
<span data-ttu-id="ad4ee-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad4ee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4ee-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4ee-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4ee-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad4ee-125">INPUTS</span></span>

## <span data-ttu-id="ad4ee-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad4ee-126">OUTPUTS</span></span>

## <span data-ttu-id="ad4ee-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad4ee-127">NOTES</span></span>

## <span data-ttu-id="ad4ee-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad4ee-128">RELATED LINKS</span></span>

[<span data-ttu-id="ad4ee-129">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ad4ee-129">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="ad4ee-130">Új – AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ad4ee-130">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="ad4ee-131">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ad4ee-131">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


