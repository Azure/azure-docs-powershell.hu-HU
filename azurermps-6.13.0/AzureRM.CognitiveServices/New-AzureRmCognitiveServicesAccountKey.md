---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 4701ae347f5a6ea8cd294a0ff75efa51f4d1370d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673170"
---
# <span data-ttu-id="08022-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="08022-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="08022-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08022-102">SYNOPSIS</span></span>
<span data-ttu-id="08022-103">Visszahozza a fiók kulcsát.</span><span class="sxs-lookup"><span data-stu-id="08022-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08022-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08022-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08022-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="08022-105">DESCRIPTION</span></span>
<span data-ttu-id="08022-106">A **New-AzureRmCognitiveServicesAccountKey** parancsmag regenerálta egy API-kulcsot a kognitív szolgáltatások fiókjához.</span><span class="sxs-lookup"><span data-stu-id="08022-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="08022-107">Példák</span><span class="sxs-lookup"><span data-stu-id="08022-107">EXAMPLES</span></span>

### <span data-ttu-id="08022-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="08022-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="08022-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08022-109">PARAMETERS</span></span>

### <span data-ttu-id="08022-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08022-110">-DefaultProfile</span></span>
<span data-ttu-id="08022-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="08022-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08022-112">-Force</span><span class="sxs-lookup"><span data-stu-id="08022-112">-Force</span></span>
<span data-ttu-id="08022-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="08022-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08022-114">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="08022-114">-KeyName</span></span>
<span data-ttu-id="08022-115">Az újragenerálni kívánt kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08022-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="08022-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="08022-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="08022-117">Key1</span><span class="sxs-lookup"><span data-stu-id="08022-117">Key1</span></span>
- <span data-ttu-id="08022-118">Azonosító2</span><span class="sxs-lookup"><span data-stu-id="08022-118">Key2</span></span>

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

### <span data-ttu-id="08022-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08022-119">-Name</span></span>
<span data-ttu-id="08022-120">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08022-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="08022-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08022-121">-ResourceGroupName</span></span>
<span data-ttu-id="08022-122">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="08022-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="08022-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="08022-123">-Confirm</span></span>
<span data-ttu-id="08022-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="08022-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08022-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08022-125">-WhatIf</span></span>
<span data-ttu-id="08022-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="08022-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08022-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08022-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08022-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08022-128">CommonParameters</span></span>
<span data-ttu-id="08022-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08022-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08022-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08022-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08022-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08022-131">INPUTS</span></span>

### <span data-ttu-id="08022-132">System. String</span><span class="sxs-lookup"><span data-stu-id="08022-132">System.String</span></span>

### <span data-ttu-id="08022-133">Microsoft. Azure. Management. CognitiveServices. modellek. kulcsnév</span><span class="sxs-lookup"><span data-stu-id="08022-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="08022-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08022-134">OUTPUTS</span></span>

### <span data-ttu-id="08022-135">Microsoft. Azure. Management. CognitiveServices. models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="08022-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="08022-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08022-136">NOTES</span></span>

## <span data-ttu-id="08022-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08022-137">RELATED LINKS</span></span>

[<span data-ttu-id="08022-138">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="08022-138">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


