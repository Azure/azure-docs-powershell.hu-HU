---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: 8866c805f0cbb42d72c8940d31652bc8e5444cad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499224"
---
# <span data-ttu-id="f3104-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f3104-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="f3104-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3104-102">SYNOPSIS</span></span>
<span data-ttu-id="f3104-103">Automatizálási változó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="f3104-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3104-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3104-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3104-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3104-105">DESCRIPTION</span></span>
<span data-ttu-id="f3104-106">A **Remove-AzureRmAutomationVariable** parancsmag egy változót távolít el az Azure automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="f3104-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="f3104-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f3104-107">EXAMPLES</span></span>

### <span data-ttu-id="f3104-108">Példa 1: változó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f3104-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f3104-109">Ez a parancs eltávolítja a StringVariable22 nevű változót a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="f3104-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="f3104-110">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3104-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f3104-111">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3104-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f3104-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3104-112">PARAMETERS</span></span>

### <span data-ttu-id="f3104-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f3104-113">-AutomationAccountName</span></span>
<span data-ttu-id="f3104-114">Annak az automatizálási fióknak a neve, amely a parancsmag által törölt változót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f3104-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3104-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3104-115">-Name</span></span>
<span data-ttu-id="f3104-116">A parancsmag által törölt változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3104-116">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3104-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3104-117">-ResourceGroupName</span></span>
<span data-ttu-id="f3104-118">Azt az erőforráscsoport-csoportot adja meg, amelyhez ez a parancsmag törli a változót.</span><span class="sxs-lookup"><span data-stu-id="f3104-118">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="f3104-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3104-119">-Confirm</span></span>
<span data-ttu-id="f3104-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3104-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3104-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3104-121">-WhatIf</span></span>
<span data-ttu-id="f3104-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3104-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3104-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3104-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3104-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3104-124">-DefaultProfile</span></span>
<span data-ttu-id="f3104-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3104-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3104-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3104-126">CommonParameters</span></span>
<span data-ttu-id="f3104-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3104-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3104-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3104-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3104-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3104-129">INPUTS</span></span>

## <span data-ttu-id="f3104-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3104-130">OUTPUTS</span></span>

### <span data-ttu-id="f3104-131">Microsoft. Azure. Command. Automation. Model. változó</span><span class="sxs-lookup"><span data-stu-id="f3104-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="f3104-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3104-132">NOTES</span></span>

## <span data-ttu-id="f3104-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3104-133">RELATED LINKS</span></span>

[<span data-ttu-id="f3104-134">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f3104-134">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="f3104-135">Új – AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f3104-135">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="f3104-136">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f3104-136">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


