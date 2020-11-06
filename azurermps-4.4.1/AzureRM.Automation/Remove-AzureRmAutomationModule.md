---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 42fc322e9f593ecad6c295952d46274eb2563799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497932"
---
# <span data-ttu-id="ae335-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ae335-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="ae335-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae335-102">SYNOPSIS</span></span>
<span data-ttu-id="ae335-103">Modul eltávolítása az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="ae335-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae335-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae335-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae335-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae335-105">DESCRIPTION</span></span>
<span data-ttu-id="ae335-106">A **Remove-AzureRmAutomationModule** parancsmag automatizálási fiókból távolítja el a modult az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="ae335-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="ae335-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ae335-107">EXAMPLES</span></span>

### <span data-ttu-id="ae335-108">1. példa: modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ae335-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ae335-109">Ez a parancs eltávolítja a ContosoModule nevű modult a Contoso17 nevű automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="ae335-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ae335-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae335-110">PARAMETERS</span></span>

### <span data-ttu-id="ae335-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ae335-111">-AutomationAccountName</span></span>
<span data-ttu-id="ae335-112">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a modult.</span><span class="sxs-lookup"><span data-stu-id="ae335-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="ae335-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ae335-113">-Force</span></span>
<span data-ttu-id="ae335-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="ae335-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae335-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ae335-115">-Name</span></span>
<span data-ttu-id="ae335-116">Annak a modulnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="ae335-116">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ae335-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae335-117">-ResourceGroupName</span></span>
<span data-ttu-id="ae335-118">Annak az erőforráscsoportnek a nevét adja meg, amelyben a parancsmag eltávolítja a modult.</span><span class="sxs-lookup"><span data-stu-id="ae335-118">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="ae335-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ae335-119">-Confirm</span></span>
<span data-ttu-id="ae335-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae335-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae335-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae335-121">-WhatIf</span></span>
<span data-ttu-id="ae335-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae335-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae335-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae335-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae335-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae335-124">-DefaultProfile</span></span>
<span data-ttu-id="ae335-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae335-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae335-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae335-126">CommonParameters</span></span>
<span data-ttu-id="ae335-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae335-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae335-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae335-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae335-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae335-129">INPUTS</span></span>

## <span data-ttu-id="ae335-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae335-130">OUTPUTS</span></span>

## <span data-ttu-id="ae335-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae335-131">NOTES</span></span>

## <span data-ttu-id="ae335-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae335-132">RELATED LINKS</span></span>

[<span data-ttu-id="ae335-133">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ae335-133">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="ae335-134">Új – AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ae335-134">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="ae335-135">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ae335-135">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


