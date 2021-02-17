---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: 1069365bb04cdf9a6d873e6fa86c61619b6d0dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205030"
---
# <span data-ttu-id="c983f-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c983f-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="c983f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c983f-102">SYNOPSIS</span></span>
<span data-ttu-id="c983f-103">A Kognitív szolgáltatások fiókjának törlése.</span><span class="sxs-lookup"><span data-stu-id="c983f-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="c983f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c983f-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c983f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c983f-105">DESCRIPTION</span></span>
<span data-ttu-id="c983f-106">A **Remove-AzCognitiveServicesAccount** parancsmag törli a megadott Kognitív szolgáltatások-fiókot.</span><span class="sxs-lookup"><span data-stu-id="c983f-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="c983f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c983f-107">EXAMPLES</span></span>

### <span data-ttu-id="c983f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c983f-108">Example 1</span></span>
<span data-ttu-id="c983f-109">Ez a parancs nem ad vissza semmit.</span><span class="sxs-lookup"><span data-stu-id="c983f-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="c983f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c983f-110">PARAMETERS</span></span>

### <span data-ttu-id="c983f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c983f-111">-DefaultProfile</span></span>
<span data-ttu-id="c983f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c983f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c983f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c983f-113">-Force</span></span>
<span data-ttu-id="c983f-114">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="c983f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c983f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c983f-115">-Name</span></span>
<span data-ttu-id="c983f-116">A törölni kívánt fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c983f-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="c983f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c983f-117">-ResourceGroupName</span></span>
<span data-ttu-id="c983f-118">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a Kognitív szolgáltatások fiók van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="c983f-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="c983f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c983f-119">-Confirm</span></span>
<span data-ttu-id="c983f-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c983f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c983f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c983f-121">-WhatIf</span></span>
<span data-ttu-id="c983f-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c983f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c983f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c983f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c983f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c983f-124">CommonParameters</span></span>
<span data-ttu-id="c983f-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c983f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c983f-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c983f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c983f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c983f-127">INPUTS</span></span>

### <span data-ttu-id="c983f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c983f-128">System.String</span></span>

## <span data-ttu-id="c983f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c983f-129">OUTPUTS</span></span>

### <span data-ttu-id="c983f-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="c983f-130">System.Void</span></span>

## <span data-ttu-id="c983f-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c983f-131">NOTES</span></span>

## <span data-ttu-id="c983f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c983f-132">RELATED LINKS</span></span>

[<span data-ttu-id="c983f-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c983f-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c983f-134">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c983f-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c983f-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c983f-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


