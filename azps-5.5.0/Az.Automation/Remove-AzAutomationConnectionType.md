---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 5eb31abcc632f06402b4196be8be4c5e32cdacf0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205511"
---
# <span data-ttu-id="5e76f-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="5e76f-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="5e76f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e76f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e76f-103">Eltávolít egy automatizálási kapcsolattípust.</span><span class="sxs-lookup"><span data-stu-id="5e76f-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="5e76f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e76f-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e76f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e76f-105">DESCRIPTION</span></span>
<span data-ttu-id="5e76f-106">A **Remove-AzAutomationConnectionType** parancsmag eltávolítja a kapcsolattípusokat az Azure Automationből.</span><span class="sxs-lookup"><span data-stu-id="5e76f-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="5e76f-107">A törölt kapcsolattípussal társított összes kapcsolat használhatatlanná válik.</span><span class="sxs-lookup"><span data-stu-id="5e76f-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="5e76f-108">Távolítsa el őket, hacsak nem hoz létre az alábbi feltételeknek megfelelő új kapcsolattípust:</span><span class="sxs-lookup"><span data-stu-id="5e76f-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="5e76f-109">A típus neve megegyezik az eredeti kapcsolattípus nevével.</span><span class="sxs-lookup"><span data-stu-id="5e76f-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="5e76f-110">A típusnak ugyanazok a meződefiníciói vannak, mint az eredeti kapcsolattípusnak.</span><span class="sxs-lookup"><span data-stu-id="5e76f-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="5e76f-111">További mezőket is tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="5e76f-111">It can have additional fields.</span></span>

## <span data-ttu-id="5e76f-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e76f-112">EXAMPLES</span></span>

### <span data-ttu-id="5e76f-113">1. példa: Kapcsolattípus eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5e76f-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5e76f-114">Ez a parancs eltávolítja a ContosoConnectionType nevű kapcsolattípust a Contoso17 nevű automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="5e76f-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5e76f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e76f-115">PARAMETERS</span></span>

### <span data-ttu-id="5e76f-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5e76f-116">-AutomationAccountName</span></span>
<span data-ttu-id="5e76f-117">Annak az automatizálási fióknak a nevét adja meg, amelyből a parancsmag eltávolítja a kapcsolattípust.</span><span class="sxs-lookup"><span data-stu-id="5e76f-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="5e76f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e76f-118">-DefaultProfile</span></span>
<span data-ttu-id="5e76f-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5e76f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e76f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5e76f-120">-Force</span></span>
<span data-ttu-id="5e76f-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="5e76f-121">ps_force</span></span>

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

### <span data-ttu-id="5e76f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5e76f-122">-Name</span></span>
<span data-ttu-id="5e76f-123">A parancsmag által eltávolított Automatizálási kapcsolattípus neve.</span><span class="sxs-lookup"><span data-stu-id="5e76f-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5e76f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e76f-124">-ResourceGroupName</span></span>
<span data-ttu-id="5e76f-125">Annak az erőforráscsoportnak a nevét adja meg, amelyből a parancsmag eltávolítja az automatizálási kapcsolattípust.</span><span class="sxs-lookup"><span data-stu-id="5e76f-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="5e76f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e76f-126">-Confirm</span></span>
<span data-ttu-id="5e76f-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5e76f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e76f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e76f-128">-WhatIf</span></span>
<span data-ttu-id="5e76f-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5e76f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e76f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e76f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e76f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e76f-131">CommonParameters</span></span>
<span data-ttu-id="5e76f-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e76f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e76f-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e76f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e76f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e76f-134">INPUTS</span></span>

### <span data-ttu-id="5e76f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5e76f-135">System.String</span></span>

## <span data-ttu-id="5e76f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e76f-136">OUTPUTS</span></span>

### <span data-ttu-id="5e76f-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="5e76f-137">System.Void</span></span>

## <span data-ttu-id="5e76f-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e76f-138">NOTES</span></span>

## <span data-ttu-id="5e76f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e76f-139">RELATED LINKS</span></span>

[<span data-ttu-id="5e76f-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5e76f-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


