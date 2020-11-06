---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 345e7c6365a66abde5f350f20f614d4d6c94b1b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505235"
---
# <span data-ttu-id="63253-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="63253-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="63253-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63253-102">SYNOPSIS</span></span>
<span data-ttu-id="63253-103">Visszahozza a fiók kulcsát.</span><span class="sxs-lookup"><span data-stu-id="63253-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63253-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63253-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63253-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="63253-105">DESCRIPTION</span></span>
<span data-ttu-id="63253-106">A **New-AzureRmCognitiveServicesAccountKey** parancsmag regenerálta egy API-kulcsot a kognitív szolgáltatások fiókjához.</span><span class="sxs-lookup"><span data-stu-id="63253-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="63253-107">Példák</span><span class="sxs-lookup"><span data-stu-id="63253-107">EXAMPLES</span></span>

## <span data-ttu-id="63253-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63253-108">PARAMETERS</span></span>

### <span data-ttu-id="63253-109">-Force</span><span class="sxs-lookup"><span data-stu-id="63253-109">-Force</span></span>
<span data-ttu-id="63253-110">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="63253-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="63253-111">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="63253-111">-KeyName</span></span>
<span data-ttu-id="63253-112">Az újragenerálni kívánt kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="63253-112">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="63253-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="63253-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63253-114">Key1</span><span class="sxs-lookup"><span data-stu-id="63253-114">Key1</span></span>
- <span data-ttu-id="63253-115">Azonosító2</span><span class="sxs-lookup"><span data-stu-id="63253-115">Key2</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63253-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="63253-116">-Name</span></span>
<span data-ttu-id="63253-117">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="63253-117">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="63253-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63253-118">-ResourceGroupName</span></span>
<span data-ttu-id="63253-119">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="63253-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="63253-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="63253-120">-Confirm</span></span>
<span data-ttu-id="63253-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="63253-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63253-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63253-122">-WhatIf</span></span>
<span data-ttu-id="63253-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="63253-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63253-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63253-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63253-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63253-125">-DefaultProfile</span></span>
<span data-ttu-id="63253-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63253-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63253-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63253-127">CommonParameters</span></span>
<span data-ttu-id="63253-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63253-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63253-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63253-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63253-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63253-130">INPUTS</span></span>

## <span data-ttu-id="63253-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63253-131">OUTPUTS</span></span>

### <span data-ttu-id="63253-132">Microsoft. Azure. Management. CognitiveServices. models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="63253-132">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="63253-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63253-133">NOTES</span></span>

## <span data-ttu-id="63253-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63253-134">RELATED LINKS</span></span>

[<span data-ttu-id="63253-135">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="63253-135">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


