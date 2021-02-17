---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: efba6588697e34b371622eaa8a5f9a3c349d9ec0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205031"
---
# <span data-ttu-id="54712-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="54712-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="54712-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54712-102">SYNOPSIS</span></span>
<span data-ttu-id="54712-103">Újragenerálja a fiókkulcsot.</span><span class="sxs-lookup"><span data-stu-id="54712-103">Regenerates an account key.</span></span>

## <span data-ttu-id="54712-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="54712-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54712-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="54712-105">DESCRIPTION</span></span>
<span data-ttu-id="54712-106">A **New-AzCognitiveServicesAccountKey** parancsmag újragenerálja a Kognitív Szolgáltatások fiók API-kulcsát.</span><span class="sxs-lookup"><span data-stu-id="54712-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="54712-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="54712-107">EXAMPLES</span></span>

### <span data-ttu-id="54712-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="54712-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="54712-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54712-109">PARAMETERS</span></span>

### <span data-ttu-id="54712-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54712-110">-DefaultProfile</span></span>
<span data-ttu-id="54712-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="54712-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54712-112">-Force</span><span class="sxs-lookup"><span data-stu-id="54712-112">-Force</span></span>
<span data-ttu-id="54712-113">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="54712-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="54712-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="54712-114">-KeyName</span></span>
<span data-ttu-id="54712-115">Az újragenerálni megfelelő kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54712-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="54712-116">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="54712-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54712-117">Billentyű1</span><span class="sxs-lookup"><span data-stu-id="54712-117">Key1</span></span>
- <span data-ttu-id="54712-118">Billentyű2</span><span class="sxs-lookup"><span data-stu-id="54712-118">Key2</span></span>

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

### <span data-ttu-id="54712-119">-Name</span><span class="sxs-lookup"><span data-stu-id="54712-119">-Name</span></span>
<span data-ttu-id="54712-120">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54712-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="54712-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54712-121">-ResourceGroupName</span></span>
<span data-ttu-id="54712-122">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="54712-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="54712-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54712-123">-Confirm</span></span>
<span data-ttu-id="54712-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="54712-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54712-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54712-125">-WhatIf</span></span>
<span data-ttu-id="54712-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="54712-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54712-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54712-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54712-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54712-128">CommonParameters</span></span>
<span data-ttu-id="54712-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54712-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54712-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54712-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54712-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54712-131">INPUTS</span></span>

### <span data-ttu-id="54712-132">System.String</span><span class="sxs-lookup"><span data-stu-id="54712-132">System.String</span></span>

### <span data-ttu-id="54712-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span><span class="sxs-lookup"><span data-stu-id="54712-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="54712-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54712-134">OUTPUTS</span></span>

### <span data-ttu-id="54712-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="54712-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="54712-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="54712-136">NOTES</span></span>

## <span data-ttu-id="54712-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54712-137">RELATED LINKS</span></span>

[<span data-ttu-id="54712-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="54712-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


