---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: efba6588697e34b371622eaa8a5f9a3c349d9ec0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017887"
---
# <span data-ttu-id="c4a84-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="c4a84-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="c4a84-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4a84-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a84-103">Visszahozza a fiók kulcsát.</span><span class="sxs-lookup"><span data-stu-id="c4a84-103">Regenerates an account key.</span></span>

## <span data-ttu-id="c4a84-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4a84-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4a84-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4a84-105">DESCRIPTION</span></span>
<span data-ttu-id="c4a84-106">A **New-AzCognitiveServicesAccountKey** parancsmag regenerálta egy API-kulcsot a kognitív szolgáltatások fiókjához.</span><span class="sxs-lookup"><span data-stu-id="c4a84-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="c4a84-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c4a84-107">EXAMPLES</span></span>

### <span data-ttu-id="c4a84-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c4a84-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="c4a84-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4a84-109">PARAMETERS</span></span>

### <span data-ttu-id="c4a84-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a84-110">-DefaultProfile</span></span>
<span data-ttu-id="c4a84-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c4a84-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4a84-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c4a84-112">-Force</span></span>
<span data-ttu-id="c4a84-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c4a84-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4a84-114">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="c4a84-114">-KeyName</span></span>
<span data-ttu-id="c4a84-115">Az újragenerálni kívánt kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4a84-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="c4a84-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c4a84-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c4a84-117">Key1</span><span class="sxs-lookup"><span data-stu-id="c4a84-117">Key1</span></span>
- <span data-ttu-id="c4a84-118">Azonosító2</span><span class="sxs-lookup"><span data-stu-id="c4a84-118">Key2</span></span>

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

### <span data-ttu-id="c4a84-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4a84-119">-Name</span></span>
<span data-ttu-id="c4a84-120">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4a84-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="c4a84-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a84-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4a84-122">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="c4a84-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="c4a84-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c4a84-123">-Confirm</span></span>
<span data-ttu-id="c4a84-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c4a84-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a84-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a84-125">-WhatIf</span></span>
<span data-ttu-id="c4a84-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c4a84-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a84-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4a84-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a84-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a84-128">CommonParameters</span></span>
<span data-ttu-id="c4a84-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4a84-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a84-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c4a84-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a84-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4a84-131">INPUTS</span></span>

### <span data-ttu-id="c4a84-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c4a84-132">System.String</span></span>

### <span data-ttu-id="c4a84-133">Microsoft. Azure. Management. CognitiveServices. modellek. kulcsnév</span><span class="sxs-lookup"><span data-stu-id="c4a84-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="c4a84-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4a84-134">OUTPUTS</span></span>

### <span data-ttu-id="c4a84-135">Microsoft. Azure. Management. CognitiveServices. models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c4a84-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="c4a84-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4a84-136">NOTES</span></span>

## <span data-ttu-id="c4a84-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4a84-137">RELATED LINKS</span></span>

[<span data-ttu-id="c4a84-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="c4a84-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


