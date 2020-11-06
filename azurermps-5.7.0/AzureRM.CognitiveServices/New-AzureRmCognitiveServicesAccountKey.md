---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 1c3ebaf3e95c1094b02b73505e471d13015721d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493214"
---
# <span data-ttu-id="e4075-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e4075-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="e4075-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4075-102">SYNOPSIS</span></span>
<span data-ttu-id="e4075-103">Visszahozza a fiók kulcsát.</span><span class="sxs-lookup"><span data-stu-id="e4075-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4075-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4075-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4075-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4075-105">DESCRIPTION</span></span>
<span data-ttu-id="e4075-106">A **New-AzureRmCognitiveServicesAccountKey** parancsmag regenerálta egy API-kulcsot a kognitív szolgáltatások fiókjához.</span><span class="sxs-lookup"><span data-stu-id="e4075-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="e4075-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4075-107">EXAMPLES</span></span>

## <span data-ttu-id="e4075-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4075-108">PARAMETERS</span></span>

### <span data-ttu-id="e4075-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4075-109">-DefaultProfile</span></span>
<span data-ttu-id="e4075-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e4075-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4075-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e4075-111">-Force</span></span>
<span data-ttu-id="e4075-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e4075-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4075-113">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="e4075-113">-KeyName</span></span>
<span data-ttu-id="e4075-114">Az újragenerálni kívánt kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4075-114">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="e4075-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e4075-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e4075-116">Key1</span><span class="sxs-lookup"><span data-stu-id="e4075-116">Key1</span></span>
- <span data-ttu-id="e4075-117">Azonosító2</span><span class="sxs-lookup"><span data-stu-id="e4075-117">Key2</span></span>

```yaml
Type: KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4075-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4075-118">-Name</span></span>
<span data-ttu-id="e4075-119">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4075-119">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4075-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4075-120">-ResourceGroupName</span></span>
<span data-ttu-id="e4075-121">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e4075-121">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4075-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e4075-122">-Confirm</span></span>
<span data-ttu-id="e4075-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e4075-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4075-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4075-124">-WhatIf</span></span>
<span data-ttu-id="e4075-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e4075-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4075-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4075-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4075-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4075-127">CommonParameters</span></span>
<span data-ttu-id="e4075-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4075-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4075-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4075-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4075-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4075-130">INPUTS</span></span>

### <span data-ttu-id="e4075-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="e4075-131">None</span></span>
<span data-ttu-id="e4075-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e4075-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4075-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4075-133">OUTPUTS</span></span>

### <span data-ttu-id="e4075-134">Microsoft. Azure. Management. CognitiveServices. models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e4075-134">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="e4075-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4075-135">NOTES</span></span>

## <span data-ttu-id="e4075-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4075-136">RELATED LINKS</span></span>

[<span data-ttu-id="e4075-137">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e4075-137">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


